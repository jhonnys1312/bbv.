# ViteX Operators Submission Guideline

## Requirements

### Information Preparation

Prepare submission documents under the following requirements.

`LOGO IMAGE`

- Image format: `png`
- Image size: `200x200 pixels`

![Icon Specification](../assets/images/icon-specification.jpg)

`JSON FILE`

| field | value required |description | schema type |
|:------------:|:-----:|:-----------:|:-----:|
| name | necessary | gateway name | String |
| address | necessary | owner of the trade pairs | String |
| overview | necessary | introduction of your token | Map<String,String> |
| links | necessary | website, whitepaper, github, and other media links | Map<String,List<String>> |
| support | necessary | customer service can be provided through Discord or Telegram | String |

> Filename should be your operator address in all `lowercase` letters, same name for both .json and .png (Including capitalization), eg: vite_050697d3810c30816b005a03511c734c1159f50907662b046f

#### Keyword in the field  Map-Value above.

* `links`

    * **website** 
    * **whitepaper** 
    * **github** 
    * explorer
    * email
    * twitter
    * facebook
    * reddit
    * instagram
    * steemit
    * coinmarketcap
    * youtube
    * telegram
    * discord
    * linkedin
    * medium
    * blog

* `overview`
    
    * **en** 
    * zh

    > Note: Providing an English version is essential.

> Note: you must use the right key name, and all must be `lowercase`.


##### Example:

```json 
{
	"name":"Vite Labs",
  "address":"vite_050697d3810c30816b005a03511c734c1159f50907662b046f",
  "overview": {
    "zh": "Vite Labs作为ViteX的技术提供方，在ViteX上线后会以官方身份成为首个运营商，届时将会完成常见跨链币种的铸币工作，并开启相应的交易对。Vite Labs在ViteX诞生初期发挥一定作用；随着ViteX和其他运营商的发展，会弱化自己的运营商功能。",
    "en": "Vite Labs is a technology provider as well as the first operator of ViteX. Vite Labs will issue common cross-chain tokens and open corresponding trading pairs. Vite Labs will weaken its role as an operator after more participants become operators on ViteX platform."
  },
  "links": {
    "website":["https://vite.org"],
    "explorer":["https://explorer.vite.net"],
    "whitepaper":[
      "https://github.com/vitelabs/whitepaper/blob/master/vite_en.pdf",
      "https://github.com/vitelabs/whitepaper/blob/master/vite_cn.pdf"
    ]
  },
  "support":"gateway@vite.org",
  "gateway":"Vite Labs"
}

```

## Steps to upload

We recommend that you complete the procedures with your developers, or you can follow [Github Guideline](../github-tutorial.en.md) to operate on github web page.

1. Fork the repo to your own github account

2. Clone the repo from your own account, please note: do not clone the origin one directly, but clone the repo you forked
```
git clone https://github.com/[your-own-repo]/crypto-info.git
cd crypto-info/
```

3. Create a new branch (file) and switch to a new branch named by your operator address
  For example:
```
git branch operator-[vite_xxx]
git checkout operator-[vite_xxx]
```

4. Please ensure to use UTF-8 encoding in the json file to avoid Travis-CI build error. Please check the template file to fill in the complete operator information: [$template.json](../operators/$template.json)


5. Create the directory with the name of your operator address under the directory `operators` if not exist. Add your operator json file and logo image to the directory created, named by your operator address. 
  For example:
```
operators/vite_050697d3810c30816b005a03511c734c1159f50907662b046f/

vite_050697d3810c30816b005a03511c734c1159f50907662b046f.json
vite_050697d3810c30816b005a03511c734c1159f50907662b046f.png
```

7. Commit and push the information to your repo
  For example:
```
git add -A
git commit -m "add operator [Operator Name] [vite_xxx]"
git push origin operator-[vite_xxx]
```

8. Under your repo page, click the "New pull request" button. Then, attach the detailed operator information, this includes but not limited to the following: (Operator name; Operator address on vite blockchain; Contact information).

   Sample PR: https://github.com/vitelabs/crypto-info/pull/xxx

9. We will review your PR as soon as possible. If there is no problem with your PR, we will merge it into our master branch. And then your token profile will display in the current Vite App

