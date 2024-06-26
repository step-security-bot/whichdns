# whichdns
When you do a DNS request, which DNS server is used? This tool will tell you.
It does a DNS request while doing a packet capture and gets the DNS server that replied.

Warning: Requires root access since it does a packet capture while doing the dns requests.


## Usage/Examples

### get DNS server
```bash
sudo ./whichdns
```

### Reutrn only the DNS server for use in scripts
```bash
sudo ./whichdns --iponly
```

## How To build
Needs pcap to build

### Fedora
```bash
dnf install libpcap-devel
```

### Debian
```bash
apt install libpcap-dev
```

### Build
```bash
CGO_ENABLED=1 go build
```

## Example output
```bash
Default interface: wlp4s0
2024/03/11 22:16:18 Making DNS requests
2024/03/11 22:16:18 DNS request made.
2024/03/11 22:16:18 DNS response from: 192.168.178.21
```

## Dependancies & Documentation
[![Go Mod](https://img.shields.io/github/go-mod/go-version/earentir/whichdns)]()

[![Dependancies](https://img.shields.io/librariesio/github/earentir/whichdns)](https://libraries.io/github/earentir/whichdns)

[![OpenSSF Best Practices](https://www.bestpractices.dev/projects/8653/badge)](https://www.bestpractices.dev/projects/8653)

[![OpenSSF Scorecard](https://api.securityscorecards.dev/projects/github.com/earentir/whichdns/badge)](https://securityscorecards.dev/viewer/?uri=github.com/earentir/whichdns)


## Contributing

Contributions are always welcome!
All contributions are required to follow the https://google.github.io/styleguide/go/

## Vulnerability Reporting

Please report any security vulnerabilities to the project using issues or directly to the owner.

## Code of Conduct

 This project follows the go project code of conduct, please refer to https://go.dev/conduct for more details

## Roadmap

- add options to return just the dns server for use in scripts

## Authors

- [@earentir](https://www.github.com/earentir)


## License

I will always follow the Linux Kernel License as primary, if you require any other OPEN license please let me know and I will try to accomodate it.

[![License](https://img.shields.io/github/license/earentir/gitearelease)](https://opensource.org/license/gpl-2-0)
