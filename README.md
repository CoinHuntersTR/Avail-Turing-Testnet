# Avail-Turing-Testnet

Avail Turing Testnet

# Kurulum

## Go Setup
```
sudo apt update
sudo apt install make clang pkg-config libssl-dev build-essential
```
```
cd
sudo mkdir avail
```

```
cd avail
```
## Dosyaları çekiyoruz

```
wget https://github.com/availproject/avail/releases/download/v2.0.0.0-rc4/x86_64-ubuntu-2204-avail-node.tar.gz
```

## Dosyaları zipten çıkartıyoruz.

```
tar -xf x86_64-ubuntu-2204-avail-node.tar.gz
```

## Sevis Oluşturuyoruz...

```
sudo tee /etc/systemd/system/availd.service > /dev/null <<'EOF'
[Unit]
Description=Avail Validator
After=network.target
StartLimitIntervalSec=0

[Service]
User=root
Type=simple
Restart=always
RestartSec=120
ExecStart=/root/avail/data-avail -d /root/avail/data --chain turing --validator --name "CoinHunters"
[Install]
WantedBy=multi-user.target
EOF
```
## Node Başlatalım

```
sudo systemctl daemon-reload
sudo systemctl enable availd.service
sudo systemctl restart availd.service
```
## Loglara Bakalım

```
journalctl -f -u availd.service
```


