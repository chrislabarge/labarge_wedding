+++
title = "RSVP"
weight = 60
draft = true
+++
<img class="" style='width:100%; border-radius: 6px;' src="/images/personal.jpg" aria-hidden="true">
<form id="contactform" method="post" action="https://formspree.io/labargeintraining@gmail.com">
	<div class="field">
		<input type="text" name="name" id="name" placeholder="Name of Attendees (First & Last)"/>
	</div>
	<div class="field">
		<input type="email" id="email" name="email" placeholder="Email">
	</div>
	<div class="field">
		<textarea name="message" id="message" rows="4" placeholder="Message (Optional)"></textarea>
	</div>
	<ul class="actions">
		<li><input type="submit" value="Send RSVP" class="special" /></li>
		<li><input type="reset" value="Reset" /></li>
	</ul>
	<input type="hidden" name="_next" value="?sent#formspree" />
	<input type="hidden" name="_subject" value="Subject for your mail like new message" />
	<input type="text" name="_gotcha" style="display:none" />
</form>
<span id="contactformsent">Thank you for your sending your RSVP.  We cannot wait to see you at the wedding!</span>

<script>
$(document).ready(function($) {
    $(function(){
        if (window.location.search == "?sent") {
            $('#contactform').hide();
        	$('#contactformsent').show();
        } else {
        	$('#contactformsent').hide();
        }
    });
});
</script>
