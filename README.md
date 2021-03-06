Hello, students, let's get started with oauth.

First, go ahead and clone my github demo, found here: [https://github.com/AnnaBNana/oauth_demo](https://github.com/AnnaBNana/oauth_demo)

I'm using some libraries here, json and Flask-OAuth.  No need to pip install json, but you will need to run:

$ pip install Flask-OAuth

I'm protecting my keys in a pretty hacky way.  The better way would be to set some environmental variables (google it).  But for the sake of simplicity and demonstration, we will hard code out variables into a separate file in our root directory, and then import that file.  My signing.py file looks like this:

```
def consumer_key():
    return 'put your secret key here'
def consumer_secret():
    return 'put your consumer key here'
def access_key():
    return 'put your access token here'
def access_secret():
    return 'put your access token secret here'
```

how do I get these keys, you ask?  by visiting [https://apps.twitter.com/](https://apps.twitter.com/) and getting yourself an consumer key and secret key.  record these somewhere secure.  twitter will ask for your name, app name, and url.  The url can be a placeholder, but needs to be formatted like a valid url.  Mine, for example, is www.placeholder.com.  Once you've done this, navigate to application management, click on keys and access tokens, and generate an access key.  this will give you two values, your access key and your access secret.

Don't forget to add signing.py to your .gitignore file!

Now, if you need to do login and registration, versus just retrieving some tweets from a users account, that's a bit more involved.  You'll have to request the access keys for each user that signs in and then store those access keys.  In addition, you'll have to periodically check to make sure the user's access keys haven't changed (because they will).  For more details, check out the documentation of your chosen API's (most have great docs, they want you to use it). Also check out the docs for json encoder, which I used here:

[https://docs.python.org/2/library/json.html](https://docs.python.org/2/library/json.html)

and for python-oauth2, also used here:

[https://github.com/joestump/python-oauth2](https://docs.python.org/2/library/json.html)

and some helpful examples from their wiki:

[https://github.com/joestump/python-oauth2/wiki/Signing-A-Request](https://github.com/joestump/python-oauth2/wiki/Signing-A-Request)

hopefully these tips will get you well on your way.  I'll be around tomorrow to answer any and all questions, and to explain what is involved in the login process, as needed.  Good luck!

and then [this](http://starecat.com/content/wp-content/uploads/i-figured-out-how-to-turn-on-my-microwave-using-python.jpg)

cheers!  have fun!
