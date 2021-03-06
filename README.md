# Prysm beacon-chain DAppNode package

[![DAppNode Available](https://img.shields.io/badge/DAppNode-Available-brightgreen.svg)](http://my.dappnode/#/installer/prysm-beacon-chain.public.dappnode.eth)

[![prysm github](https://img.shields.io/badge/prysm-Github-blue.svg)](https://prylabs.net/)
[![prysm participate](https://img.shields.io/badge/prysm-participate-753a88.svg)](https://prylabs.net/participate)

# Installation Notes

1. Install the DAppNodePackage: 

[![DAppNode Install](https://img.shields.io/badge/DAppNode-Install-blue.svg)](http://my.dappnode/#/installer/%2Fipfs%2FQmZQ35roYu64Pb6kohzNVpSHoSGcCV1wx5KBRJSrFg5Zgu)

2. After the installation the beacon-chain and the validator should be running on your DAppNode: http://my.dappnode/#/packages

![](https://i.imgur.com/11y8pgQ.png)

3. Go to https://prylabs.net/participate

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


## Updating beacon chain image
By default is going to use "latest" as image. 

If you want to use an expecific version you can do it by adding it to the .env file
```
echo "VERSION=@sha256:12dd8ace1d9f754184de2574eab96a8f447ca5c89e0b0c9f5bf25fa558acd80a" > .env
```
## Note

This is early stage software and it's just a PoC

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details
