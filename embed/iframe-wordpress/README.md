# Embed an iFrame on WordPress.org

*Last updated by [Jack Dougherty](../../introduction/who.md) on February 11, 2016*

**TO DO**
- rewrite this tutorial to merge the two versions (top and bottom)

To embed one web page (the data visualization) inside a second web page (the organization's website), we use a simple HTML code known as **iframe**. (Read more about the <a href="http://www.w3schools.com/tags/tag_iframe.asp">iframe</a><a href="http://www.w3schools.com/tags/tag_iframe.asp">tag at W3Schools</a>.)

The **general iframe concept** works across many data visualization tools and many websites:
- Copy the embed code or URL from your dataviz website
- Paste (and modify) the code as an iframe in your destination website

To embed your dataviz in a self-hosted Wordpress.org site, the [iframe plugin] (http://wordpress.org/plugins/iframe/) must be installed and activated. This plugin allows authors to embed iframe codes inside posts/pages, in a modified "shortcode" format surrounded by square brackets. Without the plugin, self-hosted WordPress.org sites will usually "strip out" iframe codes for all users except the site administrator. **I have already installed and activated** the iframe plugin on my site, and the Dashboard view looks like this:

![](WordPressOrg-iframe-plugin-activate.jpg)

Note that most WordPress.com sites do NOT support an iframe embed code.

But details vary, so read and experiment with the examples that follow.


5) To embed the iframe in a WordPress.org site, the iframe plugin must be installed, as explained in the [Embed with iframe on WordPress.org](embed/iframe-wordpress) chapter.

6) Log into your Wordpress.org site and create a new post. In the editor window, switch from the Visual to the Text tab, which allows users to modify the code behind your post. Paste the iframe code from your interactive dataviz.

![](WordPressOrg-text-tab-paste-iframe.png)

7) Initially, the code you pasted includes HTML iframe tags at the front (<iframe...) and the end (...></iframe>), which looks like this:

```javascript
<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/1fwnl5hvkkwz-YDZrogyGnx274BqmozGlIeXyjJ2TKmE/pubchart?oid=462316012&amp;format=interactive"></iframe>
```

8) Modify the front end of the iframe code by replacing the less-than symbol ( < ) with a square opening bracket ( [ ). Modify the back end by erasing the greater-than symbol ( > ) and the end tag ( </iframe> ). Replace the back end with a square closing bracket ( ] ).

![](WordPressOrg-replace-with-bracket.png)

Your modified code should look like this:
```
[iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/1fwnl5hvkkwz-YDZrogyGnx274BqmozGlIeXyjJ2TKmE/pubchart?oid=462316012&amp;format=interactive"]
```

9) Click Preview or Publish/View Post to see how it appears on the web.

10) If desired, continue to modify the iframe code to improve the display of your dataviz on your website. For example, the initial code was 600 pixels wide (width="600"). To display the dataviz across the full width of your website, change this part of the code to 100% (width="100%").


The goal is to embed an interactive chart inside your website, so that users can explore the data. This tutorial displays a *very basic chart* to simplify the process, and the end result will appear like the one below. Try it.

<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/1fwnl5hvkkwz-YDZrogyGnx274BqmozGlIeXyjJ2TKmE/pubchart?oid=462316012&amp;format=interactive"></iframe>

{% footer %}
{% endfooter %}
