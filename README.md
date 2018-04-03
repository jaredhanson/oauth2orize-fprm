# oauth2orize-fprm

[OAuth2orize](https://github.com/jaredhanson/oauth2orize) response mode plugin
providing support for [Form Post Response Mode](https://openid.net/specs/oauth-v2-form-post-response-mode-1_0.html).

This response mode uses the HTTP POST method instead of a redirect URI to return
authorization responses from the authorization server.

Status:
[![Version](https://img.shields.io/npm/v/oauth2orize-fprm.svg?label=version)](https://www.npmjs.com/package/oauth2orize-fprm)
[![Build](https://img.shields.io/travis/jaredhanson/oauth2orize-fprm.svg)](https://travis-ci.org/jaredhanson/oauth2orize-fprm)
[![Quality](https://img.shields.io/codeclimate/github/jaredhanson/oauth2orize-fprm.svg?label=quality)](https://codeclimate.com/github/jaredhanson/oauth2orize-fprm)
[![Coverage](https://img.shields.io/coveralls/jaredhanson/oauth2orize-fprm.svg)](https://coveralls.io/r/jaredhanson/oauth2orize-fprm)
[![Dependencies](https://img.shields.io/david/jaredhanson/oauth2orize-fprm.svg)](https://david-dm.org/jaredhanson/oauth2orize-fprm)


## Sponsorship

OAuth2orize is open source software.  Ongoing development is made possible by
generous contributions from [individuals and corporations](https://github.com/jaredhanson/oauth2orize/blob/master/SPONSORS.md).
To learn more about how you can help keep this project financially sustainable,
please visit Jared Hanson's page on [Patreon](https://www.patreon.com/jaredhanson).

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

Copyright (c) 2015-2018 Jared Hanson <[http://jaredhanson.net/](http://jaredhanson.net/)>

