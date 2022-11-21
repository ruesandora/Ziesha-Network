<h1 align="center"> ℤiesha Network | Solo miner </h1>

## Sistem gereksinimleri:
```
32 RAM
CPU ne kadar çoksa o kadar hashrate
```

## Kurulum:

* Komutları tek tek girersiniz:
```
screen -S zoro
cd bazuka
git pull origin master
cargo install --path .
apt install ocl-icd-opencl-dev
git clone https://github.com/ziesha-network/zoro
cd zoro
cargo install --path .
wget https://api.rues.info/update.dat
wget https://api.rues.info/withdraw.dat
wget https://api.rues.info/deposit.dat
```

## Zoro'yu çalıştıralım:

* Seed kısmına bir seed belirleyin (örnek: ruesseed) ve saklayın.
* Ekran kartınız varsa komutun sonuna `--gpu` ekleyin

```sh
zoro --node 127.0.0.1:8765 --seed "SEED" --network groth \
  --update-circuit-params update.dat --deposit-circuit-params deposit.dat \
  --withdraw-circuit-params withdraw.dat --db $HOME/.bazuka
```

## Uzi'yi çalıştırıyoruz:

* Zoro'dan CTRL+A+D ile çıkalım:
```
screen -S uzi
```
```
git clone https://github.com/ziesha-network/uzi-miner
cd uzi-miner
cargo install --path .
uzi-miner --node 127.0.0.1:8765 --threads 32
```












