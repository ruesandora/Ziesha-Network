<h1 align="center"> ℤiesha Network | The Pelmeni Testnet </h1>

![image](https://user-images.githubusercontent.com/101149671/215441281-fcccd88d-68c9-4ee7-b967-cc0e00824ae5.png)


## Bu testnetnette yapacaklarımız ve önemli konular:

> Öncelikle node'unuzun güncel olduğundan emin olun, eğer node'unuz testnet sürelerinde güncel değilse ağda `offline` olarak gözükürsünüz (explorer'da gözükseniz bile)

> [Github](https://github.com/ziesha-network), [Twitter](https://twitter.com/ZieshaNetwork), [Telegram](https://t.me/ZieshaNetworkOfficial) hesaplarını takip ettiğinizden emin olun, ana rehberde yazıyor, şart.

> [Discord'dan](discord.gg/zieshanetwork) `Pelmeni-Testnet` rolü aldığınızdan emin olun. `#role-selection` kanalında mevcut

> Testnet dışında ödül kazanmanız için [Quiz event etkinliği](https://twitter.com/ZieshaNetwork/status/1614997376892108803?s=20&t=NvIz0IWvWPi2Zn3LpI_8Ug) ve [Contributors](https://discord.com/channels/923604493378154496/1046481849163190343/1046482599415140452) olma şansı var, bu role şu an sadece 35 kişi sahip.

> Katıldığınız testnetin Repo'sunu forklamayı unutmayın, kesinlikle bir github hesabınız olsun ve katıldığınız testnetler hakkında profilde reponuz olsun.

> Testnete 3 şekilde katılabiirsiniz, [buradan](https://github.com/ruesandora/Ziesha-Network/blob/main/README.md#testnete-3-%C5%9Fekilde-kat%C4%B1labilirsiniz) kontrol edin.

## Sistem gereksinimleri:

```
2 CPU
2 RAM
20 SSD
```

## Kurulum:

```
sudo apt-get update && sudo apt-get upgrade
```
```
sudo apt install -y build-essential libssl-dev cmake
```
```
apt install git
```
```
apt install screen
```

> `rustup`'u kurduğunuzda `1-2-3` seçenekleri gelecek ve `1`'i seçip enterleyin.

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
```
git clone https://github.com/ziesha-network/bazuka
source "$HOME/.cargo/env"
```
```
cd bazuka
cargo install --path .
```

## Nodu başlatacağız:
> bazuka init komutunu girerken eğer daha önce cüzdan oluşturduysanız ve 12 kelimeniz varsa komutun sonuna --mnemonic "mnemonic" ekleyin.

> Eğer 12 kelimeniz yoksa komutu direkt girdiğinizde size 12 kelime verecek onu saklayın. Veya [buradan](http://ziesha.network/zeejs/) oluşturabilirsiniz

> IPADRESİNİZİ girmeyi unutmayın!

```sh
bazuka init --network pelmeni --external IPADRESİ:8765 --bootstrap 213.14.138.127:8765
```

## Şimdi nodu çalıştıracağız:

> Tırnak içersine discord adınızı girin. örnek `"Rues#9144"`

```
screen -S ziesha
```

```sh
bazuka node start --discord-handle "YOUR DISCORD HANDLE"
```

## Çalıştığını nasıl anlarız?

> `bazuke node start` komutunu girdikten ve bir kaç dakika bekledikten sonra görselde ki gibi gözükecektir.

![image](https://user-images.githubusercontent.com/101149671/215362906-ab86fec5-77b5-4a6d-b951-104525cf1b3d.png)

> `Height` 1-2-3 şeklinde, `Node count` 1-2-3 şeklinde artmaya başlayacak.

## Faydalı komutlar:

> Node'umuzu ziesha adlı `screen` içersinde çalıştırdık:

* Node çalıştıktan sonra screen'den çıkmak için `CTRL A D` tuşlarına basıyoruz.
* Tekrar bu screen içersine girmek için `screen -r ziesha` komutunu giriyoruz.
* Eğer bu komut ile screen içersine giremezseniz `screen -d -r ziesha` 'yı kullanabilirsiniz.
* Screen'i silmek için `screen -XS screen adı quit` ve tüm screenleri silmek için `pkill screen`.
* Yeni screen açmak için `screen -S screen adı`

> Güncelleme komutu:

* Bu komut her güncelleme için geçerli değildir, lütfen güncellemeler için `#pelmeni-testnet` kanalını takip edin.

```sh
cd bazuka
git pull origin master
cargo update
cargo install --path .
bazuka node start --discord-handle "YOUR DISCORD HANDLE"
```

## Bir kaç gün sonra devamını ekleyeceğim..


## Testnete 3 şekilde katılabilirsiniz:

* 1. Node kurabilirsiniz. (yukarı da ki rehber)
* 2. Solo madencilik veya bir havuza katılarak madenci olabilirsiniz. (Madenci olmak için [buradan](https://github.com/ziesha-network/x-testnet#mine-ziesha-as-a-solo-miner))
* 3. Madenci hazunun sahibi olabilirsiniz. (Havuz oluşturmak için [buradan](https://github.com/ziesha-network/x-testnet#mine-ziesha-in-a-mining-pool))












































