<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN" "http://www.w3.org/TR/REC-html40/loose.dtd">
<html><body><h1 id=""><a href="#" class="section-link">&#61544;</a><img src="http://inuitcss.com/img/content/logo.png" alt="inuit.css" class="img--stripe"></h1>

<p class="post__intro">inuit.css is a powerful little framework designed for <em>serious</em> developers.</p><div class="cf"></div>

<p>It is a Sass based, Object Oriented framework that is full of objects and
abstractions. inuit.css provides little-to-no design which means no undoing
things, no deleting CSS and no adhering to other peoples&acirc;&#128;&#153; design decisions.</p>

<p>inuit.css is built on a <a href="http://bem.info/">BEM</a>-style naming convention and
honed based on <a href="https://gist.github.com/1309546">work done by Nicolas Gallagher</a>.</p>

<p>inuit.css is ideally suited to designers who want to focus on the creative and
not code, and developers who understand the need for abstraction and an OO
approach.</p>

<p>inuit.css gives you design patterns, not design decisions. It features nestable,
fluid grids; a double-stranded heading hierarchy; sprites; buttons and a lot,
<em>lot</em> more.</p>

<p><strong>Use inuit.css if:</strong></p>

<ul><li>You need a powerful library of objects and abstractions.</li>
<li>You understand/appreciate the value of OO code and the need for scalability
and reuse.</li>
<li>You are a confident/competent developer comfortable with OOCSS and Sass, as
well as familiarity with OO principles in general.</li>
</ul><p><strong>Do not use inuit.css if:</strong></p>

<ul><li>You need a framework that supplies design (I&acirc;&#128;&#153;d recommend
<a href="http://twitter.github.com/bootstrap/">Bootstrap</a> for that).</li>
</ul><h2 id="browser-support"><a href="#browser-support" class="section-link">&#61544;</a>Browser support</h2>

<p>inuit.css is a modern framework for modern browsers. It takes advantage of
<a href="http://necolas.github.com/normalize.css/">normalize.css</a> and global
<code>box-sizing:border-box;</code> (optional). As such, inuit.css is intended for <strong>IE8</strong>
and above only.  The last release to support IE7 was
<a href="https://github.com/csswizardry/inuit.css/archive/v4.1.5.zip">v4.1.5</a>.</p>

<h2 id="the-developer"><a href="#the-developer" class="section-link">&#61544;</a>The developer</h2>

<p>There are a million-and-one different CSS frameworks out there so this rather
cringeworthy section is an attempt to validate inuit.css and give it some
credibility&acirc;&#128;&brvbar;</p>

<p>I am <a href="http://hry.rbrts.me">Harry Roberts</a>, I am a 22 year old developer and
front-end architect from the UK. I work as a Senior UI Developer for
<a href="http://en.wikipedia.org/wiki/BSkyB">BSkyB</a> where it is my job to build scalable
front-ends, write internally used CSS frameworks and libraries, and to architect
CSS and front-end builds.</p>

<p>I <a href="http://csswizardry.com">write</a>, <a href="http://twitter.com/csswizardry">tweet</a> and
<a href="http://speakerdeck.com/u/csswizardry/">speak</a> about OOCSS, scalable CSS,
maintainability, working in large teams, CSS performance, CSS architecture and a
whole lot more.</p>

<p>inuit.css is the result of years of my specialism in CSS (as CSS is all I do).
It is a collection of design patterns, objects, and abstractions that have been
refined and bulletproofed over hours of development across an array of projects
of varying sizes. inuit.css is the result of hundreds of hours of work all
condensed into one powerful little framework.</p>

<h2 id="installation"><a href="#installation" class="section-link">&#61544;</a>Installation</h2>

<p><strong>Requires Sass 3.2</strong></p>

<p><a href="http://www.youtube.com/watch?v=IkaILVOgGRA&amp;hd=1"><strong>Watch <em>An introduction to inuit.css</em> screencast</strong></a></p>

