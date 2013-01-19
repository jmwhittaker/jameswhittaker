---
layout: post
title: Em based layouts - Vertical rhythm calculator
published: false
tags: [css]
---

Typography on the web has become a point of focus for standards based developers recently. The pioneering work by <a href="http://www.markboulton.co.uk/">Mark Boulton</a> and <a href="http://clagnut.com/">Richard Rutter</a> has highlighted the importance of good web typography. With the advent of more standards compliant browsers and a better understanding of the capabilities of <span class="caps">CSS</span>, more developers are spending the extra time and effort in pursuit of typography excellence within their designs.

For years we have touted the phrase &lsquo;the web is not print&rsquo; and consequently have forgotten about the basics of designing for type, like working to a baseline rhythm. I have come across many a design where the developer has not thought about typography before diving straight into the code. The result is a mess of random amounts of padding and margin married with unnecessary style rules, this in turn leads to <span class="caps">CSS</span> code that is harder to understand and maintain.

One of the key concepts that we can use within our sites is consistent line-height in <span class="caps">CSS</span>terms. If you think of a ruled notebook, the lines are all equal heights.

The concept is fairly straight forward but in practice can be confusing especially for a <span class="caps">CSS</span>newcomer. All sizing needs to be relative to the base size. This allows for easy scaling up or down while keeping the required spacing and layout consistent, this can be refereed to as an elastic layout. To allow this we need to specify measurements in percent or em.
<h4>What is an <strong>em</strong> measurement?</h4>
A <strong>pixel</strong> is the &lsquo;dot&rsquo; on your computer screen. Displays are measured in pixels across and down like 1024 &times; 768. These dots are unscalable and fixed in size. In some situations this is desirable and it would be better to set your measurements as pixels.

An <strong>em</strong> is a relative measurement based on the square of the font size at that particular point. As font sizes can vary across differing systems and displays, the result is that the <strong>em</strong>measurement will always be relatively sized and scalable.

As we are now developing for a wider range of devices and screen sizes we should look to adopt em instead of pixels in all of our designs. Let&rsquo;s take a look at how.

## The browser default size

Modern browsers ( IE7, Opera, Safari and Mozilla ) have a built in default font size of 16px so we can use that as the cornerstone for all of our sizing calculations from now on. At this point we need to make a choice as to the base font-size we are going to work with, nominally this will be 12px or 14px which we can set as a percentage of the 16px browser default. An example for 12px required size would be:

    12 / 16 * 100 = 75%

As usual it&rsquo;s not always that simple and Safari 2 does apply a 13px base size to fixed width fonts. To overcome this situation you will need to tell Safari to use a base size as a set pixel value, like 16px or 12px. Beware though that you must use conditional comments to block that statement from IE. For IE&rsquo;s font scaling to work correctly it needs to be given a relative base size set in percent or em. For more guidance I refer you to Richard&rsquo;s article on <a href="http://www.alistapart.com/">A List Apart</a> titled &ndash; <a href="http://www.alistapart.com/articles/howtosizetextincss">how to size text in CSS</a>.

## Working out a required font-size

Well that&rsquo;s why I built the calculator! to save you the hassle of all of those calculations. I&rsquo;m going to cheat here and direct you to a great article on <a href="http://24ways.org/">24ways</a> titled &ndash; <a href="http://24ways.org/2006/compose-to-a-vertical-rhythm">composing to a vertical rhythm</a>. This is the background to the calculations behind my calculator.

## Using the calculator

The calculator defaults to a required base font-size of 12px and a 21px line-height. If you have set yours to be any different then please change this now. Some people prefer a line-height to be 1.5 x the base font-size, I personally prefer a larger 1.75 x the font size. It give more breathing space I feel.

Now you have set the base sizes you need to start adding some style rules, so click the button and the interface will expand down. Now give the style a name, this could be <strong>p</strong> or<strong>h1</strong> or any standard rule or your own based on your markup. This name will be in the <span class="caps">CSS</span>and can be altered later.

The parent rule is there for creating cascading calculations. Font-sizes in em&rsquo;s are always based of the parent font-size. So if you need it it&rsquo;s there if not then leave it set to document base.

Next type your required font-size in pixels and push the calculate button. Your <span class="caps">CSS</span> will be there ready to copy to the clipboard and the options to add padding or margins that will live update in the <span class="caps">CSS</span> code. <span class="caps">BEWARE</span> that if you change your font-size you will need to click the recalculate button as all the other measurements are based off the font-size.

The margins and padding are in line height units, refer to the <a href="http://24ways.org/2006/compose-to-a-vertical-rhythm">24ways article</a> for more understanding or send me an email if your stuck.

The final thing is that you have a simple em calculator for working out pixel to em values based upon the current set font-size. You could use this for working out the width of an element in em&rsquo;s. Where your design is say 120px you could get that value in em&rsquo;s. Just enter the pixel value in the box and it will auto calculate.

## Em Calculator &ndash; Adobe AIR application

The AIR application is no longer available. This is also a post from my previous blog in 2008 so time move on.



