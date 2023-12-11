$(function () {
	// iframe + touch device
	var is_touch_device = 'ontouchstart' in document.documentElement;
	if (window != window.top && is_touch_device) {
		$(document).ready(function () {
			var available_height = $("#mailpreviewframe", top.document).height();
			var $body = $("body");
			
			$body.children().wrapAll("<div id=\"iframescrollfixcontainer\">");
			
			$("div.message-part pre, div.message-htmlpart pre, div.message-part div.pre").css("font-size", "12pt", "important");
			
			var $iframescrollfixcontainer = $("#iframescrollfixcontainer");
			
			$iframescrollfixcontainer.css({
				"height" : available_height + 'px',
				"overflow" : "auto",
				"-webkit-overflow-scrolling" : "touch"
			});
			
			$(window.top).resize(function () {
				available_height = $("#mailpreviewframe", top.document).height();
				
				$iframescrollfixcontainer.css({
					"height" : available_height + 'px'
				});
			});
		});
	}
	// touch device parent frame
	else if (is_touch_device) {
		$(".minwidth").css("min-height", "600px");
	}
});