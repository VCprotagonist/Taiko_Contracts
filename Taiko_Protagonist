// SPDX-License-Identifier: MIT

pragma solidity ^0.8.0;


contract Taiko_Protagonist{

    address public owner;
    mapping (address => uint) public payments;

    constructor() {
        owner = msg.sender;
    }

    function DepositAssets() public payable {
        payments[msg.sender] = msg.value;
    }

    function WithdrawAssets() public {
        address payable _to = payable(owner);
        address _thisContract = address(this);
        _to.transfer(_thisContract.balance);
    }
}
