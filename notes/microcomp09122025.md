# microcomp sept 12, 2025

## ranges

- just the basic stuff you know already <br>

|bits | unsigned |signed magnitude | 2's complement |
|---- | -------- | --------------- | -------------- |
|000 | 0 | 0 | 0 |
|001 | 1 | 1 | 1 |
|010 | 2 | 2 | 2 |
|011 | 3 | 3 | 3 |
|100 | 4 | -0 | -4 |
|101 | 5 | -1 | -3 |
|110 | 6 | -2 | 2 |
|111 | 7 | -3 | 1 |

**unsigned** `0` to `(2^k)-1` <br>
**signed-mag** `-2^(k-1)` to `2^(k-1)-1` <br>

## casting stuff
- single expressions with a mix of signed and unsigned
  - signed values are implicitly cast to unsigned
  - includes comparison operations such as `==`, `>`, `<`, `>=`, and `<=`
  - but imo you should probably always explicitly cast the values to a common type so you don't get it mixed up and cause weird bugs down the road


## parity
- google it to review please