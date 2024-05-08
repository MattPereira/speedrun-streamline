A collection of examples for learning how to wield the power of streamline

## BuidlGuidl Sanctum Cohort

#### 1. What is the data we are working with?

Contract Address

```
0xA90F607224A0236B08Ae02178AB57aef712f86D3
```

Target Event

```
event Withdraw(address indexed to, uint256 amount, string reason);
```

#### 2. What data do we want to find?

The total withdraw amounts for each EOA that has withdrawn from this contract.

#### 3. How to get from input->output?

Given a list of Withdraw Events, sum the `amounts` for each `to` address and return a final list of all addresses with their corresponding sums.

#### Streamline CLI

1. Grab the ABI

```
streamline-cli add "https://api.etherscan.io/api?module=contract&action=getabi&address=0x2634aF3E799D3E17C6cf30bCF1275A7e3808F0df&format=raw" sanctum
```

2. Build the `output.spkg`

```
make build
```

3. Run the substream?

```
sftoken
```

```
make run MODULE=<map_module_name>
```

### Learning Resources

- https://github.com/MercuricChloride/trader-joe-v2
- https://github.com/MercuricChloride/streamline/blob/master/doc/grow-a-stream.md#store-modules-aka-sfn
