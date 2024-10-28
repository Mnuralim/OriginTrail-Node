
# OriginTrail Node Incentive

For detailed information, visit: [OriginTrail Setup Guide](https://docs.origintrail.io/dkg-v8-upcoming-version/run-a-v8-core-node-on-testnet/preparation-for-v8-dkg-core-node-deployment) 

Tutorial Video: [YouTube](www.youtube.com)

## Minimum Requirements (VPS)
- 4GB RAM
- 4GB RAM
- 50GB HDD space

## Step 1: Prepare your ethereum wallet(base sepolia chain) and get faucet from discord
1. get base sepolia eth faucet [here](https://docs.base.org/docs/tools/network-faucets/)
2. get Base Sepolia TRAC faucet [here](https://discord.gg/Y5Sar6Ex)
```bash
!fundme_v8_base_sepolia_trac <wallet_address>
```
Example:
```bash
!fundme_v8_base_sepolia_trac 0x9b17032749aa066a2DeA40b746AA6aa09CdE67d9
```
3. set Base Sepolia RPC endpoint [here](https://docs.base.org/docs/network-information/#base-mainnet)

## Step 2: Configure firewall on the server
```bash
sudo ufw allow 9999 && sudo ufw allow 8900 && sudo ufw allow 9000 && sudo ufw reload
sudo iptables -A INPUT -p tcp --dport 9999 -j ACCEPT && sudo iptables -A INPUT -p tcp --dport 8900 -j ACCEPT && sudo iptables -A INPUT -p tcp --dport 9000 -j ACCEPT
```

## Step 3: Download OriginTrail V8 DKG Core node installer
```bash
cd /root/ && curl -k -o v8_installer.sh https://raw.githubusercontent.com/OriginTrail/ot-node/v8/develop/installer/v8_installer.sh && chmod +x v8_installer.sh
```

## Step 4: Execute the installer by running
```bash
./v8_installer.sh
```

![Deskripsi Gambar](photo_6100143317980398604_y.jfif)

**DONE**

Useful commands:
Starting your node: 
```bash
otnode-start
```
or
```bash
systemctl start otnode
```

Stopping the node: 
```bash
otnode-stop
```
or
```bash
systemctl stop otnode
```

Restarting the node: otnode-restart  or systemctl restart otnode
```bash
otnode-restart
```
or
```bash
systemctl restart otnode
```

Showing node logs: 
```bash
otnode-logs
```
or
```bash
or journalctl -u otnode --output cat -fn 100
```

Opening the node config: 
```bash
otnode-config
```
or
```bash
or nano /root/ot-node/.origintrail_noderc
```


By:
GitHub: https://github.com/Mnuralim

YouTube: https://www.youtube.com/@IzzyTSN

Twitter: `@Izzycracker04`

Telegram: `@fitriay19`

