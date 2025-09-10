# microcomp sept 10, 2025

## signed and unsigned ints
- sign-magnitude
- 1's complement
- 2's complement

    ### signed magnitude
    - so like you have `1100` it'd be `-0b100` and if you had `0100` then it'd be `+0b100`
    
    ### two's complement
    - https://en.wikipedia.org/wiki/Two%27s_complement
    - basically you're like counting back from 0.
    - like you're calculating the distance from zero and you use the first bit to sorta indicate whether you're positive or negative
    - like if you have `0b0000` and you wanna have it represent some negative number so you do `2^n - n` and it's something about subtraction being slow so you instead do `2^n + (-n)` and to find `-n` you do something like `~n + 1` (ALWAYS REMEMBER THE +1) and **IGNORE LAST CARRY**
  - ### examples
    ```
    2 - 6 = -4
    2 + (-6) = -4
    
    2 = 0b0010
    6 = 0b0110
    ~0b0110 + 1 = 1001 + 1
    = 0b1010
    = -6

      0b0010
    + 0b1010
    --------
      0b1100

    = -4

    it's -4 because to get back to 0 you'd need to...
    0b1100 (+0)
    0b1101 (+1)
    0b1110 (+2)
    0b1111 (+3)
    0b10000 (+4) but since you ignore the overflow/carry? it'd be 0b0000
    ```