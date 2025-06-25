solidity
pragma solidity ^0.8.9;

contract Hello {
    string public storedData;
    uint public updateCount;
    event myEventTest(string eventOutput);
    function set(string memory myText) public {
        storedData = myText;
        updateCount++;
        emit myEventTest(myText);
    }
    function get() public view returns (string memory) {
        return storedData;
    }
}
