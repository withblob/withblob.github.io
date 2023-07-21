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


```yaml
Usage:
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

![blobdns example.com output](https://user-images.githubusercontent.com/139460414/253770768-296b80c0-e35a-490c-8efb-e92fd6d2245f.png)

Built in Rust. To use it, you will need to compile it yourself (for now). Pre-built packages will come soon!

Available under MIT license

Copyright <a href="https://withblob.com">https://withblob.com</a>