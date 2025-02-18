# Keygen

[![Latest Release](https://img.shields.io/github/release/charmbracelet/keygen.svg)](https://github.com/charmbracelet/keygen/releases)
[![GoDoc](https://godoc.org/github.com/golang/gddo?status.svg)](https://pkg.go.dev/github.com/charmbracelet/keygen?tab=doc)
[![Build Status](https://github.com/charmbracelet/keygen/workflows/build/badge.svg)](https://github.com/charmbracelet/keygen/actions)
[![Go ReportCard](https://goreportcard.com/badge/charmbracelet/keygen)](https://goreportcard.com/report/charmbracelet/keygen)

An SSH key pair generator with password protected keys support. Supports generating RSA, ECDSA, and Ed25519 keys.

## Example

```go
filepath := filepath.Join(".ssh",  "my_awesome_key")
passphrase := []byte("awesome_secret")
k, err := NewWithWrite(filepath, passphrase, key.Ed25519)
if err != nil {
	fmt.Printf("error creating SSH key pair: %v", err)
	os.Exit(1)
}
fmt.Printf("Your authorized key: %s\n", string(k.PublicKey()))
```

## Feedback

We’d love to hear your thoughts on this project. Feel free to drop us a note!

* [Twitter](https://twitter.com/charmcli)
* [The Fediverse](https://mastodon.social/@charmcli)
* [Discord](https://charm.sh/chat)

## License

[MIT](https://github.com/charmbracelet/keygen/raw/master/LICENSE)

***

Part of [Charm](https://charm.sh).

<a href="https://charm.sh/"><img alt="The Charm logo" src="https://stuff.charm.sh/charm-badge.jpg" width="400"></a>

Charm热爱开源 • Charm loves open source
