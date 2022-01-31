# Hello World Protocol

- [Query](./query)
- [Socket](./socket)

This protocol keep track of all orders of the vanity address decentralized marketplace.

## Blockchain Data Protocol (copy pasted)

Any **Bitcoin SV** transaction where the **first output** contains the fields from the below table complies with the Hello World Protocol, provided that a private key belonging to the address from field 3 has signed **at least one of the inputs** to the transaction. If no funds are in the address, an r-puzzle can be used to achieve a valid input signature.

PUSHDATA | Field
---------|---------------------------------
0        | \`OP_0\` (see [this](https://bitcoinsv.io/2019/07/27/the-return-of-op_return-roadmap-to-genesis-part-4/))
1        | \`OP_RETURN\`
2        | Protocol Namespace Address (\`1BaguettegL3S21U2erSNDYSe7UMJL2Y8v\`)
3        | Txid of the contract to be searched (the "API response" you get when you deploy a contract)
4        | The index where the contract is; probably 0
5        | Message (optionnal)

## Usage

#### If you deploy a contract

Deploy a vanity address contract.  
List the txid here.

#### If you are a searcher

Get all txid listed here.  
Verify these are vanity address contracts (I think it's pretty hard).  
Search the most profitable one.

#### If you are just curious and want to explore all listed order

- [Query](./query)  
And on my web browser I need to execute "selector = 0" in the console tab to make it work !
