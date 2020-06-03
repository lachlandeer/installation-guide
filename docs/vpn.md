# VPN 

!!! warning
    This section currently describes what one needs to do to set up a VPN connection to connect to the Uni Zurich System.

## Install anyconnect

To use the Uni Zurich VPN we need to install anyconnect from the command line.

Install as follows (and get the dependencies along the way):

```{bash}
 sudo apt-get install network-manager-openconnect
 sudo apt-get install network-manager-openconnect-gnome
```

## Verify anyconnect Install

```{bash}
anyconnect --version
```

which yields something like:

```{out}
OpenConnect version v8.02-1build1
Using GnuTLS. Features present: TPMv2, PKCS#11, RSA software token, HOTP software token, TOTP software token, Yubikey OATH, System keys, DTLS, ESP
Supported protocols: anyconnect (default), nc, gp

```

## Configuring VPN Access

The process was:

* Go to Settings -> Network and click `+` to add a new VPN.
* Select Cisco AnyConnect Compatible VPN.
* Enter a useful name
* For the gateway enter `uzhvpn1.uzh.ch`
* Save it

## Connecting to the VPN

From the Network menu select the new VPN network and enter your UZH shortname and password.
