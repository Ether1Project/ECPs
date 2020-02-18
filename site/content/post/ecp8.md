---
title: ECP-8, Create a WordPress Plugin for ethoFS
date: 2020-02-18T00:00:10.000Z # Change the date and time
description: >-
  Gather resources to develop a WordPress Plugin for ethoFS
---

ECP Originator: Goose-Tech  
ECP Sponsor: Goose-Tech  
ECP Motivation: Create a new WordPress plugin & widget for ethoFS  
ECP Summary: Update node network to support SSL/TLS, add encryption/password protection, update Ether-1 wallet and ethofs.com upload tools to allow for encryption/password protection of uploaded files, create WordPress plugin to allow secure backup of existing WordPress websites  
Discussion: 18 Feb. 2020 00:01 UTC to 23 Feb. 2020 00:01 UTC  
Voting: 14 Feb. 2020 00:01 UTC to 29 Feb. 2020 00:01 UTC  

Details:

This could be an EthoLabs initiative...

I propose we focus development on tools/apps that will make uploading to ethoFS more secure and user friendly. To that end, I would like to outline some of the steps needed to accomplish the goal of allowing any WordPress user to install the ethoFS plugin to allow for easy uploading of their website (as a backup) to the ethoFS network or widget to allow webhosts to offer secure (dropbox-style) file sharing via ethoFS. (Perhaps a Chrome or Firefox browser extension could be another avenue to pursue, but keeping with the webhosting foundation of ethoFS, we can begin with WordPress.) It will also be necessary for the plugin to allow for the purchase and storage of ETHO to faciliate its use. This could be accomplished with a smart contract linked to the user's registered ethoDNS.

Here are the steps I propose we take to achieve the goal of making ethoFS widely available to all WordPress users:

1. Secure the nodes with SSL/TLS
2. Update the protocol to allow for encryption & password protection of uploaded file(s)
3. Update the Ether-1 wallet and https://ethofs.com/uploads.html to allow for encryption/password protection of uploaded file(s)
4. Develop ethoDNS to allow users to register a .etho domain on the ETHO network
5. Develop WordPress plugin to allow for backup of existing website to ethoFS
6. Develop WordPress widget to allow sites to offer secure file sharing via ethoFS
Note: The WordPress plugin & widget will have to provide an easy way to purchase ETHO

How does it all work?

First, SSL/TLS is a requirement to ensure secure sending/receiving of sensitive data. Second, password protected files on the ethoFS network will ensure that private data cannot be accessed by anyone without the password (this includes node ops). After the wallets are updated, this added security and functionality will entice users to use the network for more than just static websites.

As for ethoDNS, the goal is ease of use. It is complicated what happens behind the scenes with ethoFS, but the average user does not need to be burdened with this. Our goal should be to make it as easy as possible to upload their website to ethoFS. This would look something like the following:

1. User purchases/registers ethoDNS domain (e.g. example.etho)
A smart contract is then tied to the ETHO address they used to pay for the domain. The same smart contract is used to fund uploads to the ethoFS network.
2. User points their .com or other domain to the .etho domain via MX or CNAME record
3. User uploads their website/content to their ethoDNS domain
Behind the scenes, the Ether-1 wallet or the WordPress plugin will automatically connect the upload hash to the user's ethoDNS domain. In the case of updating or adding new content to an existing site, the Ether-1 wallet or WordPress plugin will remove the previous upload hash, refund the balance, and reissue a new upload hash for the additional/updated content.
4. The network automatically propogates the ethoDNS domain with the new upload hash
