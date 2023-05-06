# Lab 10 - Blockchain
##

### Hash function with randomization
```
PS C:\Users\stoll\demo> cd ..
PS C:\Users\stoll> cd ~/iot/lesson10
PS C:\Users\stoll\iot\lesson10> cat hash_value.py
"""
https://docs.python.org/3/using/cmdline.html#envvar-PYTHONHASHSEED
If PYTHONHASHSEED is not set or set to random, a random value is used to to seed the hashes of str and bytes objects.
If PYTHONHASHSEED is set to an integer value, it is used as a fixed seed for generating the hash() of the types covered by the hash randomization.
Its purpose is to allow repeatable hashing, such as for selftests for the interpreter itself, or to allow a cluster of python processes to share hash values.
The integer must be a decimal number in the range [0,4294967295]. Specifying the value 0 will disable hash randomization.

https://www.programiz.com/python-programming/methods/built-in/hash
hash(object) returns the hash value of the object (if it has one). Hash values are integers.
They are used to quickly compare dictionary keys during a dictionary lookup.
Numeric values that compare equal have the same hash value even if they are of different types, as is the case for 1 and 1.0.
For objects with custom __hash__() methods, note that hash() truncates the return value based on the bit width of the host machine.
"""

# hash for integer unchanged
print('The hash for 1 is:', hash(1))

# hash for decimal
print('The hash for 1.0 is:',hash(1.0))
print('The hash for 3.14 is:',hash(3.14))

# hash for string
print('The hash for Python is:', hash('Python'))

# hash for a tuple of vowels
vowels = ('a', 'e', 'i', 'o', 'u')
print('The hash for a tuple of vowels is:', hash(vowels))

# hash for a custom object
class Person:
    def __init__(self, age, name):
        self.age = age
        self.name = name
    def __eq__(self, other):
        return self.age == other.age and self.name == other.name
    def __hash__(self):
        return hash((self.age, self.name))
person = Person(23, 'Adam')
print('The hash for an object of person is:', hash(person))
PS C:\Users\stoll\iot\lesson10> python hash_value.py
The hash for 1 is: 1
The hash for 1.0 is: 1
The hash for 3.14 is: 322818021289917443
The hash for Python is: 1531921225379861865
The hash for a tuple of vowels is: -3192169221345398755
The hash for an object of person is: -7688038485456416502
PS C:\Users\stoll\iot\lesson10> python hash_value.py
The hash for 1 is: 1
The hash for 1.0 is: 1
The hash for 3.14 is: 322818021289917443
The hash for Python is: 4816873514519561402
The hash for a tuple of vowels is: -3143580892267017068
The hash for an object of person is: -1912593758526960275
PS C:\Users\stoll\iot\lesson10>
```

