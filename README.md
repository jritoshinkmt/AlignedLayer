# Aligned Layer
Fast And Cheap Proof Verification. Accelerating the Ethereum roadmap by simplifying ZK adoption.

![0szR3LkkCdWATnRyNr9wy](https://github.com/jritoshinkmt/AlignedLayer/assets/80070027/ae29dec0-9997-4bca-85ee-472d97490ce7)
**Official Links: [Website](https://alignedlayer.com) ┃ [X](https://x.com/alignedlayer) ┃ [Discord](https://discord.com/invite/alignedlayer) ┃ [Telegram](https://t.me/aligned_layer) ┃ [Galxe](https://app.galxe.com/quest/Aligned)**

<br>

## ➤ Getting Started
**Update & Upgrade Packages**
```
sudo apt update -y
```
```
sudo apt upgrade -y
```
### Install curl 
```
sudo apt-get install curl -y
```

<br>
<br>
 
## ➤ Download and install Aligned Proofs
<img width="712" alt="image" src="https://github.com/jritoshinkmt/AlignedLayer/assets/80070027/faeadb71-af20-4d86-bb6b-c8d17398e52e">

```
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/install_aligned.sh | bash
```

**• run this command if you are using a VPS**
```
source /root/.bashrc
```
**• run this command if you are using a Gitpod**
```
source /home/gitpod/.bashrc
```

<br>
<br>
 
## ➤ Download an example SP1 proof & ELF file
![image](https://github.com/jritoshinkmt/AlignedLayer/assets/80070027/bc4eaaf4-b53f-4c4e-b252-3e94b3d1afbb)

```
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/get_proof_test_files.sh | bash
```

<br>
<br>
 
## ➤ Send the proof
<img width="840" alt="image" src="https://github.com/jritoshinkmt/AlignedLayer/assets/80070027/80e59b53-b055-404b-b4a1-29fcc84e4e74">

```
rm -rf ~/aligned_verification_data/ &&
aligned submit \
--proving_system SP1 \
--proof ~/.aligned/test_files/sp1_fibonacci.proof \
--vm_program ~/.aligned/test_files/sp1_fibonacci-elf \
--aligned_verification_data_path ~/aligned_verification_data \
--conn wss://batcher.alignedlayer.com
```

> [!NOTE]
> You should get a response like the **blue block** in the image above ⬆️
> 
> Click and Copy your the Explorer Block LinkSure, and you will also see the image below ⬇️

![image](https://github.com/jritoshinkmt/AlignedLayer/assets/80070027/7004ae8d-1d71-4a4e-9d96-61df367a4671)
 
<br>
<br>
 
## ➤ Check the status of your transaction
<img width="457" alt="image" src="https://github.com/jritoshinkmt/AlignedLayer/assets/80070027/ca65d3bc-0ed5-4e20-afab-4a62cfb678f0">

```
aligned verify-proof-onchain \
--aligned-verification-data ~/aligned_verification_data/*.json \
--rpc https://ethereum-holesky-rpc.publicnode.com \
--chain holesky
```

✅You should get this result:
```
[2024-06-17T21:58:43Z INFO  aligned] Your proof was verified in Aligned and included in the batch!
```

❌If the proof wasn't verified you should get this result:
```
[2024-06-17T21:59:09Z INFO  aligned] Your proof was not included in the batch.
```

<br>
<br>
 
## ➤ Take A Screenshoot, upload to X and Discord
<img width="847" alt="image" src="https://github.com/jritoshinkmt/AlignedLayer/assets/80070027/7764336d-20e6-4f4e-ad57-09a906169b06">

> [!NOTE]
> **X Post Template:**
> ![IMG_4986](https://github.com/jritoshinkmt/AlignedLayer/assets/80070027/95a9d16f-00b2-4f88-b3c6-3e3b53c094a4)

```
Just submitted a proof via @alignedlayer
I am now #aligned ✅

[Paste Your Block Explorer Link]
```

> [!NOTE]
> **Discord Post Template:**
> ![image](https://github.com/jritoshinkmt/AlignedLayer/assets/80070027/9a63ea20-16ac-438f-98e8-bef49c0cbbab)
