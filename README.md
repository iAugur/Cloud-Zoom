Cloud-Zoom
==========

Cloudzoom v1 blank image fix

see full details here http://bit.ly/S20r7I

Forked from: http://www.professorcloud.com/downloads/cloud-zoom.1.0.2.zip

the Mousetrap Div has a background image that doesn't exist so we get 404 errors all the time
<pre>
<code>
style='background-image:url(\".\");
</code>
</pre>
This fork puts an inline transparent 1x1 gif in the background so we it still works as a mousetrap but we don't get a 404
Transparent gif idea from here http://css-tricks.com/snippets/html/base64-encode-of-1x1px-transparent-gif/
<pre>
<code>
style='background-image:url(data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7);
</code>
</pre>

In v1.0.3 uses a blank.gif - but this method still avoids an http call for a 1x1 gif

Forked from http://www.professorcloud.com/downloads/cloud-zoom.1.0.3.zip
