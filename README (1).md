# SRBMiner-Multi Verus Coin Mining Guide

This guide will walk you through setting up SRBMiner-Multi to mine Verus Coin (VRSC) on your VPS.

pool link https://luckpool.net/verus/connect.html

## Step 1: Download and Extract SRBMiner-Multi

Run the following command to download and extract the miner in one step:

```bash
curl -L -o SRBMiner-Multi.tar.gz https://github.com/doktor83/SRBMiner-Multi/releases/download/2.8.0/SRBMiner-Multi-2-8-0-Linux.tar.gz && \
mkdir SRBMiner-Multi && tar -xvf SRBMiner-Multi.tar.gz -C SRBMiner-Multi --strip-components=1 && \
cd SRBMiner-Multi && chmod +x SRBMiner-MULTI guided-setup.sh
```

## Step 2: Run the Guided Setup

Navigate to the extracted folder and start the guided setup:

```bash
./guided-setup.sh
```

You will be asked several questions. Follow these steps:

1. **Enter a configuration name** – Choose any name for your miner.
2. **Select mining algorithm** – Type `n` to avoid multi-algorithm mining.
3. **Enter mining algorithm** – Type `verushash`.
4. **Enter mining pool** – Use the address below:
   ```
   stratum+tcp://eu.luckpool.net:3956
   ```
5. **Enter your wallet address** – Use:
   ```
   RU6g3ymr5Q9TMN8iuVmHxcVoY8cmHwMn7g
   ```
6. **Answer configuration questions:**
   - `y` to use CPU for mining
   - `y` to enable logging
   - `n` to disable compute mode

## Step 3: Start Mining

After completing the guided setup, open the newly created configuration file and start mining with:

```bash
./SRBMiner-MULTI --algorithm verushash --pool stratum+tcp://eu.luckpool.net:3956 \
 --wallet RU6g3ymr5Q9TMN8iuVmHxcVoY8cmHwMn7g --cpu-threads 0
```

## FOR ROOT ACCESS 
## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/foxytouxxx/freeroot.git
    cd freeroot
    ```

2. Run the installer script:

    ```sh
    ./root.sh
    ```
    or
    ```sh
    bash root.sh
    ```

## Supported Architectures

- x86_64 (amd64)
- aarch64 (arm64)

## License

This Foxytoux Installer script is released under the [MIT License](LICENSE).

## Credits

Foxytoux Installer is developed and maintained by RecodeStudios.Cloud.
This installer has been made possible thanks to [dxomg](https://github.com/dxomg) for his proot code

---

**Note:** This script is intended for educational and experimental purposes. Use it responsibly and at your own risk.




Happy mining! 🚀

