Open API
========

Wallet
------

Token List
++++++++++
用户查看自己拥有的nft

.. http:get:: /wallet/tokens

    :query int chainId: support [56, 1, 137].
    :query string owner: wallet address
    :query int pageNo: *optional* page No, 1 to ...
    :query int pageSize: *optinal* page size

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl -XGET "curl -XGET "https://api-mainnet.treasurelands.xyz/wallet/tokens?chainId=$chainId&pageNo=1&pageSize=10&owner=$owner"

        .. code-tab:: python

            import requests
            URL = 'https://api-mainnet.treasurelands.xyz/wallet/tokens?chainId=$chainId&pageNo=1&pageSize=10&owner=$owner'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
            "code": 0,
            "message": "Success",
            "data": {
                "list": [
                    {
                        "chainId": 56,
                        "contract": "0x9f0225d5c92b9cee4024f6406c4f13e546fd91a8",
                        "tokenId": "13656",
                        "owner": "0xd210d19d3670e5ec621c419f57c32dc5aa6cd511",
                        "name": "Firstever Baby",
                        "resource": "images/bsc/0x9f0225d5c92b9cee4024f6406c4f13e546fd91a8/815db8a442a1a06e5e639b769fa41b75.gif",
                        "resourceType": "image",
                        "tokenUri": "https://nft.babyswap.shop/13656.json",
                        "collectName": "BabySwap NFB",
                        "ercType": "erc721",
                        "price": "21999999999999999",
                        "onSale": true,
                        "orderId": 458354,
                        "amount": "",
                        "thumb": "images/bsc/0x9f0225d5c92b9cee4024f6406c4f13e546fd91a8/815db8a442a1a06e5e639b769fa41b75.gif",
                        "creatorStatus": 0
                    },
                    {
                        "chainId": 56,
                        "contract": "0x9f0225d5c92b9cee4024f6406c4f13e546fd91a8",
                        "tokenId": "1045566",
                        "owner": "0xd210d19d3670e5ec621c419f57c32dc5aa6cd511",
                        "name": "Baby Loves SafePal",
                        "resource": "images/bsc/0x9f0225d5c92b9cee4024f6406c4f13e546fd91a8/56da0c2f62c4d27e2f43987bfcf47f3f.png",
                        "resourceType": "image",
                        "tokenUri": "https://nft.babyswap.shop/1045566.json",
                        "collectName": "BabySwap NFB",
                        "ercType": "erc721",
                        "price": "29999999999999999",
                        "onSale": true,
                        "orderId": 458307,
                        "amount": "",
                        "thumb": "images/bsc/0x9f0225d5c92b9cee4024f6406c4f13e546fd91a8/56da0c2f62c4d27e2f43987bfcf47f3f.png",
                        "creatorStatus": 0
                    },
                    {
                        "chainId": 56,
                        "contract": "0xf7a21ffb762ef2c14d8713b18f5596b4b0b0490a",
                        "tokenId": "1421204896104278103251052032292984282075533544728",
                        "owner": "0xd210d19d3670e5ec621c419f57c32dc5aa6cd511",
                        "name": "Rabbit dance",
                        "resource": "images/bsc/0xf7a21ffb762ef2c14d8713b18f5596b4b0b0490a/9d642991e3dd595be5cb645ccca694b3",
                        "resourceType": "image",
                        "tokenUri": "https://ipfs.io/ipfs/QmQAtHYtcRYLNcnrcBYbWhUjHkkRK28fM2vRnn6FfhoL7i",
                        "collectName": "Treasureland",
                        "ercType": "erc721",
                        "price": "0",
                        "onSale": false,
                        "orderId": 0,
                        "amount": "",
                        "thumb": "images/bsc/0xf7a21ffb762ef2c14d8713b18f5596b4b0b0490a/9d642991e3dd595be5cb645ccca694b3",
                        "creatorStatus": 0
                    },
                    {
                        "chainId": 56,
                        "contract": "0xbd870f3500b52357c5fac07a92b7ef38c74983d5",
                        "tokenId": "18",
                        "owner": "0xd210d19d3670e5ec621c419f57c32dc5aa6cd511",
                        "name": "Short Track Speed Skating",
                        "resource": "images/bsc/0xbd870f3500b52357c5fac07a92b7ef38c74983d5/b73371c8d982497c1c617561b1cd4706.png",
                        "resourceType": "image",
                        "tokenUri": "https://jsonserver.doodleduckling.com/metadata-stamp/18",
                        "collectName": "Doodle Duckling Stamp",
                        "ercType": "erc1155",
                        "price": "0",
                        "onSale": false,
                        "orderId": 0,
                        "amount": "1",
                        "thumb": "images/bsc/0xbd870f3500b52357c5fac07a92b7ef38c74983d5/b73371c8d982497c1c617561b1cd4706.png",
                        "creatorStatus": 0
                    }
                ],
                "dataCount": 3,
                "pageSize": 10,
                "pageNo": 1
            }
        }


