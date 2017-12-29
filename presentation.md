# Cross-Origin Resource Sharing

## Act I : Ajax and XSS

## Act II : Same-Origin Policy

## Act III : Work-Arounds

## Act IV : CORS

## Dénouement

---

# Act I : Ajax and XSS

- Alice is a customer of _Too Big To Fail_ (http://too-big-to-fail.com)

--

- Bob is the developer of a malicious website: http://your-secretz.com

---

1. Alice visits the online banking website, http://too-big-to-fail.com , and logs
in with her credentials.

The website sets a cookie for Alice's browser to identify her in future
requests. This cookie indicates that the request came from Alice, just as if
it contained her login credentials.

--

2. Bob sends Alice a link to his website, http://your-secretz.com

Bob is one bad dude, and really wants to control Alice's bank account.

--

3. Alice clicks the link, and the page loads malicious javascript.

This javascript tries to make Ajax requests to http://too-big-to-fail.com ,
which would already include Alice's cookie because cookies are automatically
sent with requests to the cookie's domain.

These requests are for a cash transfer to Bob's account.

---

# Second Slide

This is the second slide
