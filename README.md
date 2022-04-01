# Roman Numeral HTTP Status Codes

Why should the Romans not enjoy the web, just because they are all dead?

This project includes a simple webserver, fork from [nolibc-httpd](https://github.com/Francesco149/nolibc-httpd)
with the status code replaced with the corresponding roman numeral.

To make sure we still adhere to the HTTP spec, we use the `0r` prefix for the status code.
Thanks [@ylebre](https://github.com/ylebre) for this suggestion!

## Install

Clone the repo and build the server:

```bash
git clone https://github.com/potherca-blog/roman-numeral-http-status-codes.git
cd roman-numeral-http-status-codes && ./build.sh 
```

## Usage

Start the server:

```sh
./httpd index.html
```

Visit the page: [http://localhost:MMXXII](http://localhost:2022) and, as you can see, the response is "OK".

![image](https://user-images.githubusercontent.com/195757/161277345-872b62ba-e497-43b3-8c10-149d741a150f.png)

Sadly the browser does not show Roman Numerals, but the status is there!

Use `curl` to see it:

```sh
$ curl --include http://localhost:MMXXII
HTTP/1.1 0rCC OK

<!doctype>
<title>hello world!</title>
<h1>hello world!</h1>
```

To see a "Not Found" response, start the server with a non-existent file:

```sh
./httpd whatever.html
```

```sh
curl --include http://localhost:MMXXII 
HTTP/1.1 0rCDIV Not Found
```

## List of Roman Numeral HTTP Status Codes

| Use      | Instead of | For                                        |
|----------|-----------:|--------------------------------------------|
| C        |        100 | Continue                                   |
| CI       |        101 | Switching Protocols                        |
| CII      |        102 | Processing (WebDAV; RFC 2518)              |
| CIII     |        103 | Early Hints (RFC 8297)                     |
| CX       |        110 | Response is Stale                          |
| CXI      |        111 | Revalidation Failed                        |
| CXII     |        112 | Disconnected Operation                     |
| CXIII    |        113 | Heuristic Expiration                       |
| CXCVIV   |        199 | Miscellaneous Warning                      |
| CC       |        200 | OK                                         |
| CCI      |        201 | Created                                    |
| CCII     |        202 | Accepted                                   |
| CCIII    |        203 | Non-Authoritative Information              |
| CCIV     |        204 | No Content                                 |
| CCV      |        205 | Reset Content                              |
| CCVI     |        206 | Partial Content (RFC 7233)                 |
| CCVII    |        207 | Multi-Status (WebDAV; RFC 4918)            |
| CCVIII   |        208 | Already Reported (WebDAV; RFC 5842)        |
| CCXIV    |        214 | Transformation Applied                     |
| CCXXVI   |        226 | IM Used (RFC 3229)                         |
| CCXCVIV  |        299 | Miscellaneous Persistent Warning           |
| CCC      |        300 | Multiple Choices                           |
| CCCI     |        301 | Moved Permanently                          |
| CCCII    |        302 | Found (Previously "Moved temporarily")     |
| CCCIII   |        303 | See Other (since HTTP/1.1)                 |
| CCCIV    |        304 | Not Modified (RFC 7232)                    |
| CCCV     |        305 | Use Proxy (since HTTP/1.1)                 |
| CCCVI    |        306 | Switch Proxy                               |
| CCCVII   |        307 | Temporary Redirect (since HTTP/1.1)        |
| CCCVIII  |        308 | Permanent Redirect (RFC 7538)              |
| CD       |        400 | Bad Request                                |
| CDI      |        401 | Unauthorized (RFC 7235)                    |
| CDII     |        402 | Payment Required                           |
| CDIII    |        403 | Forbidden                                  |
| CDIV     |        404 | Not Found                                  |
| CDV      |        405 | Method Not Allowed                         |
| CDVI     |        406 | Not Acceptable                             |
| CDVII    |        407 | Proxy Authentication Required (RFC 7235)   |
| CDVIII   |        408 | Request Timeout                            |
| CDVIV    |        409 | Conflict                                   |
| CDX      |        410 | Gone                                       |
| CDXI     |        411 | Length Required                            |
| CDXII    |        412 | Precondition Failed (RFC 7232)             |
| CDXIII   |        413 | Payload Too Large (RFC 7231)               |
| CDXIV    |        414 | URI Too Long (RFC 7231)                    |
| CDXV     |        415 | Unsupported Media Type (RFC 7231)          |
| CDXVI    |        416 | Range Not Satisfiable (RFC 7233)           |
| CDXVII   |        417 | Expectation Failed                         |
| CDXVIII  |        418 | I'm a teapot (RFC 2324, RFC 7168)          |
| CDXVIV   |        419 | Page Expired (Laravel Framework)           |
| CDXX     |        420 | Enhance Your Calm (Twitter)                |
| CDXX     |        420 | Method Failure (Spring Framework)          |
| CDXXI    |        421 | Misdirected Request (RFC 7540)             |
| CDXXII   |        422 | Unprocessable Entity (WebDAV; RFC 4918)    |
| CDXXIII  |        423 | Locked (WebDAV; RFC 4918)                  |
| CDXXIV   |        424 | Failed Dependency (WebDAV; RFC 4918)       |
| CDXXV    |        425 | Too Early (RFC 8470)                       |
| CDXXVI   |        426 | Upgrade Required                           |
| CDXXVIII |        428 | Precondition Required (RFC 6585)           |
| CDXXVIV  |        429 | Too Many Requests (RFC 6585)               |
| CDXXX    |        430 | Request Header Fields Too Large (Shopify)  |
| CDXXXI   |        431 | Request Header Fields Too Large (RFC 6585) |
| CDXL     |        440 | Login Time-out                             |
| CDXLIV   |        444 | No Response                                |
| CDXLVIV  |        449 | Retry With                                 |
| CDL      |        450 | Blocked by Windows Parental Controls       |
| CDLI     |        451 | Redirect                                   |
| CDLI     |        451 | Unavailable For Legal Reasons (RFC 7725)   |
| CDLX     |        460 | 460                                        |
| CDLXIII  |        463 | 463                                        |
| CDXCIV   |        494 | Request header too large                   |
| CDXCV    |        495 | SSL Certificate Error                      |
| CDXCVI   |        496 | SSL Certificate Required                   |
| CDXCVII  |        497 | HTTP Request Sent to HTTPS Port            |
| CDXCVIII |        498 | Invalid Token (Esri)                       |
| CDXCVIV  |        499 | Client Closed Request                      |
| CDXCVIV  |        499 | Token Required (Esri)                      |
| D        |        500 | Internal Server Error                      |
| DI       |        501 | Not Implemented                            |
| DII      |        502 | Bad Gateway                                |
| DIII     |        503 | Service Unavailable                        |
| DIV      |        504 | Gateway Timeout                            |
| DV       |        505 | HTTP Version Not Supported                 |
| DVI      |        506 | Variant Also Negotiates (RFC 2295)         |
| DVII     |        507 | Insufficient Storage (WebDAV; RFC 4918)    |
| DVIII    |        508 | Loop Detected (WebDAV; RFC 5842)           |
| DVIV     |        509 | Bandwidth Limit Exceeded                   |
| DX       |        510 | Not Extended (RFC 2774)                    |
| DXI      |        511 | Network Authentication Required (RFC 6585) |
| DXX      |        520 | Web Server Returned an Unknown Error       |
| DXXI     |        521 | Web Server Is Down                         |
| DXXII    |        522 | Connection Timed Out                       |
| DXXIII   |        523 | Origin Is Unreachable                      |
| DXXIV    |        524 | A Timeout Occurred                         |
| DXXV     |        525 | SSL Handshake Failed                       |
| DXXVI    |        526 | Invalid SSL Certificate                    |
| DXXVII   |        527 | Railgun Error                              |
| DXXVIV   |        529 | Site is overloaded                         |
| DXXX     |        530 | 530                                        |
| DXXX     |        530 | Site is frozen                             |
| DLXI     |        561 | Unauthorized                               |
| DXCVIII  |        598 | Network read timeout error                 |
| DXCVIV   |        599 | Network Connect Timeout Error              |

## Contribute

All feedback and contributions are welcome.


## License

Created by @Potherca under the [April Fools' Public License](LICENSE).