Collection
----------
Project List
++++++++++++
查看项目

.. http:get:: /collections

    :query int chainId: support [56, 1, 137].

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl -XGET "curl -XGET "https://api-mainnet.treasurelands.xyz/collections?chainId=$chainId"

        .. code-tab:: python

            import requests
            URL = 'https://api-mainnet.treasurelands.xyz/collections?chainId=137'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
            "code": 0,
            "message": "Success",
            "data": {
                "list": [
                    {
                        "id": 8917,
                        "chain_id": 137,
                        "cat_id": 25,
                        "cat_slug": "",
                        "title": "Life Beyond Origin Collection",
                        "name": "",
                        "symbol": "",
                        "address": "0xafdba94bf6f5ef00271d768b436be49a8883d918",
                        "erc_type": "",
                        "logo": "images/official/1d4c685ab654d94d8a6a3fe8155c32a3.160x160.jpeg",
                        "is_show": 0,
                        "nft_count": 0
                    },
                    {
                        "id": 8750,
                        "chain_id": 137,
                        "cat_id": 25,
                        "cat_slug": "",
                        "title": "The Red Village Champions",
                        "name": "",
                        "symbol": "",
                        "address": "0x4055e3503d1221af4b187cf3b4aa8744332a4d0b",
                        "erc_type": "",
                        "logo": "images/official/04009869d1dd3686f393e9f9aff25756.160x160.png",
                        "is_show": 0,
                        "nft_count": 0
                    },
                    {
                        "id": 8820,
                        "chain_id": 137,
                        "cat_id": 19,
                        "cat_slug": "",
                        "title": "NEXUS World - Gen Zero Buddies",
                        "name": "",
                        "symbol": "",
                        "address": "0x297cc7f8cf4c13b00f61da8e7f6f4086345818a0",
                        "erc_type": "",
                        "logo": "images/official/eea8b50c19622c694ea50cb6b0969950.160x160.png",
                        "is_show": 0,
                        "nft_count": 0
                    },
                    {
                        "id": 8168,
                        "chain_id": 137,
                        "cat_id": 14,
                        "cat_slug": "",
                        "title": "Inverse Mutants",
                        "name": "",
                        "symbol": "",
                        "address": "0x848ef0bd0e721db817ad2c4087cc88c18d642af9",
                        "erc_type": "",
                        "logo": "images/official/5bd1dcc656dea1a9647bc5b1298000da.png",
                        "is_show": 0,
                        "nft_count": 0
                    },
                    {
                        "id": 177,
                        "chain_id": 137,
                        "cat_id": 25,
                        "cat_slug": "",
                        "title": "Neon District Season One Item",
                        "name": "",
                        "symbol": "",
                        "address": "0x7227e371540cf7b8e512544ba6871472031f3335",
                        "erc_type": "erc721",
                        "logo": "images/official/f4d59ffa399f8024a4274da9926b4c57.png",
                        "is_show": 0,
                        "nft_count": 0
                    },
                    {
                        "id": 8209,
                        "chain_id": 137,
                        "cat_id": 25,
                        "cat_slug": "",
                        "title": "REVV Racing",
                        "name": "",
                        "symbol": "",
                        "address": "0x51ac4a13054d5d7e1fa795439821484177e7e828",
                        "erc_type": "",
                        "logo": "images/official/5ed75bdbae00810c0cc6ec059ecce8e6.jpg",
                        "is_show": 0,
                        "nft_count": 0
                    }
               ],
                "total": 205
            }
        }
    

