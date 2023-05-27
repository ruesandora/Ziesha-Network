<h1 align="center"> Ziesha Network | Deruny Testnet </h1>


<h1 align="center"> Bu testnetnette yapacaklarımız ve önemli konular </h1>

> Öncelikle node'unuzun güncel olduğundan emin olun, eğer node'unuz testnet sürelerinde güncel değilse ağda `offline` olarak gözükürsünüz (explorer'da gözükseniz bile)

> [Github](https://github.com/ziesha-network), [Twitter](https://twitter.com/ZieshaNetwork), [Telegram](https://t.me/ZieshaNetworkOfficial) hesaplarını takip ettiğinizden emin olun.

> [Discord'dan](discord.gg/zieshanetwork) `Deruny-Testnet` rolü aldığınızdan emin olun. `#role-selection` kanalında mevcut

> Katıldığınız testnetin Repo'sunu forklamayı unutmayın, kesinlikle bir github hesabınız olsun ve katıldığınız testnetler hakkında profilde reponuz olsun.

<h1 align="center"> Sistem Gereksinimleri </h1>

>  Hetzner'in en küçük sunucusu yeterli, [Hetzner Rehberi Linki](https://github.com/ruesandora/Hetzner/blob/main/README.md)
```
2 CPU
2 RAM
20 SSD
```

<h1 align="center"> Kurulum </h1>

```
sudo apt-get update && sudo apt-get upgrade -y
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

# cargo yüklemesi biraz uzun (birkaç dakika) sürebilir.
```

<h1 align="center"> Node'u başlatalım </h1>

> bazuka init komutunu girerken eğer daha önce cüzdan oluşturduysanız ve 12 kelimeniz varsa komutun sonuna --mnemonic "mnemonic" ekleyin.

> Eğer 12 kelimeniz yoksa komutu direkt girdiğinizde size 12 kelime verecek onu saklayın. Veya [buradan](http://ziesha.network/zeejs/) oluşturabilirsiniz

> IPADRESİNİZİ girmeyi unutmayın!

```sh
bazuka init --external 5.75.182.65:8765 --bootstrap 31.210.53.186:8765
```

<h1 align="center"> Node'u çalıştıralım </h1>

> Tırnak içersine discord adınızı girin. örnek `"Rues#9144"`

```
screen -S ziesha
```
```sh
bazuka node start --discord-handle "Rues"
```

<h1 align="center"> Çalıştığını nasıl anlarız? </h1>

> `bazuke node start` komutunu girdikten ve bir kaç dakika bekledikten sonra görselde ki gibi gözükecektir.

![image](https://user-images.githubusercontent.com/101149671/215362906-ab86fec5-77b5-4a6d-b951-104525cf1b3d.png)

> `Height` 1-2-3 şeklinde, `Node count` 1-2-3 şeklinde artmaya başlayacak.

<h1 align="center"> Faydalı komutlar </h1>

> Node'umuzu ziesha adlı `screen` içersinde çalıştırdık:

* Node çalıştıktan sonra screen'den çıkmak için `CTRL A D` tuşlarına basıyoruz.
* Tekrar bu screen içersine girmek için `screen -r ziesha` komutunu giriyoruz.
* Eğer bu komut ile screen içersine giremezseniz `screen -d -r ziesha` 'yı kullanabilirsiniz.
* Screen'i silmek için `screen -XS screen adı quit` ve tüm screenleri silmek için `pkill screen`.
* Yeni screen açmak için `screen -S screen adı`

> Güncelleme komutu:

* Bu komut her güncelleme için geçerli değildir, lütfen güncellemeler için `#deruny-testnet` kanalını takip edin.

```sh
cd bazuka
git pull origin master
cargo update
cargo install --path .
screen -r ziesha
```
* Node güncellendikten sonra screen'e giriyoruz. `CTRL C` tuşlarıyla durdurup aşağıdaki kodla tekrar çalıştırıyoruz.
```sh
bazuka node start --discord-handle "YOUR DISCORD HANDLE"
```

<h1 align="center"> Validatör ve Prover hakkında </h1>

> Validatör olmak istiyorsanız donanımda herhangi bir değişiklik yok.
>> Token'e ihtiyacınız var bunun için faucet'i kullanabilirsiniz. Aynı zamanda ağda bir kaç işlem yapın.
>>> Validatör nasıl olunur hakkında gün içinde discordda duyuru gelecek.

> Prover olmak isteyenler için GPU'ya ihtiyaçları var.
>> Prover olmak isteyenler prover kanalından diğer proverler ile veya chate yazarak kurulum yapabilir.
>>> Hepsi burada mevcut: https://github.com/ziesha-network/









































