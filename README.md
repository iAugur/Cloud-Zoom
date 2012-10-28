Cloud-Zoom
==========

Cloudzoom v1 blank image fix

Forked from: http://www.professorcloud.com/downloads/cloud-zoom.1.0.2.zip

the Mousetrap Div has a background image that doesn't exist so we get 404 errors all the time

$mouseTrap = jWin.parent().append(format("<div class='mousetrap' style='background-image:url(\".\");z-index:999;position:absolute;width:%0px;height:%1px;left:%2px;top:%3px;\'></div>", sImg.outerWidth(), sImg.outerHeight(), 0, 0)).find(':last');

This fork puts an inline transparent 1x1 gif in the background so we it still works as a mousetrap but we don't get a 404

$mouseTrap = jWin.parent().append(format("<div class='mousetrap' style='background-image:url(\"%0\");z-index:999;position:absolute;width:%1px;height:%2px;left:%3px;top:%4px;\'></div>",'data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7',sImg.outerWidth(),sImg.outerHeight(),0,0)).find(':last');



In v1.0.3 uses a blank.gif - but this method still avoids an http call for a 1x1 gif

Forked from http://www.professorcloud.com/downloads/cloud-zoom.1.0.3.zip
