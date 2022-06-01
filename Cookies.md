# Cookies
a cookie is a small text file that is stored by a browser on the user’s machine. Cookies are plain text; they contain no executable code. A web page or server instructs a browser to store this information and then send it back with each subsequent request based on a set of rules. Web servers can then use this information to identify individual users. Most sites requiring a login will typically set a cookie once your credentials have been verified, and you are then free to navigate to all parts of the site so long as that cookie is present and validated. Once again, the cookie just contains data and isn’t harmful in and of itself.

### Using
Cookies are mainly used for three purposes:
1. Session management<br>
Logins, shopping carts, game scores, or anything else the server should remember.

2. Personalization<br>
User preferences, themes, and other settings.

3. Tracking<br>
Recording and analyzing user behavior.


### Automatic cookie removal
There are a few reasons why a cookie might be automatically removed by the browser:
1. Session cookies are removed when the session is over (browser is closed).
2. Persistent cookies are removed when the expiration date and time have been reached.
3. If the browser’s cookie limit is reached, then cookies will be removed to make room for the most recently created cookie.

Cookies that are used for sensitive information (such as indicating authentication) should have a short lifetime.

### Atributies
- A cookie with the Secure attribute is only sent to the server with an encrypted request over the HTTPS protocol. It's never sent with unsecured HTTP (except on localhost), which means man-in-the-middle attackers can't access it easily.

- A cookie with the HttpOnly attribute is inaccessible to the JavaScript Document.cookie API; it's only sent to the server.

- The Domain attribute specifies which hosts can receive a cookie. If unspecified, the attribute defaults to the same host that set the cookie, excluding subdomains. If Domain is specified, then subdomains are always included.

- The Path attribute indicates a URL path that must exist in the requested URL in order to send the Cookie header.

### Summary
Thanks to cookies, you can save information about the visitor and retrieve it again on subsequent requests. This is a very important technique, used in a wide range of situations, like keeping the user logged in, tracking their use of your website and much more.

#### Ref: [HTTP Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies), [HTTP Cookies Explained](https://humanwhocodes.com/blog/2009/05/05/http-cookies-explained/) and [.NET Cookies Simplified](https://asp.mvc-tutorial.com/httpcontext/cookies/).