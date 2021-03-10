# Web-scraping and OpenRefine

Thursday, March 11



## What is HTML?
<section>
  <pre><code>
	<h1> This is header </h1>
	<p> This is a paragraph </p>
	<p> This is a paragraph <a href="https://sceckert.github.io/IntroDHSpring2021/">linking to our course webpage.</a></p>
  </code></pre>
</section>



## What is OpenRefine?



## What is an API??!



1. Create new project on clipboard and paste in the following:
<section>
  <pre><code>
artist, album
Beyonce, Lemonade
Beyonce, Beyonce
  </code></pre>
</section>

2. Create column called album_tracklist_urls based on column artist using the following expression (in GREL)
<section>
  <pre><code>
	"https://genius.com/albums/" + value.escape('url') + "/" +cells['album'].value.escape('url')"
  </code></pre>
</section>



3. Create column called album_html by fetching URLs based on column album_tracklist_urls using the following expression (in GREL)
<section>
  <pre><code>
	value
  </code></pre>
</section>

4. Create column release_date based on column album_html using the following expression (in GREL):
<section>
  <pre><code>
	value.parseHtml().select("div.metadata_unit")[0].htmlText()
  </code></pre>
</section>



5. Create column song_titles based on column album_html using the following expression (in GREL):
<section>
  <pre><code>
	forEach(value.parseHtml().select("h3.chart_row-content-title"),e,e.htmlText()).join(" ||| ")
  </code></pre>
</section>

6. Create column song_titles_urls based on column album_html using the following expression (in GREL)
<section>
  <pre><code>
	forEach(value.parseHtml().select("a[href].u-display_block"),e,e.htmlAttr("href")).join(" ||| ")
  </code></pre>
</section>



7. Split multi-valued cells in column song_titles_urls

8. Split multi-valued cells in column song_titles

9. Remove column album_html 



10. Fill down cells in column release_date

11. Fill down cells in column album

12. Fill down cells in column artist

13. Fill down cells in column album_tracklist_urls 



14. Create column song_lyrics_html at index 3 by fetching URLs based on column song_titles_urls using the following expression (in GREL):
<section>
  <pre><code>
	value
  </code></pre>
</section>

15. Create column song_lyrics_text at index 4 based on column song_lyrics_html using the following expression (in GREL):
<section>
  <pre><code>
	value.parseHtml().select("p")[0].htmlText()
  </code></pre>
</section>

16. Remove column song_lyrics_html

17. Reorder columns