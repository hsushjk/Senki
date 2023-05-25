# Development Guide

### Compile Documentation <a href="#compile-documentation" id="compile-documentation"></a>

Xray supports multiple platforms, and you can perform cross-compilation on various platforms by yourself.

Please click Compile Documentation to view specific compile-related content.

### Design Concept <a href="#design-concept" id="design-concept"></a>

Xray kernel provides a platform for secondary development.

This section explains the design goals and architecture of Xray.

Please click Design Principles to learn about the design goals and architecture of Xray.

### Development Standards <a href="#development-standards" id="development-standards"></a>

This section outlines the guidelines to follow when obtaining code, developing, submitting PRs, as well as the relevant coding standards.

Please click Development Specification to view the guidelines that should be followed during Xray development.

### Protocol Details <a href="#protocol-details" id="protocol-details"></a>

Xray uses many protocols, and you can obtain a detailed description of each protocol through various means.

#### VLESS Protocol <a href="#vless-protocol" id="vless-protocol"></a>

VLESS is a stateless lightweight transport protocol that can serve as a bridge between Xray clients and servers.

#### VMess Protocol <a href="#vmess-protocol" id="vmess-protocol"></a>

VMess is an encrypted transport protocol that can act as a bridge between Xray clients and servers.

#### Mux.Cool Protocol <a href="#mux-cool-protocol" id="mux-cool-protocol"></a>

Mux.Cool protocol is a multiplexing transport protocol used to transmit multiple independent data streams within an established data stream.

#### mKCP Protocol <a href="#mkcp-protocol" id="mkcp-protocol"></a>

mKCP is a stream transmission protocol modified from the [KCP protocolopen in new window](https://github.com/skywind3000/kcp) that can transmit arbitrary data streams in order.
