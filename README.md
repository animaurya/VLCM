Hyperledger

$ curl -sSL http://bit.ly/2ysbOFE | sudo bash -s 1.3.0 "install the Fabric Samples and binaries"

$ cd fabric-samples

$ export PATH=/bin:$PATH "to add that to your PATH environment variable so that these can be picked up without fully qualifying the path to each binary."

$ cd first-network "Let’s open that sub-directory now <fabric-samples/first-network>"

$ sudo ./byfn.sh generate "Generate Network Artifacts -- generates all of the certificates and keys for our various network entities, the genesis block used to bootstrap the ordering service, and a collection of configuration transactions required to configure a Channel"

$ sudo ./byfn.sh up "Bring Up the Network -- compile Golang chaincode images and spin up the corresponding containers"

$ sudo ./byfn.sh down "Bring Down the Network --bring it all down so we can explore the network setup one step at a time. The following will kill your containers, remove the crypto material and four artifacts, and delete the chaincode images from your Docker Registry"

[//]: # (SPDX-License-Identifier: CC-BY-4.0)

## Hyperledger Fabric Samples

Please visit the [installation instructions](http://hyperledger-fabric.readthedocs.io/en/latest/install.html)
to ensure you have the correct prerequisites installed. Please use the
version of the documentation that matches the version of the software you
intend to use to ensure alignment.

## Download Binaries and Docker Images

The [`scripts/bootstrap.sh`](https://github.com/hyperledger/fabric-samples/blob/release-1.3/scripts/bootstrap.sh)
script will preload all of the requisite docker
images for Hyperledger Fabric and tag them with the 'latest' tag. Optionally,
specify a version for fabric, fabric-ca and thirdparty images. Default versions
are 1.4.0, 1.4.0 and 0.4.14 respectively.

```bash
./scripts/bootstrap.sh [version] [ca version] [thirdparty_version]
```

## License <a name="license"></a>

Hyperledger Project source code files are made available under the Apache
License, Version 2.0 (Apache-2.0), located in the [LICENSE](LICENSE) file.
Hyperledger Project documentation files are made available under the Creative
Commons Attribution 4.0 International License (CC-BY-4.0), available at http://creativecommons.org/licenses/by/4.0/.
