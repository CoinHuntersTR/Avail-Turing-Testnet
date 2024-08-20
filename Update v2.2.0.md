## Update v2.2.0

### Release Information:
Binary Version: v2.2.5.0-rc1
Node Version: v2.2.0

```
cd avail
```
## Dosyaları çekiyoruz

```
wget https://github.com/availproject/avail/releases/download/v2.2.5.0-rc1/x86_64-ubuntu-2204-avail-node.tar.gz
```

## Dosyaları zipten çıkartıyoruz.

```
tar -xf x86_64-ubuntu-2204-avail-node.tar.gz
```

## Sevis Oluşturuyoruz...

```
screen -r avail
```

## Node Başlatalım

> [name your node] yerine Validator ismini giriyoruz.

```
./avail-node --chain turing --name [name your node] --validator
```
