# ExampleHomeSubdirectory
An stripped down example to illustrate the problem I am having moving the hugo homepage into a subdirectory
___________________________

For this exercise I would like to move my entire hugo website to a subdirectory.

In the configuration file I have set <code>baseURL = 'http\://example.com/subdir/'</code>

If I run hugo now, it correctly processes the image and its hyperlink, but the link to the other website page is now broken - it refers to example.com/new_page rather than example.com/subdir/new_page.

I have read elsewhere that adding combinations of 
  <code>relativeURLs= "true"</code>
and
  <code>canonifyURLs = "true"</code>
to config.toml can help. However, no combination seems to work for both links. If I include both, then the link to the new page is processed correctly, but now the image hyperlink is broken.

_______________________


Note: I have added 
<code>
[markup]
  [markup.goldmark]
    [markup.goldmark.renderer]
      unsafe = true
</code>
into the config.toml file since I want to include some html in the markdown.
