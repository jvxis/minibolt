# Node Status Install Instructions

## Initial Setup
1. Dependencies:
   Flask Library
   pip3 install flask
2. Get the files node-status.py and status.html
3. Place node-status.py in your user directory `/home/user/`
4. Make a directory `templates`
   ```bash
   sudo mkdir templates
   ```
5. Move the file status.html to the directory `/home/user/templates`

6. Open the file node-status.py and fill out with your Bitcoind credentials

   BITCOIN_RPC_USER = 'YOUR_BITCOIN_RPCUSER'
   BITCOIN_RPC_PASSWORD = 'YOUR_BITCOIN_RPCPASS'
   BITCOIN_RPC_HOST = 'YOUR_BITCOIN_MACHINE_IP'
   BITCOIN_RPC_PORT = '8332'

7. Save and Exit

8. Execute:
   ```bash
   python3 node-status.html
   ```
   
   
