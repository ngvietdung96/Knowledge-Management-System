Tags: #SecondBrain 
Status: #open, #unprocessed
Related: 

---

# Overview

**Transport Layer Security** (**TLS**) is a [cryptographic protocol](https://en.wikipedia.org/wiki/Cryptographic_protocol "Cryptographic protocol") designed to provide communications security over a computer network, such as the [Internet](https://en.wikipedia.org/wiki/Internet "Internet"). The [protocol](https://en.wikipedia.org/wiki/Communication_protocol "Communication protocol") is widely used in [applications](https://en.wikipedia.org/wiki/Application_software "Application software") such as [email](https://en.wikipedia.org/wiki/Email "Email"), [instant messaging](https://en.wikipedia.org/wiki/Instant_messaging "Instant messaging"), and [voice over IP](https://en.wikipedia.org/wiki/Voice_over_IP "Voice over IP"), but its use in securing [HTTPS](https://en.wikipedia.org/wiki/HTTPS "HTTPS") remains the most publicly visible.

The TLS protocol aims primarily to provide security, including [privacy](https://en.wikipedia.org/wiki/Privacy "Privacy") (confidentiality), integrity, and authenticity through the use of [cryptography](https://en.wikipedia.org/wiki/Cryptography "Cryptography"), such as the use of [certificates](https://en.wikipedia.org/wiki/Public_key_certificate "Public key certificate"), between two or more communicating computer applications. It runs in the [presentation layer](https://en.wikipedia.org/wiki/Presentation_layer "Presentation layer") and is itself composed of two layers: the TLS record and the TLS [handshake protocols](https://en.wikipedia.org/wiki/Handshake_\(computing\) "Handshake (computing)").

# History and development

Netscape developed the original SSL protocols. SSL version 1.0 was never publicly released because of serious security flaws in the protocol.

SSL 2.0 was deprecated in 2011 by [RFC 6176](https://www.rfc-editor.org/rfc/rfc6176). In 2014, SSL 3.0 was found to be vulnerable to the [POODLE](https://en.wikipedia.org/wiki/POODLE "POODLE") attack that affects all [block ciphers](https://en.wikipedia.org/wiki/Block_cipher "Block cipher") in SSL; [RC4](https://en.wikipedia.org/wiki/RC4 "RC4"), the only non-block cipher supported by SSL 3.0, is also feasibly broken as used in SSL 3.0. SSL 3.0 was deprecated in June 2015 by [RFC 7568](https://www.rfc-editor.org/rfc/rfc7568).

TLS 1.0 was first defined in [RFC 2246](https://www.rfc-editor.org/rfc/rfc2246) in January 1999 as an upgrade of SSL Version 3.0, and written by Christopher Allen and Tim Dierks of Certicom.
> [!quote]
> The Netscape/Microsoft browser wars in the mid-90's were really vicious and competitive. As a part of the cutthroat competition, Microsoft decided to revise the SSL 2 protocol with some additions of their own, and specified a protocol called "PCT" that was derived from SSL 2. It was only supported in IE and IIS.
> We negotiated a deal where Microsoft and Netscape would both support the IETF taking over the protocol and standardizing it in an open process, which led to me editing the RFC. 
> TLS 1.0 was born (which was really SSL 3.1)
> "[Tim Dierks](https://tim.dierks.org/2014/05/)"

TLS 1.2 was defined in [RFC 5246](https://www.rfc-editor.org/rfc/rfc5246) in August 2008.
TLS 1.3 was defined in [RFC 8446](https://www.rfc-editor.org/rfc/rfc8446) in August 2018.

| Protocol | Published   | Status             |
| -------- | ----------- | ------------------ |
| SSL 1.0  | Unpublished | Unpublished        |
| SSL 2.0  | 1995        | Deprecated in 2011 |
| SSL 3.0  | 1996        | Deprecated in 2015 |
| TLS 1.0  | 1999        | Deprecated in 2021 |
| TLS 1.1  | 2006        | Deprecated in 2021 |
| TLS 1.2  | 2008        | In use since 2008  |
| TLS 1.3  | 2018        | In use since 2018  |


Example:
https://www.cloudflare.com/learning/ssl/transport-layer-security-tls/
https://www.cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake/

https://aws.amazon.com/what-is/ssl-certificate/




---
# References
Official website:
Wikipedia: https://en.wikipedia.org/wiki/Transport_Layer_Security
Youtube: