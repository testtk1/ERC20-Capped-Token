# ERC20-Capped-Token
ERC20 Capped Token
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/extensions/ERC20Capped.sol";

contract CappedToken is ERC20Capped {
    constructor() ERC20("CappedToken", "CAP") ERC20Capped(10000 ether) {
        _mint(msg.sender, 1000 ether);
    }
}
