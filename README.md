```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

// Store a single data point and allow fetching/updating of that datapoint
contract Hello {

    // data point
    string public storedData;

    // counter for updates
    uint public updateCount;

    // event to emit the updated data
    event myEventTest(string eventOutput);

    // store a new value and emit the event
    function set(string memory myText) public {
        storedData = myText;
        updateCount++; // increment the counter
        emit myEventTest(myText);
    }

    // retrieve the stored value
    function get() public view returns (string memory) {
        return storedData;
    }
}
