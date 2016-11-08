# Diffie-Hellman groups

## JSON list of common groups

You can find commonly-shared Diffie-Hellman groups in `gen/common.json` in the following
form:

```json
{
    "name": "Oakley 1 from RFC 2409, 768-bit",
    "g": 2,
    "p": 1552518092300708935130918131258481755631334049434514313202351194902966239949102107258669453876591642442910007680288864229150803718918046342632727613031282983744380820890196288509170691316593175367469551763119843371637221007210577919,
    "length": 768,
    "prime": true,
    "safe_prime": true
}
```

where `p` is the integer definining the group, `g` is a generator of this group and
`length` is the bit-length of `p`.  `prime` is `true` if `p` passed the Baillie-PSW test.
`safe_prime` is `true` if `(p - 1) / 2` passed the Baillie-PSW test.

## Why?

This work is motivated by key exchange weaknesses due to commonly-shared Diffie-Hellman
groups being used, such as pointed out on [weakdh.org][weakdh].

Cryptosense tests for these groups on TLS and SSH servers at
[discovery.cryptosense.com][discovery] and in applications in its [Analyzer][analyzer].

## Contributing

If you found a group used by some piece of software which is not in the list, please open an
issue or a pull request.

[weakdh]: https://weakdh.org/
[discovery]: https://discovery.cryptosense.com/
[analyzer]: https://cryptosense.com/analyzer/
