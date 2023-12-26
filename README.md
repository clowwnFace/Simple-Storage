# My First Solidity Smart Contract: SimpleStorage

I'm proud to present my first Solidity smart contract, crafted using Solidity and Foundry. This simple yet impactful contract allows users to store and retrieve their favorite numbers on the blockchain, along with the option to add persons to the contract.

## Contract Functions


```solidity
function store(uint256 _favoriteNumber) public {
    myFavoriteNumber = _favoriteNumber;
}

function retrieve() public view returns (uint256) {
    return myFavoriteNumber;
}

function addPerson(string memory _name, uint256 _favoriteNumber) public {
        listOfPeople.push(Person(_favoriteNumber, _name));
        nameToFavoriteNumber[_name] = _favoriteNumber;
    }
```
### Deploy
```forge create SimpleStorage --private-key <PRIVATE_KEY> --rpc-url <ALCHEMY_URL>```

-REPLACE PRIVATE KEY WITH YOUR KEY AND THE ALCHEMY RPC URL

-THANKS

--FEEL FREE TO MODIFY THE CODE

author:clowwnFace
