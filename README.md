# Prysm beacon-chain DAppNode package

# Install this DNP:
To install, join your dappnode wireless network, then click this link:

[![Install DNP](https://img.shields.io/badge/DAppNode-Available-brightgreen.svg)](http://my.dappnode/#/installer/%2Fipfs%2FQmc4Gfb6f7v76i8fkeMeKEjouhYJzqPTwXLSTf7ZoeUgnh)

# Additional Prysm Info:
[![prysm github](https://img.shields.io/badge/prysm-Github-blue.svg)](https://prylabs.net/)
[![prysm participate](https://img.shields.io/badge/prysm-participate-753a88.svg)](https://prylabs.net/participate)

# Adding a validator:

### (THIS SECTION IS A WORK IN PROGRESS)

1. After the installation the beacon-chain and the validator should be running on your DAppNode: http://my.dappnode/#/packages

![](https://i.imgur.com/11y8pgQ.png)

2. Go to https://prylabs.net/participate

    3.1 Skip step one, go to number two (Get GöETH — Test ether) and follow the steps

    3.2 Generate a validator public / private key

    To obtain this data you will have to download a file from your dappnode, to do this:

    * Go to: http://my.dappnode/#/Packages/prysm-validator.public.dappnode.eth
    * File Manager > Download from DNP
    * Write `/data/deposit_data.txt` and click Download
    * Open the file, and you will get something like this:

        ```
        ========================Deposit Data=======================

        0xbc0000006....

        ===========================================================
        ```
    * Paste the value `0xbc0000006...` in the field `your validator deposit data`
   ![](https://i.imgur.com/mZVLC6u.png)

    3.2 Skip step four and go to number five (Send a validator deposit) and `Make deposit`.

    3.3 Wait for your validator assignment (it takes a while)

    ![](https://i.imgur.com/fmDspYw.png)


**Congratulations! With this you will already have a network validator node on testnet**

You can check it by looking at the validator logs: http://my.dappnode/#/Packages/prysm-validator.public.dappnode.eth

![](https://i.imgur.com/Sfq88es.png)


## Note

This is early stage software and it's just a PoC

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details
