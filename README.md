# Swisstronik Testnet 2.0 - Mint ERC-20 Tokens.

Link : [Click!](https://www.swisstronik.com/testnet2/dashboard)

Swisstronik Testnet Address

```
0xE9b0493B3A058E467FFAA1c57b7b5DFD80d40C0d
```

## Steps

### 1. Clone Repository

```bash
git clone https://github.com/skepticola/swisstronik-erc20-mint-token.git
```

```
cd swisstronik-erc20-mint-token
```

### 2. Install Dependency

```bash
npm install
```

### 3. Set .env File

create .env file in root project

```bash
touch .env
```

add this to your .env file
```bash
PRIVATE_KEY="your private key"
```

### 4. Create Smart Contract

- Open contract folder
- Create Token.sol file
- Copy this code and paste there
- Feel free to modify token name and token symbol

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract TestToken is ERC20 {
    constructor()ERC20("Phantom","PHTM"){}

    function mint1000tokens() public {
        _mint(msg.sender,1000*10**18);
    }

    function burn1000tokens() public{
        _burn(msg.sender,1000*10**18);
    }

}
```

### 5. Compile Smart Contract

```bash
npm run compile
```

### 6. Deploy Smart Contract

```bash
npm run deploy
```

### 7. Mint Token

```bash
npm run mint
```

### 8. Check Supply

```bash
npm run check-supply
```

### 9. Check Balance

```bash
npm run balance-of
```

### 10. Tranfer Token

```bash
npm run transfer
```

### Finished.
