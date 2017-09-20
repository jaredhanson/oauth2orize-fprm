# oauth2orize-fprm

[OAuth2orize](https://github.com/jaredhanson/oauth2orize) response mode plugin
providing support for [Form Post Response Mode](https://openid.net/specs/oauth-v2-form-post-response-mode-1_0.html).

This response mode uses the HTTP POST method instead of a redirect URI to return
authorization responses from the authorization server.

## Install

```bash
$ npm install oauth2orize-fprm
```

## Usage

#### Add Response Mode

For each grant in which form post response mode is desired, add support by
passing a `modes` option containing form post response mode.  For example,
using the token grant:

```js
server.grant({ 
  modes: {
    form_post: require('oauth2orize-fprm')
  } }, 
  oauth2orize.grant.token(function(client, user, ares, done) {
    // TODO: issue token
  })
);
```

## License

[The MIT License](http://opensource.org/licenses/MIT)

Copyright (c) 2015-2017 Jared Hanson <[http://jaredhanson.net/](http://jaredhanson.net/)>

<a target='_blank' rel='nofollow' href='https://app.codesponsor.io/link/vK9dyjRnnWsMzzJTQ57fRJpH/jaredhanson/oauth2orize-fprm'>  <img alt='Sponsor' width='888' height='68' src='https://app.codesponsor.io/embed/vK9dyjRnnWsMzzJTQ57fRJpH/jaredhanson/oauth2orize-fprm.svg' /></a>
