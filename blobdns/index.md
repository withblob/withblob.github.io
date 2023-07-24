---
layout: default
title: "Blob DNS CLI"
nav_order: 1
---
<span style="font-size: 300%; color:#89CFF0;">🌐</span>

# Blob DNS — global DNS checking CLI app

### Like `dig` or `dog` but checks DNS records in three regions:

* USA (Ohio)
* Germany (Frankfurt)
* Singapore

Unlike other similar tools that connect to remote nameservers, `blobdns` actually runs the DNS queries globally by utilizing Blob's distributed DNS checking API.

This approach will actually test the DNS record propagation from the perspective of real users, located in those countries.

In other words, it can be useful to see how your DNS records propagate blobally ;)

## Usage:

```md
  blobdns <arguments> [options]

Examples:
  blobdns example.com
  blobdns example.com A
  blobdns foo.example.com bar.example.com CNAME

  # Get AAAA record from 1.1.1.1 Cloudflare server
  blobdns example.com AAAA @1.1.1.1  

Arguments:
  <arguments> domains, records

Options:
  -v, --version Print version information
  -h, --help Print list of options
```

## Example output

### `$ blobdns example.com`
<br/>

![blobdns example.com output](https://user-images.githubusercontent.com/139460414/255538187-8bf6e40d-ccfa-4e08-a82f-e934c66bd2e3.png)

Built in Rust. To use it, please download available packages from the [releases](https://github.com/withblob/dns/releases) page.
You can also compile it from source, see GitHub readme for details.

### 💚 Contributions and feature requests are welcome!

Available under MIT license.

Copyright <a href="https://withblob.com">https://withblob.com</a>