<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN" "http://www.w3.org/TR/REC-html40/loose.dtd">
<html><body><h1 id="batch-webfont-how-to-and-faq"><a href="#batch-webfont-how-to-and-faq" class="section-link">&#61544;</a>Batch Webfont How-To and FAQ</h1>

<h3 id="this-guide-is-not-the-only-way-to-incorporate-the-batch-webfont-into-your-work-i-am-far-from-classing-myself-as-a-developer-it-is-just-a-guide-to-help-you-understand-more-how-the-web-font-is-constructed-and-how-you-could-implement-it"><a href="#this-guide-is-not-the-only-way-to-incorporate-the-batch-webfont-into-your-work-i-am-far-from-classing-myself-as-a-developer-it-is-just-a-guide-to-help-you-understand-more-how-the-web-font-is-constructed-and-how-you-could-implement-it" class="section-link">&#61544;</a>This guide is not the only way to incorporate the Batch webfont into your work. I am far from classing myself as a developer. It is just a guide to help you understand more how the web-font is constructed and how you could implement it.</h3>

<h4 id="if-you-get-stuck-at-all-or-require-further-details-the-quickest-way-to-contact-me-is-via-my-twitter"><a href="#if-you-get-stuck-at-all-or-require-further-details-the-quickest-way-to-contact-me-is-via-my-twitter" class="section-link">&#61544;</a>If you get stuck at all, or require further details the quickest way to contact me is via my <a href="http://twitter.com/sdmix">twitter</a>.</h4>

<h5 id="font-face-setup"><a href="#font-face-setup" class="section-link">&#61544;</a>Font Face Setup</h5>

<p class="post__intro">First up, let's get the CSS for getting the Batch web-font into your project:</p><div class="cf"></div>

<pre class="prettyprint  linenums"><code>  @font-face{
    font-family:Batch;
    src:url('assets/batch.eot');
    src:url('assets/batch.eot?#iefix') format('embedded-opentype'),
      url('assets/batch.woff') format('woff'),
      url('assets/batch.ttf') format('truetype'),
      url('assets/batch.svg#batchregular') format('svg');
    font-weight:normal;
    font-style:normal;
  }
</code></pre>

<p>In this example, the font files are located in the <em>root/assets/</em>  folder, if this isn't where you plan on storing the files, just change these values.
Once you've got this in your CSS, you're set up and ready to go.</p>

<h5 id="css-setup"><a href="#css-setup" class="section-link">&#61544;</a>CSS Setup</h5>

<p>The Batch web-font is designed and built to be give you pixel perfect icons at the size you declare within your CSS. So using the following code:</p>

<pre class="prettyprint  linenums"><code>  .batch {
    font-family:"Batch"; /*or whatever you've decalred your font name as*/
    font-size:16px;
    line-height:1;
    display:inline-block;
  }
</code></pre>

<p>will give you the icon at 16px. This is handy for when you're working from your designs.</p>

<h5 id="pulling-the-icons"><a href="#pulling-the-icons" class="section-link">&#61544;</a>Pulling the icons</h5>

<p>All the icons in the Batch web-font are within the Private Unicode character range. This means that if for any reason the font file fails to load, you will either see nothing or a blank square depending on your system setup.
This also stops screen readers from reading out your icon's as letters. Something that is useful for accessability.
The easiest way to quickly test to make sure your code is working and the font is loading correctly is to place the following into your markup (based on the above code example):</p>

<pre class="prettyprint  linenums"><code>&lt;div class="batch"&gt;
  &amp;#xf000; &amp;#xf001; &amp;#xf002; &amp;#xf003; &amp;#xf004;
&lt;/div&gt;
</code></pre>

<p>Loading the page should show you some lovely icons at 16px. Nice.
If it doesn't check your developer tools to make sure the fonts are loading in correctly. If there is an issue, you might have a corrupt font file for the browser you are using.</p>

<h5 id="where-to-from-here"><a href="#where-to-from-here" class="section-link">&#61544;</a>Where to from here</h5>

<p>You can use the example above as the basic starting point. 
There are many ways you can implement the font into your work, the above was just to show you the basic way.</p>

<p>My personal favourite would be using the following markup:</p>

<pre class="prettyprint  linenums"><code>&lt;a href="#"&gt;&lt;i class="batch" data-icon="&amp;#xF000;"&gt;&lt;/i&gt; Join the Conversation&lt;/a&gt;
</code></pre>

<p>With the above code plus the following extra line in your CSS:</p>

<pre class="prettyprint  linenums"><code>.batch:before {
    content:attr(data-icon);
}
</code></pre>

<p>You can then also add sizing elements to alter the size of the icons produced:</p>

<pre class="prettyprint  linenums"><code>.batch--large { font-size:32px; }
.batch--huge { font-size:64px; }
.batch--natural { font-size:inherit; }
</code></pre>

<p>Pretty cool right!</p>

<h4 id="further-questions-or-ideas"><a href="#further-questions-or-ideas" class="section-link">&#61544;</a>Further questions or ideas?</h4>

<p>Hit me up on [Twitter](https://twitter.com/intent/tweet?text=@sdmix Hey dude! I've got a question about the Batch web-font......) with any questions you'd like to see answered here. I live in the UK, so apologies if the time difference means I can't get back to you straight away but I'll be as quick as I can in getting back to you.</p></body></html>
