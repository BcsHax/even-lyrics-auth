# even-lyrics-auth

The Spotify OAuth landing page for [even-lyrics](https://github.com/BcsHax), a
lyrics display for Even Realities G2 smart glasses.

It is one static HTML file. Spotify redirects here after you approve access; the
page reads the `code` from the query string and shows it so you can paste it back
into the Lyrics app on your phone.

**It cannot complete the sign-in itself, by design.** The app uses PKCE, and the
code verifier never leaves the phone — so this page has no way to exchange the
code even in principle. That is the security property, not a limitation.

Nothing is sent anywhere. There is no script beyond reading the query string, and
no network request of any kind.