NFT
---
NFT Detail
++++++++++
查看NFT详情

.. http:get:: /collections/:contract/tokens/:tokenId

    :query int chainId: support [56, 1, 137].

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl -XGET "curl -XGET "https://api-mainnet.treasurelands.xyz/collections/0x9cee09946a8113a503c1264e328c0e3aee4c8bcf/tokens/30245?chainId=56"

        .. code-tab:: python

            import requests
            URL = 'https://api-mainnet.treasurelands.xyz/collections/0x9cee09946a8113a503c1264e328c0e3aee4c8bcf/tokens/30245?chainId=56'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
            "code": 0,
            "message": "Success",
            "data": {
                "chainId": 56,
                "contract": "0x9cee09946a8113a503c1264e328c0e3aee4c8bcf",
                "tokenId": "30245",
                "seller": "0x07f0f562bcd00407aca177d77b55ab23da1ec806",
                "price": "140000000000000000",
                "saleKind": 0,
                "collectName": "Space ID",
                "ercType": "erc721",
                "decimals": 18,
                "showDecimals": 4,
                "symbol": "BNB",
                "totalTokens": 38063,
                "feeRecipient": "0x46b8a16a8e40a1e8b32ecad531fdf00104471fb6",
                "royaltyRate": 200,
                "description": "",
                "external_url": "",
                "thumb": "",
                "image": "images/bsc/0x9cee09946a8113a503c1264e328c0e3aee4c8bcf/ead28259fc537a141af845c25aed363d.png",
                "image_type": "image",
                "name": "SPACE ID AMA II Badge",
                "attributes": [
                    {
                        "display_type": "string",
                        "trait_type": "animation_url",
                        "value": "",
                        "alias": "animation_url",
                        "format": "",
                        "same_trait": 0
                    },
                    {
                        "display_type": "string",
                        "trait_type": "background_color",
                        "value": "",
                        "alias": "background_color",
                        "format": "",
                        "same_trait": 0
                    },
                    {
                        "display_type": "date",
                        "trait_type": "birthday",
                        "value": "1656922994",
                        "alias": "birthday",
                        "format": "",
                        "same_trait": 1
                    },
                    {
                        "display_type": "string",
                        "trait_type": "category",
                        "value": "SPACE ID AMA II Badge",
                        "alias": "category",
                        "format": "",
                        "same_trait": 4871
                    },
                    {
                        "display_type": "string",
                        "trait_type": "owner",
                        "value": "0x3a2086aF88834dEd36e14374b1DA75E17a83BadA",
                        "alias": "owner",
                        "format": "",
                        "same_trait": 3
                    }
                ]
            }
        }



Transaction
-----------
Latest Transactions
+++++++++++++++++++
最近交易

