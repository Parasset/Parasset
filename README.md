# Parasset
使用去中心化的链上原生资产，如ETH、NToken，用于生成平行的资产。

![](https://img.shields.io/github/issues/Parasset/Parasset-Protocol)
![](https://img.shields.io/github/stars/Parasset/Parasset-Protocol)
![](https://img.shields.io/github/license/Parasset/Parasset-Protocol)
![](https://img.shields.io/twitter/url?url=https%3A%2F%2Fgithub.com%2FParasset%2FParasset-Protocol%2F)

![image](https://github.com/Parasset/Doc/blob/main/Parasset_Smart_Contracts2.png)

## 安装

```
1. npm init
2. npm install --save-dev hardhat
3. npx hardhat
```


## 编译合约

```
npx hardhat compile
```

## 部署

### Mainnet

```
npx hardhat run scripts/1_1_deployAndSetting_mainnet.js --network mainnet

```
#### v1.0-0430

合约 | 地址 | 描述
---|---|---
NestContract | 0x04abEdA201850aC0124161F037Efd70c74ddC74C | NEST Token合约
USDTContract | 0xdac17f958d2ee523a2206206994597c13d831ec7 | USDT Token 合约
PTokenFactory | 0x978f0038A69a0ecA925df4510e0085747744dDA8 | P资产工厂合约
MortgagePool | 0xd49bFB7e44E3E66a59b934D45CcBf9165AcE34b3 | 抵押池合约
InsurancePool | 0x46955ccEc435465C8C70BD64E2f5FFBd33308C8C | 保险池合约
PriceController | 0x2Ce14C65cD3cCC546433E3b1E8c712E102377635 | 价格调用合约
NTokenController | 0xc4f1690eCe0145ed544f0aee0E2Fa886DFD66B62 | NToken控制合约
NestQuery | 0xB5D2890c061c321A5B6A4a4254bb1522425BAF0A | NEST 价格合约
PUSDT | 0x9786bD44c30cD84Fc6C9b026c2e826De066F688c | PUSDT合约
PETH | 0x6319F81e8C5F5E20fD675bc484EdFbb7E121831a | PETH合约

### Ropsten

```
npx hardhat run scripts/1_deployAndSetting.js --network ropsten

```
#### V1.0

合约 | 地址 | 描述
---|---|---
NestContract | 0x1e481DA2B644d2E63b0aa36e3D6eFb8a802804CF | NEST Token合约
USDTContract | 0xfA3b8a37e941b8b3e83F0505A104a91330bd40Ba | USDT Token 合约
PTokenFactory | 0x260D92a64D24eCCE01db2013E060Af99aE95A4F0 | P资产工厂合约
MortgagePool | 0x99a57B75b968e73eec8D46eDCde5EC2998101f52 | 抵押池合约
InsurancePool | 0xc52027340De12037FC2A6865DdcD693011D3d8fe | 保险池合约
NestQuery | 0xa5993c159947390f0858A2dD1a887590AF1E20da | NEST 价格合约
PUSDT | 0xB5f515c6E6cbed73E21f3d1278b3265511a5d2fb | PUSDT合约
PETH | 0xFA189E7774325D172A0580C4523E98972c20c7e3 | PETH合约

#### V1.1

增加查询其他人债仓数据接口

合约 | 地址 | 描述
---|---|---
MortgagePool | 0x3A94F468ADC13F1715c094388417C599810f3ed9 | 抵押池合约
InsurancePool | 0x37b9F494ee29C9907684415681247FE3ec150ff0 | 保险池合约

#### V1.2

1. 增加价格调用合约
2. 修改抵押率展示方式
3. 增加P资产增发、销毁日志

价格：

2USDT=1ETH

3NEST=1ETH

合约 | 地址 | 描述
---|---|---
NestContract | 0xae6E04ED92FC12238852cA212f09b96Dc23407C1 | NEST Token合约
USDTContract | 0xEDfe846E914d0aaaA42aC031D2D5Fc5467E68a81 | USDT Token合约
PTokenFactory | 0x94914baE774EcAc54a29078F010ef7c588573f4d | P资产工厂合约
MortgagePool | 0xBFDFD8b3a95A4863ae00772d81A9d5Ff1894AF5E | 抵押池合约
InsurancePool | 0x610a0e22286C6408A2384D7Ff14a10B85C6d8E50 | 保险池合约
PriceController | 0xEBb7eEbC4DF86Ae5917FAD26A2B3464BB97e0C95 | 价格调用合约
NestQuery | 0x364b22983ed7EABb4de94924D7e17411FDE674Ae | NEST 价格合约
PUSDT | 0x1a8A52074932Af7333626a3e757524E3667D78C5 | PUSDT合约
PETH | 0x282f780533B748a256872E5855d3d84C3bf64Ac0 | PETH合约

#### V1.3

1. 增加抵押资产、减少铸币，抵押率不能低于0%
2. 铸币、减少抵押、新增铸币，抵押率小于等于70%
3. 增加返回地址列表，单条数据查询接口

价格：

2USDT=1ETH

3NEST=1ETH

保险赎回时间：10分钟赎回一次，每次赎回时间5分钟

合约 | 地址 | 描述
---|---|---
NestContract | 0xae6E04ED92FC12238852cA212f09b96Dc23407C1 | NEST Token合约
USDTContract | 0xEDfe846E914d0aaaA42aC031D2D5Fc5467E68a81 | USDT Token 合约
PTokenFactory | 0x94914baE774EcAc54a29078F010ef7c588573f4d | P资产工厂合约
MortgagePool | 0x73fc3699F2aD42Cb3ae8dB0F998B36E9BB784324 | 抵押池合约
InsurancePool | 0xf8246405404c59964206Fac834317f2f50b9a670 | 保险池合约
PriceController | 0xEBb7eEbC4DF86Ae5917FAD26A2B3464BB97e0C95 | 价格调用合约
NestQuery | 0x364b22983ed7EABb4de94924D7e17411FDE674Ae | NEST 价格合约
PUSDT | 0x1a8A52074932Af7333626a3e757524E3667D78C5 | PUSDT合约
PETH | 0x282f780533B748a256872E5855d3d84C3bf64Ac0 | PETH合约

#### V1.4

1. 增加保险返回上期赎回时间接口
2. 增加抵押池操作，手续费日志

价格：

2USDT=1ETH

3NEST=1ETH

保险赎回时间：10分钟赎回一次，每次赎回时间5分钟

合约 | 地址 | 描述
---|---|---
NestContract | 0xae6E04ED92FC12238852cA212f09b96Dc23407C1 | NEST Token合约
USDTContract | 0xEDfe846E914d0aaaA42aC031D2D5Fc5467E68a81 | USDT Token 合约
PTokenFactory | 0x94914baE774EcAc54a29078F010ef7c588573f4d | P资产工厂合约
MortgagePool | 0x16bCC9A1206A3cD3c4A11aBED4A73bae20aFA1aa | 抵押池合约
InsurancePool | 0xf1dfE5c3C0D2D26a721514f31BE02D90EE54D5B3 | 保险池合约
PriceController | 0xEBb7eEbC4DF86Ae5917FAD26A2B3464BB97e0C95 | 价格调用合约
NestQuery | 0x364b22983ed7EABb4de94924D7e17411FDE674Ae | NEST 价格合约
PUSDT | 0x1a8A52074932Af7333626a3e757524E3667D78C5 | PUSDT合约
PETH | 0x282f780533B748a256872E5855d3d84C3bf64Ac0 | PETH合约

#### V1.5

价格：

2USDT=1ETH

3NEST=1ETH

保险赎回时间：30分钟赎回一次，每次赎回时间15分钟

合约 | 地址 | 描述
---|---|---
NestContract | 0xae6E04ED92FC12238852cA212f09b96Dc23407C1 | NEST Token合约
USDTContract | 0xEDfe846E914d0aaaA42aC031D2D5Fc5467E68a81 | USDT Token 合约
PTokenFactory | 0x94914baE774EcAc54a29078F010ef7c588573f4d | P资产工厂合约
MortgagePool | 0x113F218D567ee2f4f92214CE9900Eb34789C17C0 | 抵押池合约
InsurancePool | 0xB0257E6aA1492e689C18671712CF80a1502aCe2E | 保险池合约
PriceController | 0xEBb7eEbC4DF86Ae5917FAD26A2B3464BB97e0C95 | 价格调用合约
NestQuery | 0x364b22983ed7EABb4de94924D7e17411FDE674Ae | NEST 价格合约
PUSDT | 0x1a8A52074932Af7333626a3e757524E3667D78C5 | PUSDT合约
PETH | 0x282f780533B748a256872E5855d3d84C3bf64Ac0 | PETH合约


#### V1.6

价格：

2USDT=1ETH

3NEST=1ETH

保险赎回时间：30分钟赎回一次，每次赎回时间15分钟

合约 | 地址 | 描述
---|---|---
NestContract | 0xae6E04ED92FC12238852cA212f09b96Dc23407C1 | NEST Token合约
USDTContract | 0xEDfe846E914d0aaaA42aC031D2D5Fc5467E68a81 | USDT Token 合约
PTokenFactory | 0x94914baE774EcAc54a29078F010ef7c588573f4d | P资产工厂合约
MortgagePool | 0x22d0E15Dc69d2e996d92eC3a576580C3756D5fb9 | 抵押池合约
InsurancePool | 0x242BCDd5E446b57CDeDA46E19343D1aAe8557Ee2 | 保险池合约
PriceController | 0xEBb7eEbC4DF86Ae5917FAD26A2B3464BB97e0C95 | 价格调用合约
NestQuery | 0x364b22983ed7EABb4de94924D7e17411FDE674Ae | NEST 价格合约
PUSDT | 0x1a8A52074932Af7333626a3e757524E3667D78C5 | PUSDT合约
PETH | 0x282f780533B748a256872E5855d3d84C3bf64Ac0 | PETH合约

#### V1.7

1. PUSDT,PETH，保险初始值为-100
2. 增加负账户操作改变日志

价格：

2USDT=1ETH

3NEST=1ETH

保险赎回时间：30分钟赎回一次，每次赎回时间15分钟

合约 | 地址 | 描述
---|---|---
NestContract | 0xae6E04ED92FC12238852cA212f09b96Dc23407C1 | NEST Token合约
USDTContract | 0xEDfe846E914d0aaaA42aC031D2D5Fc5467E68a81 | USDT Token 合约
PTokenFactory | 0x94914baE774EcAc54a29078F010ef7c588573f4d | P资产工厂合约
MortgagePool | 0x29cab865522dC14e5a1910a47DB979b841f5fDbA | 抵押池合约
InsurancePool | 0xc692cdDc5C920D6365DFa7bC31981cb77E172b43 | 保险池合约
PriceController | 0xEBb7eEbC4DF86Ae5917FAD26A2B3464BB97e0C95 | 价格调用合约
NestQuery | 0x364b22983ed7EABb4de94924D7e17411FDE674Ae | NEST 价格合约
PUSDT | 0x1a8A52074932Af7333626a3e757524E3667D78C5 | PUSDT合约
PETH | 0x282f780533B748a256872E5855d3d84C3bf64Ac0 | PETH合约

#### V1.8

1. 合约内部抵押率保留18位计算精度
2. PUSDT保险负账户为100，PETH正常

价格：

2USDT=1ETH

3NEST=1ETH

保险赎回时间：30分钟赎回一次，每次赎回时间15分钟

合约 | 地址 | 描述
---|---|---
NestContract | 0xae6E04ED92FC12238852cA212f09b96Dc23407C1 | NEST Token合约
USDTContract | 0xEDfe846E914d0aaaA42aC031D2D5Fc5467E68a81 | USDT Token 合约
PTokenFactory | 0x94914baE774EcAc54a29078F010ef7c588573f4d | P资产工厂合约
MortgagePool | 0x398F09004225AA8f6a0775829e9b993697E806E2 | 抵押池合约
InsurancePool | 0x0705C9bC1023edC418852a9957767a0359df1Bd9 | 保险池合约
PriceController | 0xEBb7eEbC4DF86Ae5917FAD26A2B3464BB97e0C95 | 价格调用合约
NestQuery | 0x364b22983ed7EABb4de94924D7e17411FDE674Ae | NEST 价格合约
PUSDT | 0x1a8A52074932Af7333626a3e757524E3667D78C5 | PUSDT合约
PETH | 0x282f780533B748a256872E5855d3d84C3bf64Ac0 | PETH合约

#### V1.9

修正合约审计中的问题

价格：

2USDT=1ETH

3NEST=1ETH

保险赎回时间：30分钟赎回一次，每次赎回时间15分钟

合约 | 地址 | 描述
---|---|---
NestContract | 0xd791228a2eeb931739A5faC4a41af55fA194E08E | NEST Token合约
USDTContract | 0x955702776C7624f3EF4B49d6900946ED4f403d9A | USDT Token 合约
PTokenFactory | 0xe635F9d3e3EFE67Ad42898F38d2E373270CD58c3 | P资产工厂合约
MortgagePool | 0x3048bC3cd8dbCE68c7b4E6D5E0c117bD2885322D | 抵押池合约
InsurancePool | 0xe0bc8c4f65f08ab71437bdA1f261d9E6A96A6F66 | 保险池合约
PriceController | 0x32ED66917687131f3852Fc64A638b8e8D9f3b5aa | 价格调用合约
NestQuery | 0xbF6dBeF11649fa1b55f850fd003ff4c3B4E5C025 | NEST 价格合约
PUSDT | 0xffaa58c0bc5069E19FcCa94aDb70EA63578F9860 | PUSDT合约
PETH | 0x64B100bDA18c2A5AF4A370547adaB2712Dcf41dD | PETH合约

### Rinkeby

#### V1.0

合约 | 地址 | 描述
---|---|---
NestContract | 0x5f24106d9768E2D124e16aF8713907c9F7Cf73F4 | NEST Token合约
USDTContract | 0x3d329E93491867B8B448862dC0A031D7b2046aC4 | USDT Token 合约
PTokenFactory | 0xF35Fda2a25C955c0362ee28b52261C91bc2D516d | P资产工厂合约
MortgagePool | 0x2b64031944149dF84ba8110A176DdE0F769B465c | 抵押池合约
InsurancePool | 0x2FF1A766C231E878b1c20ed91Ca57a29D0A91Cb6 | 保险池合约
PriceController | 0x272627AF55856c3aC9d4015146a57411Cdcf5f61 | 价格调用合约
NestQuery | 0x50C3c947Fc7A1ce4F51c514501B98D23232e416C | NEST 价格合约
PUSDT | 0x4db49cef7494960D65d838d4b4ea19b87919D225 | PUSDT合约
PETH | 0x57eE2A4Ee1454A9825c5664085bf402E5f574c80 | PETH合约

#### V1.1

参数设置：

nest抵押率上限40%，nest-k:1.333

ETH抵押率上限70%，ETH-k:1.25

合约 | 地址 | 描述
---|---|---
NestContract | 0xCC04e910083067d32370F1ac2C4Dea22c68a623a | NEST Token合约
USDTContract | 0x47860Cac0D3e10E3E2baa30F151E2b7051cA1816 | USDT Token 合约
PTokenFactory | 0x7f0E5E8f9Abe51c3C79B8fBE5b0Aa27987DB21d4 | P资产工厂合约
MortgagePool | 0x281eAdf15223889431f500f80B33079654b478f6 | 抵押池合约
InsurancePool | 0x16083A46Df5e719a55CB354a5F8b51284dA11217 | 保险池合约
PriceController | 0x172728B14b568548370CA975af214D04d3Ce4DB3 | 价格调用合约
NestQuery | 0x0F91E433D1e7B94dAd0B341CEc4e71D5BEA57836 | NEST 价格合约
PUSDT | 0x89b8C4a0c908C18F846A03B1dFE7699Bda809A47 | PUSDT合约
PETH | 0x108E0bb98c6BBED7ddDfe8d339a17cabD5c99673 | PETH合约

#### V1.2

参数设置：

nest抵押率上限40%，nest清算线:75%

ETH抵押率上限70%，ETH清算线:84%

价格：

2USDT=1ETH

3NEST=1ETH

保险赎回时间：30分钟赎回一次，每次赎回时间15分钟

合约 | 地址 | 描述
---|---|---
NestContract | 0x52805f9C36E7F9eC6390DCB51f7fB8Cc1575A85e | NEST Token合约
USDTContract | 0xC4FC237b2BB407d14ce925F70063Ef7312A336B6 | USDT Token 合约
PTokenFactory | 0x5C6aa34708a1c7F9D40aF15C9FAD54B6aFaaEc8D | P资产工厂合约
MortgagePool | 0x509F84D973B2C75fD62a8454d80575fF89FDe3d4 | 抵押池合约
InsurancePool | 0xf4B0b23Fe4C0F21c627a7f94E6F2A0d08694B8Db | 保险池合约
PriceController | 0xAcc44E0F32766174B3BE4Fc1735EeCAe9E74287B | 价格调用合约
NTokenController | 0xeA77d90E3B54CbF6ED1053Ec60680Fa223deb4cf | NToken控制合约
NestQuery | 0x11Cf802193Ae6167622b0c68007882A0D90B7642 | NEST 价格合约
PUSDT | 0xBf1710D43C3BdC50195c15019F48DC5c1f065806 | PUSDT合约
PETH | 0x039D3f87F90Ec6F1fc73467c396093418ece53aC | PETH合约

### .private.json

>将sample.private.json更名为.private.json

```
{
    //  infura节点私钥
    "alchemy": {
        "ropsten": {
            "apiKey": "XXX"
        },
        "mainnet": {
            "apiKey": "XXX"
        }
    },
    //  填写私钥
    "account": {
        "ropsten": {
            "key": "XXX",
            "userA": "XXX",
            "userB": "XXX"
        },
        "mainnet": {
            "key": "XXX",
            "userA": "XXX",
            "userB": "XXX"
        }
    }
}
```





