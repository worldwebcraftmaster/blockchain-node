About the project

NodeJs - Http - Implementation of basic Blockchain
This project is basic implentation of Blockchain in NodeJs for people who are struggling hard to understand What Blockchain is basically.

How to download and start the project?

$ git clone https://github.com/worldwebcraftmaster/blockchain-node.git
$ cd blockchain-node
$ npm install
$ node index.js 3000 

By default port no. is 3000. So you should see server running at http://localhost:3000/
You can test http functions with postman.
If you aren’t using Postman, then you can make the equivalent request using cURL:
$ curl -X POST -H "Content-Type: application/json" -d '{
"sender": "d4ee26eee15148ee92c6cd394edd974e",
"recipient": "someone-other-address",
"amount": 5
}' "http://localhost:3000/transactions/new"

###Endpoints

/blockchain/transactions/new [POST] - Add a new transaction

JSON data to be posted.

{
"sender": "d4ee26eee15148ee92c6cd394edd974e",
"recipient": "someone-other-address",
"amount": 5
}

/blockchain/mine [GET] - Mine a new Block
/blockchain/chain [GET] - Get Full chain
/blockchain/nodes/register [POST] - Register a new node in the blockchain network

JSON data to be posted.

{
"nodes":["http://127.0.0.1:3001"]
}

/blockchain/nodes/resolve [GET] - Resolve Conflict among nodes in the network

Future Plans
Adding Database Support