.. http:get:: /transactions

    :query int chainId: support [56, 1, 137].
    :query int pageNo: *optional* page No, 1 to ...
    :query int pageSize: *optinal* page size

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl -XGET "curl -XGET "https://api-mainnet.treasurelands.xyz/transactions?chainId=137"

        .. code-tab:: python

            import requests
            URL = 'https://api-mainnet.treasurelands.xyz/transactions?chainId=137'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
            "code": 0,
            "message": "Success",
            "data": {
                "list": [
                    {
                        "orderId": 68651,
                        "chainId": 1,
                        "contract": "0x60f80121c31a0d46b5279700f9df786054aa5ee5",
                        "tokenId": "1143929",
                        "name": "Bitlux",
                        "resource": "images/eth/0x60f80121c31a0d46b5279700f9df786054aa5ee5/47ae8dfc40beb323c600f4935c991cea.jpeg",
                        "resourceType": "image",
                        "maker": "0xc7d5436e719820ab757772d0017d4a279f1cab4b",
                        "taker": "0xe2d4c2df272422c66ad8ae1dedcbd0148ecadca3",
                        "side": 1,
                        "price": "25000000000000000",
                        "erc20": "0x0000000000000000000000000000000000000000",
                        "title": "",
                        "symbol": "ETH",
                        "decimals": 18,
                        "showDecimals": 4
                    },
                    {
                        "orderId": 68648,
                        "chainId": 1,
                        "contract": "0x60f80121c31a0d46b5279700f9df786054aa5ee5",
                        "tokenId": "1148117",
                        "name": "Don   t..... bE..... SaD",
                        "resource": "images/eth/0x60f80121c31a0d46b5279700f9df786054aa5ee5/87656310f34fa4b65638b808ccec3d85.jpeg",
                        "resourceType": "image",
                        "maker": "0xc7d5436e719820ab757772d0017d4a279f1cab4b",
                        "taker": "0xd928731bae119cf71e5817621fc073dfa1e57afd",
                        "side": 1,
                        "price": "50000000000000000",
                        "erc20": "0x0000000000000000000000000000000000000000",
                        "title": "",
                        "symbol": "ETH",
                        "decimals": 18,
                        "showDecimals": 4
                    },
                    {
                        "orderId": 376250,
                        "chainId": 1,
                        "contract": "0xef5236aaa9c5ac41db844fade25f7a6b5a3b80fb",
                        "tokenId": "424004407781418698419329739917407005780345667133",
                        "name": "test sosss",
                        "resource": "images/eth/0xef5236aaa9c5ac41db844fade25f7a6b5a3b80fb/9f9209de30b788f45aac25d062d1df64",
                        "resourceType": "image",
                        "maker": "0x4a4503e52d510f049093376dbee4febbcf51e24f",
                        "taker": "0x8ce0b3905172c58bf96f73712c6de020681ca30a",
                        "side": 1,
                        "price": "10000000000000000000",
                        "erc20": "0x3b484b82567a09e2588a13d54d032153f0c0aee0",
                        "title": "",
                        "symbol": "SOS",
                        "decimals": 18,
                        "showDecimals": 2
                    },
                    {
                        "orderId": 363802,
                        "chainId": 1,
                        "contract": "0xdc35bf4c06ce5b43a0082b8f84e92d03abfb1060",
                        "tokenId": "340630",
                        "name": "D-VERSE: Mage #340630",
                        "resource": "images/eth/0xdc35bf4c06ce5b43a0082b8f84e92d03abfb1060/e3d6b88ace04159018f7ef417869c6ed.png",
                        "resourceType": "image",
                        "maker": "0x47597e3f4e32157fd75b13ea6c017226d3f4c7aa",
                        "taker": "0x92a617b7991853f6c2a3a0d0aa8c7b8b5d7b3a76",
                        "side": 1,
                        "price": "100000000000000000",
                        "erc20": "0x0000000000000000000000000000000000000000",
                        "title": "",
                        "symbol": "ETH",
                        "decimals": 18,
                        "showDecimals": 4
                    },
                    {
                        "orderId": 311439,
                        "chainId": 1,
                        "contract": "0xdc35bf4c06ce5b43a0082b8f84e92d03abfb1060",
                        "tokenId": "366630",
                        "name": "D-VERSE: Farmer #366630",
                        "resource": "images/eth/0xdc35bf4c06ce5b43a0082b8f84e92d03abfb1060/cd8639a46d14b77e30d60dd1e6c115cd.png",
                        "resourceType": "image",
                        "maker": "0xf2b8c4f7d1025a495e52765eb05e90c4a1c9ba3b",
                        "taker": "0x5db6291455a6491ff9bd5460bc34655984e23a75",
                        "side": 1,
                        "price": "100000000000000000",
                        "erc20": "0x0000000000000000000000000000000000000000",
                        "title": "",
                        "symbol": "ETH",
                        "decimals": 18,
                        "showDecimals": 4
                    },
                    {
                        "orderId": 63478,
                        "chainId": 1,
                        "contract": "0x0966a53f2533eaf01d0bb2fa0e2274f3002287f1",
                        "tokenId": "2382",
                        "name": "El Doggie Doble",
                        "resource": "images/eth/0x0966a53f2533eaf01d0bb2fa0e2274f3002287f1/800fd28681eb971a98c11a54109e31c7.png",
                        "resourceType": "image",
                        "maker": "0xd8099dc17bbd7d95f8f8781f47e96e9e87b73256",
                        "taker": "0x5d306c15447fc924b3d0834beb7363180780a7d8",
                        "side": 1,
                        "price": "8213000000000000",
                        "erc20": "0x0000000000000000000000000000000000000000",
                        "title": "",
                        "symbol": "ETH",
                        "decimals": 18,
                        "showDecimals": 4
                    },
                    {
                        "orderId": 65787,
                        "chainId": 1,
                        "contract": "0xb41d60df81a633ebdcb1de5ce3807c4aed5e72af",
                        "tokenId": "638820188435824583259866851756326362127409650148",
                        "name": "v",
                        "resource": "images/eth/0xb41d60df81a633ebdcb1de5ce3807c4aed5e72af/c318c0fa0e51c058c37e42b3bf0b4ea8",
                        "resourceType": "image",
                        "maker": "0x6fe5b01ebe6d1de59ee0d992ffdd5c3e4a8b8c4e",
                        "taker": "0x2493d4da050973cdd9a9a709984c7f7a99e418da",
                        "side": 1,
                        "price": "10000000000000",
                        "erc20": "0x0000000000000000000000000000000000000000",
                        "title": "",
                        "symbol": "ETH",
                        "decimals": 18,
                        "showDecimals": 4
                    }
                ],
                "pageNo": 1,
                "pageSize": 7,
                "total": 14
            }
        }