<p>inuit.css is incredibly easy to get up and running (provided you&acirc;&#128;&#153;re all set for
Sass). Simply <a href="https://github.com/csswizardry/inuit.css/zipball/master">download the latest version</a>
of inuit.css from right here on GitHub, unpack the zip file, rename
<code>your-project.scss</code> to whatever your project is called and then watch that file.</p>

<p>You can watch the file by <code>cd</code>ing into the directory that houses the <code>.scss</code>
and running the following:</p>

<pre class="prettyprint  linenums"><code>sass --watch [your-project].scss:[your-project].min.css --style compressed
</code></pre>

<p>&acirc;&#128;&brvbar;where <code>[your-project]</code> is the name you have chosen for your build.</p>

<p>Alternatively you can modify <a href="https://github.com/csswizardry/inuit.css/blob/master/watch.sh"><code>watch.sh</code></a>
to reflect the name of your project and simply run:</p>

<pre class="prettyprint  linenums"><code>sh watch.sh
</code></pre>

<p>&acirc;&#128;&brvbar;from the command line.</p>

<p>That&acirc;&#128;&#153;s it, your project is now set up on inuit.css.</p>

<p>To begin adding your styles on top of inuit.css just begin including things in
<a href="https://github.com/csswizardry/inuit.css/blob/master/your-project.scss#L22"><code>[your-project].scss</code></a>
<em>after</em> you&acirc;&#128;&#153;ve called in your variables and the inuit.css framework.</p>

<p>If there are any  objects and abstractions you <em>don&acirc;&#128;&#153;t</em> use in your project, it
is advisable that you comment out their inclusion in
<a href="https://github.com/csswizardry/inuit.css/blob/master/inuit.css/inuit.scss"><code>inuit.scss</code></a>.
For example, if your project doesn&acirc;&#128;&#153;t require any pagination, text columns or
flyouts, you&acirc;&#128;&#153;d have:</p>

<pre class="prettyprint  linenums"><code>   @import "partials/objects/grids";
   @import "partials/objects/flexbox";
// @import "partials/objects/columns";
   @import "partials/objects/nav";
// @import "partials/objects/pagination";
   @import "partials/objects/media";
   @import "partials/objects/island";
   @import "partials/objects/block-list";
   @import "partials/objects/matrix";
   @import "partials/objects/split";
   @import "partials/objects/this-or-this";
   @import "partials/objects/complex-link";
// @import "partials/objects/flyout";
   @import "partials/objects/sprite";
   @import "partials/objects/icon-text";
   @import "partials/objects/buttons";
   @import "partials/objects/lozenges";
   @import "partials/objects/greybox";
</code></pre>

<p>This ensures that you aren&acirc;&#128;&#153;t packaging more than you need to.</p>

<h2 id="footprint"><a href="#footprint" class="section-link">&#61544;</a>Footprint</h2>

<p><strong>inuit.css is tiny.</strong> The full framework &acirc;&#128;&#147; <em>including</em> debug mode &acirc;&#128;&#147; once minified
and gzipped weighs <strong>less than 5.6kB</strong></p>

<p>It is essential to <strong>compile to a minified file</strong> because inuit.css is packed
full of comments and whitespace; so much so that it would be detrimental to
your website&acirc;&#128;&#153;s performance to serve the unminified version.</p>

<h2 id="documentation"><a href="#documentation" class="section-link">&#61544;</a>Documentation</h2>

<p>There are no official docs for inuit.css because the code <em>is</em> the
documentation. Everything is heavily commented with example HTML. If you
struggle with anything please tweet at <a href="http://twitter.com/inuitcss">@inuitcss</a>
and/or <a href="https://github.com/csswizardry/inuit.css/issues">open an issue</a> and I&acirc;&#128;&#153;ll
try help out and use your feedback to improve the documentation.</p>

<h3 id="demos"><a href="#demos" class="section-link">&#61544;</a>Demos</h3>

