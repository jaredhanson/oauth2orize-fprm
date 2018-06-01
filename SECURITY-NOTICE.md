# Security vulnerability details for oauth2orize-fprm < 0.2.1

1. [Reflected cross-site scripting](#reflected-cross-site-scripting)

## Reflected cross-site scripting

### Description

Input values utilized by `oauth2orize-fprm` were not properly encoded and, when utilized in an HTML context, could be leveraged to cause reflected cross-site scripting via HTML injection.

This may allow an adversary to obtain sensitive information which in turn may enable additional attack vectors, potentially resulting in further unauthorized information disclosure.

Due to the nature of reflected cross-site scripting, such an attack would require a potential victim to open a malicious URL crafted by the adversary.

### Mitigation

Updated packages are available on `npm`. To ensure delivery of additional bug fixes moving forward, please make sure your `package.json` file is updated to take patch and minor level updates of our libraries. See below:

```json
{
  "dependencies": {
    "oauth2orize-fprm": "^0.2.1"
  }
}
```

### Upgrade Notes

1. This fix patches the library that your application runs, but will not impact your users, their current state, or any existing sessions.

### References

1. [CVE-2018-11647](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-11647).

### Credits

- Satyam Pujari
