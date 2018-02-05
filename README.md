## jackson-exploiter
This is PoC with two different gadgets to reproduce [CVE-2018-5968](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-5968 "CVE-2018-5968") which can be used to exploit the default typing in [jackson-databind](https://github.com/FasterXML/jackson-databind/).

## Context
Jackson-databind allows developers to use default-typing to handle polymorph fields when unmarshalling the `json` to `Java Object`. When developers open this feature by calling `ObjectMapper.enableDefaultTyping()` method, it can be dangerous when the input is controlled by attackers.

Jackson-databind has a blacklist mechanism to avoid unmarshalling some dangerous classes. These classes are called gadgets. Now in this project, you will see that how can I use two different gadgets to bypass this blacklist and exploit to RCE vulnerability successfully.

MITRE assigned CVE-2018-5968 to this issue.

## Affected versions

Through 2.8.11 and 2.9.x through 2.9.3

## Mitigation
This issue was fixed in 2.9.4. So just update to the lastest version of jackson-databind to avoid potential risks.

## References
[https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-5968](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-5968)

[https://github.com/FasterXML/jackson-databind/issues/1899](https://github.com/FasterXML/jackson-databind/issues/1899)