### snakecoin.py
```
PS C:\Users\stoll\iot\lesson10> python snakecoin.py
Block #1 has been added to the blockchain!
Hash: 61263c1a90736733e0106aae7756f8199aaffb79c9984a549da8260e7e57da8a

Block #2 has been added to the blockchain!
Hash: cabc279406c4bef38ff3862021fa759d38d2929c9c25e7562881479855478225

Block #3 has been added to the blockchain!
Hash: 14ea723e0b8b396ed7e38bed3ed967486e124bcd4fe7dd801cac9d50d06105b8

Block #4 has been added to the blockchain!
Hash: 37520c3715cd125e8e8af066d94f41e6372889f2d37e4ba5e2a92a72b61a6bb0

Block #5 has been added to the blockchain!
Hash: 222ddd83c6f7958070a62393b37e1c70becfd559f5ba924b7b7df9fe73fb0508

Block #6 has been added to the blockchain!
Hash: c3c4dacb4c392b531104953d813b19fe6d15c44d34cc33567353ea1309d536b7

Block #7 has been added to the blockchain!
Hash: 8b591c6d269765543e8febee26a8e22ba309910d767ad4093fc7701904ce735a

Block #8 has been added to the blockchain!
Hash: d0e7bf7214e56e66cb0bad4d7190d345dd4f7bc61801cbd3c316d07f4fe56418

Block #9 has been added to the blockchain!
Hash: fb98230e871c62472ea04c506db1452d102975bb423894b012fbe67cdac063c9

Block #10 has been added to the blockchain!
Hash: 7c7264a0a6eae59a54d7cb0c2852b74fb80b374e9735cde76e635db18ee76b67

Block #11 has been added to the blockchain!
Hash: bdc24ae1ef87fabc3c1dea1a7d5ff25918d497a4346cc0032d00dbcbd4352894

Block #12 has been added to the blockchain!
Hash: 121abda6692a17ce52c143e0338e78b8cf6fea1b96820b3300201226aaed1ccc

Block #13 has been added to the blockchain!
Hash: a71bc7ff505c2d233ebe3a81bcb3800ac583b6d46cac9f0f430ddb7e309aa272

Block #14 has been added to the blockchain!
Hash: a3cd9f9e3079470ef0be7f0cab45047b40943d19784025fa9c2c41dd6c317d85

Block #15 has been added to the blockchain!
Hash: 8af41eb59337e2feee8ea6bedd12eb9c19d7eed0bff375c5e3d02e462b29b71f

Block #16 has been added to the blockchain!
Hash: fba4e2352ea1d55fc97ab81249f3c74601234c1d64ce6e39bcab6ffb52c7f7ba

Block #17 has been added to the blockchain!
Hash: 95f5cd8e0fc554e3d9241d18db80f961f234923ecf0480556c76af2723afb0b0

Block #18 has been added to the blockchain!
Hash: 78191e444a089badeb8027580cb0ca19de5608deedc162c3275e67ccd3d093bf

Block #19 has been added to the blockchain!
Hash: 61d0f184a8f9c041b8e70f7b3c8ecee4b9ad0f5e80a42cd30c56b5c77b09ddc6

Block #20 has been added to the blockchain!
Hash: 90b0375f268b4897a1807b2c95bf54773a0f4797080f02fc1de421b3cc2e7984
```

