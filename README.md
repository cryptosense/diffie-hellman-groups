# Diffie-Hellman groups

## JSON list of common groups

You can find commonly-shared Diffie-Hellman groups in `gen/common.json` in the following
form:

```json
{
    "name": "Oakley 1 from RFC 2409, 768-bit",
    "p": 1552518092300708935130918131258481755631334049434514313202351194902966239949102107258669453876591642442910007680288864229150803718918046342632727613031282983744380820890196288509170691316593175367469551763119843371637221007210577919,
    "length": 768
}
```

where `p` is the group as a decimal integer and `length` is the bit-length of the group.

## Why?

This work is motivated by key exchange weaknesses due to commonly-shared Diffie-Hellman
groups being used, such as pointed out on [weakdh.org][weakdh].

## Contributing

If you found a group used by some piece of software which is not in the list, please open an
issue or a pull request.

[weakdh]: https://weakdh.org/
