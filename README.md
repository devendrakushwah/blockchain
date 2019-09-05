# Simple Blockchain implementation in python
 Simple python implementation of a blockchain and the API endpints created using flask.
 The implementation includes :
 * The blockchain structure
 * Proof of work algorithm
 * Endpoint to make transactions
 * Endpoint to mine blocks
 * Consensus algorithm to resolve conflicts
 
## Requirements
1. python 3.5+ 
2. pipenv 
3. flask 
4. requests

## Run the server:
* `pipenv run python blockchain.py -p 5001`
* `pipenv run python blockchain.py -p 5002`

## Endpoint
* `127.0.0.1:5000/nodes/resolve`
```json
{
    "chain": [
        {
            "index": 1,
            "previous_hash": "1",
            "proof": 100,
            "timestamp": 1567662531.29454,
            "transactions": []
        },
        {
            "index": 2,
            "previous_hash": "f320a6dac42a7e54ccbf97aa6ba9ea9d66cf02d79ea11918c8fdbc000a2619e5",
            "proof": 108178,
            "timestamp": 1567662840.2465315,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "2a0c758ae5de47b7b96338d26130b832",
                    "sender": "0"
                }
            ]
        },
        {
            "index": 3,
            "previous_hash": "dbf1211fb34b6c42da8b40b6c34fb15c472860411d1cff85e6a3a0beb9f6f43b",
            "proof": 84137,
            "timestamp": 1567662986.6913767,
            "transactions": [
                {
                    "amount": 1,
                    "recipient": "2a0c758ae5de47b7b96338d26130b832",
                    "sender": "0"
                }
            ]
        }
    ],
    "message": "Our chain is authoritative"
}```
