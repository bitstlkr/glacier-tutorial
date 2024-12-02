# Tutorial Glacier Verifier Node

Install Requirements packages
```
sudo apt install wget screen
```

Create new folder called "glacier-node"
```
mkdir glacier-node
```

And enter that folder with
```
cd glacier-node
```

Download the binary node & config file
```
wget https://github.com/Glacier-Labs/node-bootstrap/releases/download/v0.0.3-beta/verifier_linux_amd64
```
```
wget https://glacier-labs.github.io/node-bootstrap/config.yaml
```

Change permission of binary node
```
chmod +x verifier_linux_amd64
```

Now, we have something to do with `config.yaml` file, take a look this sample
```
Http:
  Listen: "127.0.0.1:10801"
Network: "testnet"
RemoteBootstrap: "https://glacier-labs.github.io/node-bootstrap/"
Keystore:
  PrivateKey: "YourPrivateKey"
TEE:
  IpfsURL: "https://greenfield.onebitdev.com/ipfs/"
```

We are going to change PrivateKey: `"YourPrivateKey"` with our wallet PK.

```
nano config.yaml
```

Then paste your Private Key there, hit `CTRL + X` and hit `Y` to save.

## Running the Node
Simply just enter this command...to make new session called `glacier-node`

TIPS! screen si terminal multiplexer allowing user to make multiple session in one terminal.

```
screen -S glacier-node
```

```
./verifier_linux_amd64
```

Hit `CTRL + A + D` to minimize the session, if you want to enter that session again
```
screen -R glacier-node
```

Thanks for reading. Don't forget to [join our Telegram channel](https://t.me/airdropStalkerChannel).
