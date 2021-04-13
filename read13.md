# SENDING FORM DATA

![](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data/client-server.png)

An HTML form on a web page is nothing more than a convenient user-friendly way to configure an HTTP request to send data to a server. This enables the user to provide information to be delivered in the HTTP request.

```
<form action="/action_page.php" method="get">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="submit" value="Submit">
</form>
```

* The method attribute specifies how to send form-data (the form-data is sent to the page specified in the action attribute).

* The form-data can be sent as URL variables (with method="get") or as HTTP post transaction (with method="post").

## Notes on GET:


* Appends form-data into the URL in name/value pairs.

* The length of a URL is limited (about 3000 characters).

* Never use GET to send sensitive data! (will be visible in the URL).

* Useful for form submissions where a user wants to bookmark the result.

* GET is better for non-secure data, like query strings in Google.

## Notes on POST:

* Appends form-data inside the body of the HTTP request (data is not shown in URL).

* Has no size limitations.

* Form submissions with POST cannot be bookmarked.

## Summary: Form Tag attributes

* action = "/path-to-url"

* method = "GET/POST"

* name = "formName"

* autocomplete = "on/off"

* target = "_blank" (new tab) / "_self" (current tab)

* enctype = "text/plain" (text input form) "multipart/form-data" (forms containing files)