NFT Transaction
+++++++++++++++
NFT交易历史

.. http:get:: /transactions/tokens

    :query int chainId: support [56, 1, 137].
    :query string contract: contract address
    :query string tokenId: tokenId
    :query int pageNo: *optional* page No, 1 to ...
    :query int pageSize: *optinal* page size

    **Example request**:

    .. tabs::

        .. code-tab:: bash

            $ curl -XGET "curl -XGET "https://api-mainnet.treasurelands.xyz/transactions/tokens?chainId=56&contract=0x9f0225d5c92b9cee4024f6406c4f13e546fd91a8&tokenId=13656&pageSize=10&pageNo=1"

        .. code-tab:: python

            import requests
            URL = 'https://api-mainnet.treasurelands.xyz/transactions/tokens?chainId=56&contract=0x9f0225d5c92b9cee4024f6406c4f13e546fd91a8&tokenId=13656&pageSize=10&pageNo=1'
            response = requests.get(URL)
            print(response.json())

    **Example response**:

    .. sourcecode:: json

        {
            "code": 0,
            "message": "Success",
            "data": {
                "total": 3,
                "list": [
                    {
                        "blockNumber": 19518159,
                        "logIndex": 262,
                        "txHash": "0xd35765780fdcbba28acb4a929475a0c95e264771d3a008f35198bafd202373b4",
                        "timestamp": 0,
                        "from": "0x32b0d2e57cba72e5eaccdc8d584e30d4b159194f",
                        "to": "0xd210d19d3670e5ec621c419f57c32dc5aa6cd511",
                        "type": "Sale",
                        "price": "20000000000000000",
                        "symbol": "BNB",
                        "decimals": 18,
                        "showDecimals": 4
                    },
                    {
                        "blockNumber": 19518159,
                        "logIndex": 261,
                        "txHash": "0xd35765780fdcbba28acb4a929475a0c95e264771d3a008f35198bafd202373b4",
                        "timestamp": 1657725936,
                        "from": "0x32b0d2e57cba72e5eaccdc8d584e30d4b159194f",
                        "to": "0xd210d19d3670e5ec621c419f57c32dc5aa6cd511",
                        "type": "Transfer",
                        "price": "",
                        "symbol": "",
                        "decimals": 0,
                        "showDecimals": 0
                    },
                    {
                        "blockNumber": 8604144,
                        "logIndex": 109,
                        "txHash": "0x73a62a0781136c091cf4aec2dcd795422c5a1c62c29775912943a90f6ba637f4",
                        "timestamp": 0,
                        "from": "0x0000000000000000000000000000000000000000",
                        "to": "0x32b0d2e57cba72e5eaccdc8d584e30d4b159194f",
                        "type": "Create",
                        "price": "",
                        "symbol": "",
                        "decimals": 0,
                        "showDecimals": 0
                    }
                ],
                "pageSize": 10,
                "pageNo": 1
            }
        }
