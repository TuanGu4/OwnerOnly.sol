# OwnerOnly.sol
OwnerOnly.sol6
pragma solidity ^0.8.20;

contract OwnerOnly {
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    function changeOwner(address _newOwner) public {
        require(msg.sender == owner, "Not owner");
        owner = _newOwner;
    }
}
Add new function
Add comments for clarity
Improve naming consistency