<p>Although there are no docs as such, there is <a href="http://jsfiddle.net/user/inuitcss/fiddles/">a dedicated inuit.css jsFiddle
account</a> which houses plenty of
demos of various aspects of the framework.</p>

<h3 id="development"><a href="#development" class="section-link">&#61544;</a>Development</h3>

<p>You can keep up-to-date with upcoming features, suggestions and fixes by looking
at the <a href="https://trello.com/board/inuit-css/50a16487543dea585502f3d2">inuit.css Trello board</a>.</p>

<h2 id="looking-for-a-little-less"><a href="#looking-for-a-little-less" class="section-link">&#61544;</a>Looking for a little LESS?</h2>

<p><a href="http://twitter.com/pwcc">Peter Wilson</a> is maintaining a LESS port of inuit.css:
check <a href="https://github.com/peterwilsoncc/inuit.css">the GitHub repo</a>.</p>

<h2 id="using-compass"><a href="#using-compass" class="section-link">&#61544;</a>Using Compass?</h2>

<p><a href="http://github.com/stephenway">Stephen Way</a> is maintaining a Compass port of
inuit.css: check <a href="https://github.com/stephenway/compass-inuit">the GitHub repo</a>.</p>

<h2 id="test-drive"><a href="#test-drive" class="section-link">&#61544;</a>Test-drive</h2>

<p>If you would like to try inuit.css out before you download anything there is a
compiled version <a href="http://jsfiddle.net/inuitcss/a6yS3/">on jsFiddle</a> that you
are encouraged to fork and play with. Refer back to
<a href="https://github.com/csswizardry/inuit.css/blob/master/inuit.css/inuit.scss">the source here on GitHub</a>
for documentation.</p>

<h2 id="as-used-by"><a href="#as-used-by" class="section-link">&#61544;</a>As used by</h2>

<ul><li><a href="http://en.wikipedia.org/wiki/BSkyB">BSkyB</a></li>
<li><a href="http://pr.ofile.me">pr.ofile.me</a></li>
<li><a href="http://lu-x.me">Lukas Bestle</a></li>
<li><a href="http://matthewtyas.com/">Matthew Tyas</a></li>
</ul><h3 id="using-inuit-css"><a href="#using-inuit-css" class="section-link">&#61544;</a>Using inuit.css?</h3>

<p>If you use inuit.css on a live project then <a href="http://twitter.com/inuitcss">tweet at me</a>
and I&acirc;&#128;&#153;ll send you some inuit.css stickers!</p>

<h2 id="support-inuit-css"><a href="#support-inuit-css" class="section-link">&#61544;</a>Support inuit.css</h2>

<p>If you use and/or like inuit.css, perhaps you might consider <a href="http://gum.co/nOoht">supporting it
through Gumroad</a>.</p>

<h2 id="credits"><a href="#credits" class="section-link">&#61544;</a>Credits</h2>

<p>inuit.css, although produced and maintained by one developer, could not have
been possible without inspiration and work from an array of other people.</p>

<ul><li><strong><a href="https://twitter.com/stubbornella">Nicole Sullivan</a></strong> for her work on OOCSS</li>
<li><strong><a href="https://twitter.com/snookca">Jonathan Snook</a></strong> for his work on SMACSS</li>
<li><strong><a href="https://twitter.com/necolas">Nicolas Gallagher</a></strong> for his work on numerous
CSS things</li>
<li><strong><a href="https://twitter.com/WengersToyBus">Bryan James</a></strong> for the inuit.css logo</li>
</ul><p>And probably more&acirc;&#128;&brvbar;</p>

<h2 id="license"><a href="#license" class="section-link">&#61544;</a>License</h2>

<p>Copyright 2012 Harry Roberts</p>

<p>Licensed under the Apache License, Version 2.0.</p>

<hr><p><strong>inuit.css is the most powerful little framework out there, and it&acirc;&#128;&#153;s ready to
go!</strong></p></body></html>
