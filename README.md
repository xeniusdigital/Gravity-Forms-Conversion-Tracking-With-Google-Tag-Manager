# Gravity-Forms-Conversion-Tracking-With-Google-Tag-Manager
Gravity Forms Conversion Tracking With Google Tag Manager

Step 1 – Create a form listener tag for Gravity Forms in Google Tag Manager
The form listener tag will create an event in Google Tag Manager that is fired when the gravity form confirmation message is displayed. The event will include the formID that we insert in Step 2.

Create a custom HTML tag with the following code in Google Tag Manager:

<script type="text/javascript">
jQuery(document).ready(function() {
jQuery(document).bind("gform_confirmation_loaded", function(event, formID) {
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
event: "formSubmission",
formID: formID
});
});
});
</script>



Source: https://www.m4b.co.uk/resources/gravity-forms-conversion-tracking-with-tag-manager/


