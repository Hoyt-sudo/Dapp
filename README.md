https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.26+commit.8a97fa7a.js

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "hardhat/console.sol";

contract paynow{
    address payer;
    address payee;
    uint amount;
    address owner;

    constructor(){
        owner=msg.sender;
        console.log(owner);

    }

    function weixin(address payer_add, address payee_add, uint pay_amount) public{
        payer=payer_add;
        payee=payee_add;
        amount=pay_amount;

        console.log(payer,payee,amount);
    }

    function transaction() public view returns(address,address,uint){
        return (payer,payee,amount);
    }

}
