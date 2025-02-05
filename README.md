<h1 align="center"> Zeeka Network | Bazuka </h1>

![image](https://user-images.githubusercontent.com/101149671/188958599-67a3b79f-9dc1-450f-b2fd-4461598b9100.png)

<h1 align="center"> Selamlar, bu repoda Zeeka Network node kurulum rehberi ile karşınızdayım </h1>

 * Cosmos dışı bir proje olduğu için kurmanızı öneririm

 * Ödüllü değil, ödüllü testnet yakında

 * Hocam sunucum boşta ne kuralım diyenler için

 * Sorularınız için: [Sohbet kanalı](https://discord.gg/jZBhUBf7)

## Sistem gereksinimleri:
```
2 CPU
2 RAM
50 SSD (fazla bile)
```

## libssl-dev kurarak başlıyoruz:
```
sudo apt update && sudo apt upgrade -y
sudo apt install curl tar wget clang pkg-config libssl-dev jq build-essential bsdmainutils git 
make ncdu gcc git jq chrony liblz4-tool -y
```

## cmake kuruyoruz:
```
sudo apt install cmake -y
```

## rustup'ı kuruyoruz:

 * Kurulum tamamlandıktan sonra 1'e basıp enterliyoruz

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
![image](https://user-images.githubusercontent.com/101149671/188959152-b52fae46-8004-4fa5-9ca3-e0758c6f3301.png)

## git clone çekiyoruz:
```
git clone https://github.com/zeeka-network/bazuka
```

## Cargo'yu yüklüyoruz:
```
apt install cargo -y
```

## path'i kuruyoruz:

```
cd
cd bazuka && cargo install --path .
```

## Görselde ki gibi bir uyarı alırsanız bu komutu
```
source "$HOME/.cargo/env"
```

![image](https://user-images.githubusercontent.com/101149671/188959534-3ea71c13-fe85-430b-8cdb-8c0650c982ec.png)

## seedi ekliyoruz:
```
bazuka init --seed 38b4d78c7d6582fb170f6c19330a7e37e6964212@rues.forum.info:8765 --network debug --node 127.0.0.1:8765
```

## nodu kuruyoruz:

 * your external ip kısmını sunucu ip'inizi girin ve daha sonra parantezleri kaldırın

```
bazuka node --network debug --bootstrap [your_external_ip]:8765
--network debug --db ~/.bazuka-debug --bootstrap 152.228.155.120:8765 --bootstrap 95.182.120.179:8765 --bootstrap 195.2.80.120:8765 --bootstrap 195.54.41.148:8765 --bootstrap 65.108.244.233:8765 --bootstrap 195.54.41.130:8765 --bootstrap 185.213.25.229:8765 --bootstrap 195.54.41.115:8765 --bootstrap 62.171.188.69:8765 --bootstrap 49.12.229.140:8765 --bootstrap 213.202.238.77:8765 --bootstrap 5.161.152.123:8765 --bootstrap 65.108.146.132:8765 --bootstrap 65.108.250.158:8765 --bootstrap 195.2.73.130:8765 --bootstrap 188.34.167.3:8765 --bootstrap 188.34.166.77:8765 --bootstrap 45.88.106.199:8765 --bootstrap 79.143.188.183:8765 --bootstrap 62.171.171.11:8765 --bootstrap 65.108.201.41:8765 --bootstrap 159.203.176.252:8765 --bootstrap 194.163.191.80:8765 --bootstrap 146.19.207.4:8765 --bootstrap 135.181.43.174:8765 --bootstrap 95.111.234.205:8765 --bootstrap 192.241.131.113:8765 --bootstrap 45.67.217.16:8765 --bootstrap 65.108.157.67:8765 --bootstrap 65.108.251.175:8765 --bootstrap 95.216.204.235:8765 --bootstrap 45.82.178.159:8765 --bootstrap 161.97.111.145:8765 --bootstrap 149.102.133.130:8765 --bootstrap 65.108.61.32:8765 --bootstrap 95.216.204.32:8765 --bootstrap 188.34.160.74:8765 --bootstrap 185.245.183.246:8765 --bootstrap 213.246.39.14:8765

```

## nodu çalıştırıyoruz:
```
apt install screen
```
```
screen -S bazuka
```
```
bazuka node
```

## Nodunuz bu şekilde çalışır olacak:

 * Cüzdanlarınızı kaydedin.

![image](https://user-images.githubusercontent.com/101149671/188964602-895b445c-8829-4d72-bb5a-ed57a0a41f84.png)

## Miner floodu paylaşmadım, yakında ödüllüye geçeceğiz zaten, illa kuracağım derseniz: [Rehber](https://github.com/zeeka-network/bazuka)

## Explorer [Linki](http://152.228.155.120:8000/)
