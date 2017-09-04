# BaseN
Convert between bases using arbitrary Positional Numeral Systems

## Usage:
To illustrate simple usage, see Hex examples:

### Hexadecimal
```
>>> import BaseN
>>> hexadecimal = '0123456789abcdef'

# 19 (decimal) == 13 (hex)
>>> BaseN.DecToBaseN('19', hexadecimal)
'13'
>>> BaseN.BaseNToDec('13', hexadecimal)
'19'

# afe (hex) == 
>>> BaseN.BaseNToDec('afe', hexadecimal)
'2814'
>>> BaseN.DecToBaseN('2814', hexadecimal)
'afe'

```

### Complex Symbol Sets
The main purpose of this module is to support complex symbol sets. For example, consider the digit set of all unreserved URL symbols (per [RFC 3986 section 2.3](https://tools.ietf.org/html/rfc3986#section-2.3)):

```
>>> import BaseN
>>> DIGIT_SET = '0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ_.-~'

>>> BaseN.DecToBaseN('68', DIGIT_SET)
'12'
>>> BaseN.BaseNToDec('12', DIGIT_SET)
'68'

>>> BaseN.BaseNToDec('afe', DIGIT_SET)
'44564'
>>> BaseN.DecToBaseN('44564', DIGIT_SET)
'afe'

```
