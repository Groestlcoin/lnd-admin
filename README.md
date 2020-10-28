# LND Admin

Admin web interface for [LND](https://github.com/groestlcoin/lnd), via gRPC. Built with Node.js, express, bootstrap-v4.

Live demo: https://lnd-admin.groestlcoin.org

# Features

* UI for connecting to LND - requires host/port/admin.macaroon/tls.cert, which can be supplied in various ways, including using LND Connect strings
* Browse and search the public lightning network
* View invoices, payments, and forwarded payments
* Create and pay invoices
* Open and close channels
* Connect to multiple LND nodes and switch between them
* Simple/intuitive sorting filtering for most data
* Tools for sign/very, query route, generate LND Connect strings
* Star (favorite) nodes and channels
* Responsive design (but UI is data/table heavy, so works best on large screens)


# Getting started

### 1. Install/Run LND

* [Install LND](https://github.com/groestlcoin/lnd/blob/master/docs/INSTALL.md)

### 2. Install LND Admin (from source)

* `git clone git@github.com:groestlcoin/lnd-admin.git`
* `cd lnd-admin; npm install`
* `npm start`
* Open [http://127.0.0.1:3004/](http://127.0.0.1:3004/)

### 3. Setup LND Admin via UI

Once started, LND Admin's UI will guide you to set an admin password and then to connect to any LND nodes you're running. Your hashed password and your LND credentials (encrypted with your password), will be stored in the file `~/.lnd-admin/credentials.json`. If you restart the app after setup, you'll need to "unlock" with your same admin password (in order to decrypt LND credentials). Deleting this file at any time and restarting will prompt you to go through the setup process again.
