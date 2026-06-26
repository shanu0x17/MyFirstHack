# Day 13 - COOKIES


## Key Learnings

- A cookie is a small text file a website puts on your computer to remember something about you
- The web is stateless — every page request stands alone. Cookies were invented to give it memory. They're the pass that the browser hands back to the server on every visit.
- A cookie is just a small piece of text- A name and value, An expiry date, Security flags
- A session cookie is a portable proof of who you are. Session cookies don't care who is holding them
- Security flags:
   1. Secure — tells the browser "only send this cookie over HTTPS, never over HTTP."
   2. HttpOnly — tells the browser "don't let JavaScript on the page read this cookie"
   3. SameSite — tells the browser when it's allowed to send the cookie on requests originating from other sites
   4. Expires / Max-Age — how long the cookie lives
