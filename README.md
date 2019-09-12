# Dark Slack

** NOTE: This theme does not work in Slack.app v 4.0.0 and above. Watch this space for an updated theme that is v4 compatible! **

** UPDATE: On 9/12/2019 Slack released offical dark mode support! As such, I am stopping development of this project. Thank you to anyone who found this useful! **

* This is a dark theme for Slack that can be customized to the user's content.
* Inspired by this thread: https://gist.github.com/DrewML/0acd2e389492e7d9d6be63386d75dd99#gistcomment-1991368

1. Close Slack
2. Open this file
```/Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static/ssb-interop.js```
3. Append this to it
```
document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/knlandes/dark-slack/master/resources/drk_theme.css',
   success: function(css) {
     $("<style></style>").appendTo('body').html(css);
   }
 });
});
```
4. Save the file.
5. Open Slack and enjoy the darkness!
