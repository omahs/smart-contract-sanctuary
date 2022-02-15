<sup>
 <b>Smart Contract Sanctuary - MultiRepo / Index</b><br>
 ⚠️<b>UPDATE:</b> Repo layout changed! see <a href="https://github.com/tintinweb/smart-contract-sanctuary/issues/13">#13</a> (<a href="https://github.com/tintinweb/smart-contract-sanctuary/releases/tag/v1">v1-layout</a>)
</sup>

# Smart Contract Sanctuary
🐦🌴🌴🌴🦕 A home for ethereum smart contracts verified on Etherscan. 🏠
<br><br>
<sup>
**⇝** This is the **index repository** for the **smart-contract-sanctuary**. 🔖 Bookmark this repo.<br>
**⇝** Chain-specific sub-repos and the index are updated twice a day.<br>
**⇝** Expect a full, recursive check-out to take 2GB+ disk space.<br>
</sup>

## Usage

The repo is configured for use with `git+ssh` (much more stable and faster).

#### First time - clone the index and checkout all chain-specific sub repositories from scratch:

```console
⇒  git clone --recursive --depth=1 git@github.com:tintinweb/smart-contract-sanctuary.git
```

<sub> also see https://git-scm.com/docs/git-submodule for more options</sub>


#### Existing repository but submodules never initialized - checkout submodules and update all chain-specific sub repositories:

```console
⇒  git submodule update --init --remote --depth=1 --progress
```

#### Existing repository with submodules - update all chain-specific sub repositories:

```console
⇒  git submodule update --remote --progress
```

## Layout

| Folder       | Description   |
| ------------ | ------------- |
| _docs        | autogenerated stats; static github page |
| &lt;chain&gt;<sub>/contracts</sub> | Chain specific smart contracts |
| ↳ [ethereum](https://github.com/tintinweb/smart-contract-sanctuary-ethereum)<sub>/contracts</sub> | Git SubModule 👉 https://github.com/tintinweb/smart-contract-sanctuary-ethereum |
| ↳ [arbitrum](https://github.com/tintinweb/smart-contract-sanctuary-arbitrum)<sub>/contracts</sub> | Git SubModule 👉 https://github.com/tintinweb/smart-contract-sanctuary-arbitrum|
| ↳ [avalanche](https://github.com/tintinweb/smart-contract-sanctuary-avalanche)<sub>/contracts</sub> | Git SubModule 👉 https://github.com/tintinweb/smart-contract-sanctuary-avalanche|
| ↳ [bsc](https://github.com/tintinweb/smart-contract-sanctuary-bsc)<sub>/contracts</sub> | Git SubModule 👉 https://github.com/tintinweb/smart-contract-sanctuary-bsc|
| ↳ [fantom](https://github.com/tintinweb/smart-contract-sanctuary-fantom)<sub>/contracts</sub> | Git SubModule 👉 https://github.com/tintinweb/smart-contract-sanctuary-fantom|
| ↳ [polygon](https://github.com/tintinweb/smart-contract-sanctuary-polygon)<sub>/contracts</sub> | Git SubModule 👉 https://github.com/tintinweb/smart-contract-sanctuary-polygon|
| ↳ [tron](https://github.com/tintinweb/smart-contract-sanctuary-tron)<sub>/contracts</sub> | Git SubModule 👉 https://github.com/tintinweb/smart-contract-sanctuary-tron|
| &lt;chain&gt;<sub>/utils</sub> | Chain specific support scripts |


##### 📂 &lt;chain&gt;/contracts

Contains smart contract sources for various networks, grouped by the first two chars of the contract address.
Files are named in the format `<address>_<source_unit_name>`, e.g. `0f0c3fedb6226cd5a18826ce23bec92d18336a98_URToken.sol`

Some contracts are listed in `contracts.json`, but the file-system may contain more files than what is listed in this summary. Rely on the folder/file structure for a full list. 
This repo used to auto submit contracts to [4byte.directory](https://www.4byte.directory/).


##### 📂 &lt;chain&gt;/utils

Support scripts for various activies like dumping smart contracts from public sources (etherscan.io, etherchain.com)

**requires:** `pip install -r requirements.txt`

###### Dev Notes

To use [List of Verified Contract addresses with an OpenSource license](https://etherscan.io/exportData?type=open-source-contract-codes), you can download the csv file, add it to the util folder, and run `parse_download_contracts_etherscan_io.py` (with your etherscan API). This will add the new contracts to the appropriate folder

## 👩‍🔬 Data Science Tools

* [🧠 SolGrep](https://github.com/tintinweb/solgrep) - A scriptable semantic grep utility for solidity (crunch numbers, find specific contracts, extract data)

## 🎓 Citation

If you are using this dataset in your research and paper, here's how you can cite this dataset: 

- APA6
```
Ortner, M., Eskandari, S. (n.d.). Smart Contract Sanctuary. Retrieved from https://github.com/tintinweb/smart-contract-sanctuary.
```

- LateX (Bib)
```
 @article{smart_contract_sanctuary, 
          title={Smart Contract Sanctuary}, 
          url={https://github.com/tintinweb/smart-contract-sanctuary}, 
          author={Ortner, Martin and Eskandari, Shayan}} 
 ```
