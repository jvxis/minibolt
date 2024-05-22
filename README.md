# Light Minibolt
## For installations with Bitcoin Core on another machine

Guys, I made a light version of minibolt here, without bitcoind. Just with the setup configurations, tor, i2p, and lnd. In this case, I used LND via git pull and compiled it to ensure the latest available version 0.18.0 rc2.

[Disk Image Download](https://1drv.ms/u/s!AuOr1MO73leJi5RS3MFUBo7HP_xutg?e=SExAEJ)

Use: User: `admin` Pass: `lightning` to login and then change password using `passwd`

Change your hostname:
```sudo nano /etc/hostname```

The lnd.conf is complete and commented, for now in tor only, but clearnet configuration is commented.
You need to point in lnd.conf to your bitcoin core.

`sudo nano /data/lnd/lnd.conf`

Change your node alias (name)
`alias=YOURNODENAME`

Change this part to your bitcoind credentials

`# External Bitcoin Node - Please change to your bitcoin node IP, and your RPCUSER and RPCPASS`

`bitcoind.rpchost=192.168.68.74:8332`

`bitcoind.rpcuser=jvxminibolt`

`bitcoind.rpcpass=Suc31709801%%`

`bitcoind.zmqpubrawblock=tcp://192.168.68.74:28332`

`bitcoind.zmqpubrawtx=tcp://192.168.68.74:28333`


Type `journalctl -f -u lnd`
you should see:

May 21 23:09:38 jvx-minibolt-tmp lnd[812]: 2024-05-21 23:09:38.318 [INF] LTND: Waiting for wallet encryption password. Use `lncli create` to create a wallet, `lncli unlock` to unlock an existing wallet, or lncli changepassword` to change the password of an existing wallet and unlock it.
May 21 23:09:38 jvx-minibolt-tmp systemd[1]: Started lnd.service - Lightning Network Daemon.

It has active services and is right at the point where it asks to create the wallet password. From this step:

So Follow this step to create your wallet
https://v2.minibolt.info/lightning/lightning/lightning-client#wallet-setup

Use RUFUS to create a bootable Flash Drive
https://github.com/pbatard/rufus/releases/download/v4.4/rufus-4.4.exe
