<h1 align="center"> ℤiesha Network | Mining Pool </h1>

## Bir havuz oluşturmak istiyorsanız [Link](https://github.com/ziesha-network/uzi-pool)

## Havuza dahil olmak isteyenler için sistem gereksinimleri:

* Minimum
```
4 RAM (tahmini, test edeceğiz)
CPU Sayınız ne kadar yüksekse, hashrate o kadar çok olur.
```

## Havuza dahil olmadan önce Uzi kuralım:
```
screen -S uzi
```
```
git clone https://github.com/ziesha-network/uzi-miner
cd uzi-miner
cargo update
cargo install --path .
```

## Poola dahil olma:

* Havuzun IP'si ve mıner token kısmını doldurun:
* Bunları yaparken havuz sahibi ile iletişimde olmalısınız.
* Miner token bazuka node kurarken oluşturduğunuz cüzdan çıktısında yazıyor
```
uzi-miner --pool --node HAVUZIPİSİ:8766 --threads 32 --miner-token MINER_TOKEN
```

![image](https://user-images.githubusercontent.com/101149671/203015859-ee201937-82a4-40cb-a59e-a408a64acc96.png)