### cat snakecoin-server-full-code.py
```
PS C:\Users\stoll\iot\lesson10> cat snakecoin-server-full-code.py
# Gerald Nash, "Letâ€™s Make the Tiniest Blockchain Bigger Part 2: With More Lines of Python"
# Referred to https://www.pythonanywhere.com/forums/topic/12382/ that fixed sha.update() TypeError: Unicode-objects must be encoded before hashing
# Running on http://127.0.0.1:5000/mine (Reload the page to mine and press CTRL+C to quit)
from flask import Flask
from flask import request
import json
import requests
import hashlib as hasher
import datetime as date
from flask import send_from_directory
import os
node = Flask(__name__)

# Define what a Snakecoin block is
class Block:
  def __init__(self, index, timestamp, data, previous_hash):
    self.index = index
    self.timestamp = timestamp
    self.data = data
    self.previous_hash = previous_hash
    self.hash = self.hash_block()

  def hash_block(self):
    sha = hasher.sha256()
#    sha.update(str(self.index) + str(self.timestamp) + str(self.data) + str(self.previous_hash))
    sha.update((str(self.index) + str(self.timestamp) + str(self.data) + str(self.previous_hash)).encode("utf-8"))
    return sha.hexdigest()

# Generate genesis block
def create_genesis_block():
  # Manually construct a block with
  # index zero and arbitrary previous hash
  return Block(0, date.datetime.now(), {
    "proof-of-work": 9,
    "transactions": None
  }, "0")

# A completely random address of the owner of this node
miner_address = "q3nf394hjg-random-miner-address-34nf3i4nflkn3oi"
# This node's blockchain copy
blockchain = []
blockchain.append(create_genesis_block())
# Store the transactions that
# this node has in a list
this_nodes_transactions = []
# Store the url data of every
# other node in the network
# so that we can communicate
# with them
peer_nodes = []
# A variable to deciding if we're mining or not
mining = True

@node.route("/")
def hello():
    return "SnakeCoin Server"

@node.route('/favicon.ico')
def favicon():
    return send_from_directory(os.path.join(node.root_path, 'static'),
                               'favicon.ico',
                               mimetype='image/vnd.microsoft.icon')

@node.route('/txion', methods=['POST'])
def transaction():
  # On each new POST request,
  # we extract the transaction data
  new_txion = request.get_json()
  # Then we add the transaction to our list
  this_nodes_transactions.append(new_txion)
  # Because the transaction was successfully
  # submitted, we log it to our console
  print("New transaction")
  print(("FROM: {}".format(new_txion['from'].encode('ascii','replace'))))
  print(("TO: {}".format(new_txion['to'].encode('ascii','replace'))))
  print(("AMOUNT: {}\n".format(new_txion['amount'])))
  # Then we let the client know it worked out
  return "Transaction submission successful\n"

@node.route('/blocks', methods=['GET'])
def get_blocks():
  chain_to_send = blockchain
  # Convert our blocks into dictionaries
  # so we can send them as json objects later
  for i in range(len(chain_to_send)):
    block = chain_to_send[i]
    block_index = str(block.index)
    block_timestamp = str(block.timestamp)
    block_data = str(block.data)
    block_hash = block.hash
    chain_to_send[i] = {
      "index": block_index,
      "timestamp": block_timestamp,
      "data": block_data,
      "hash": block_hash
    }
  chain_to_send = json.dumps(chain_to_send)
  return chain_to_send

def find_new_chains():
  # Get the blockchains of every
  # other node
  other_chains = []
  for node_url in peer_nodes:
    # Get their chains using a GET request
    block = requests.get(node_url + "/blocks").content
    # Convert the JSON object to a Python dictionary
    block = json.loads(block)
    # Add it to our list
    other_chains.append(block)
  return other_chains

def consensus():
  # Get the blocks from other nodes
  other_chains = find_new_chains()
  # If our chain isn't longest,
  # then we store the longest chain
  longest_chain = blockchain
  for chain in other_chains:
    if len(longest_chain) < len(chain):
      longest_chain = chain
  # If the longest chain isn't ours,
  # then we stop mining and set
  # our chain to the longest one
  blockchain = longest_chain

def proof_of_work(last_proof):
  # Create a variable that we will use to find
  # our next proof of work
  incrementor = last_proof + 1
  # Keep incrementing the incrementor until
  # it's equal to a number divisible by 9
  # and the proof of work of the previous
  # block in the chain
  while not (incrementor % 9 == 0 and incrementor % last_proof == 0):
    incrementor += 1
  # Once that number is found,
  # we can return it as a proof
  # of our work
  return incrementor

@node.route('/mine', methods = ['GET'])
def mine():
  # Get the last proof of work
  last_block = blockchain[len(blockchain) - 1]
  last_proof = last_block.data['proof-of-work']
  # Find the proof of work for
  # the current block being mined
  # Note: The program will hang here until a new
  #       proof of work is found
  proof = proof_of_work(last_proof)
  # Once we find a valid proof of work,
  # we know we can mine a block so
  # we reward the miner by adding a transaction
  this_nodes_transactions.append(
    { "from": "network", "to": miner_address, "amount": 1 }
  )
  # Now we can gather the data needed
  # to create the new block
  new_block_data = {
    "proof-of-work": proof,
    "transactions": list(this_nodes_transactions)
  }
  new_block_index = last_block.index + 1
  new_block_timestamp = this_timestamp = date.datetime.now()
  last_block_hash = last_block.hash
  # Empty transaction list
  this_nodes_transactions[:] = []
  # Now create the
  # new block!
  mined_block = Block(
    new_block_index,
    new_block_timestamp,
    new_block_data,
    last_block_hash
  )
  blockchain.append(mined_block)
  # Let the client know we mined a block
  return json.dumps({
      "index": new_block_index,
      "timestamp": str(new_block_timestamp),
      "data": new_block_data,
      "hash": last_block_hash
  }) + "\n"

node.run()
```

### Run snakecoin-server-full-code.py
```
PS C:\Users\stoll\iot\lesson10> python snakecoin-server-full-code.py
 * Serving Flask app 'snakecoin-server-full-code'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on http://127.0.0.1:5000
Press CTRL+C to quit
New transaction
FROM: b'akjflw'
TO: b'fjlakdj'
AMOUNT: 3

127.0.0.1 - - [06/May/2023 16:22:27] "POST /txion HTTP/1.1" 200 -
127.0.0.1 - - [06/May/2023 16:22:48] "GET /mine HTTP/1.1" 200 -


Terminal 2:
PS C:\Users\stoll\iot\lesson10> Invoke-RestMethod "http://localhost:5000/txion" -ContentType 'application/json' -Method Post -Body '{"from": "akjflw", "to":"fjlakdj", "amount": 3}'
Transaction submission successful

PS C:\Users\stoll\iot\lesson10>  Invoke-RestMethod "http://localhost:5000/mine"

index timestamp                  data
----- ---------                  ----
    1 2023-05-06 16:22:48.162890 @{proof-of-work=18; t...

```
![image](https://user-images.githubusercontent.com/98097869/236645025-7dfb1422-dd6e-40ab-8ac8-45ed4bafe29f.png)

I had some issues with running the code, but I looked it up and discussed with my peers and I figured out that I needed to run a different version of the code. 

### Running the Blockchain App

```
Terminal 1:
PS C:\Users\stoll> git clone https://github.com/satwikkansal/python_blockchain_app.git
Cloning into 'python_blockchain_app'...
remote: Enumerating objects: 173, done.
remote: Counting objects: 100% (72/72), done.
remote: Compressing objects: 100% (28/28), done.
Receiving objectsremote: Total 173 (delta 52), reused 56 (delta 43), pack-reused 101
Receiving objects: 100% (173/173), 230.00 KiB | 1.19 MiB/s, done.
Resolving deltas: 100% (84/84), done.
PS C:\Users\stoll> cd ~/python_blockchain_app
PS C:\Users\stoll\python_blockchain_app> nano node_server.py
PS C:\Users\stoll\python_blockchain_app> python node_server.py
 * Serving Flask app 'node_server'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on http://127.0.0.1:8000
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 973-954-183
127.0.0.1 - - [06/May/2023 16:31:02] "GET / HTTP/1.1" 404 -
127.0.0.1 - - [06/May/2023 16:31:02] "GET /favicon.ico HTTP/1.1" 404 -
127.0.0.1 - - [06/May/2023 16:31:14] "GET / HTTP/1.1" 404 -
127.0.0.1 - - [06/May/2023 16:31:16] "GET / HTTP/1.1" 404 -
127.0.0.1 - - [06/May/2023 16:32:58] "GET /chain HTTP/1.1" 200 -

Terminal 2:
PS C:\Users\stoll> cd ~/python_blockchain_app
PS C:\Users\stoll\python_blockchain_app>
PS C:\Users\stoll\python_blockchain_app> python run_app.py
 * Serving Flask app 'app'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on http://127.0.0.1:5000
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 973-954-183
127.0.0.1 - - [06/May/2023 16:32:58] "GET / HTTP/1.1" 200 -
127.0.0.1 - - [06/May/2023 16:32:58] "GET /favicon.ico HTTP/1.1" 404 -
```

![image](https://user-images.githubusercontent.com/98097869/236645595-f656a87c-2a35-4b7b-a5ec-3807ed300a26.png)

![image](https://user-images.githubusercontent.com/98097869/236645641-11baa086-f720-47b0-8be7-dc947833bb3f.png)

![image](https://user-images.githubusercontent.com/98097869/236645674-18ffffe2-9245-4da5-a1ab-bc253d8a79e2.png)
