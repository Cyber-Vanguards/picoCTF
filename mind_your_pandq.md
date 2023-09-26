
# Mind your Ps and Qs

- `#Cryptography`
- In RSA a small `e` value can be problematic but what about `N`? Can you decrypt this?
- values: `https://mercury.picoctf.net/static/2604f8b51a5cc62d38a3736938f19cef/values`
- `wget <link>`
- `file values` ASCII text

```
#--------------------------------  myRSA.py file
# Decrypt my super sick RSA:
c = 861270243527190895777142537838333832920579264010533029282104230006461420086153423
n = 1311097532562595991877980619849724606784164430105441327897358800116889057763413423
e = 65537
```


- we have these values, c is likely cipher text, e is encryption key
-  use in VM (not secure) `factordb.com` and factorize `n` and save the factorized value as `p`
- copy the 2nd factorized value and save as `q`
- calculate the _totient_ : `t = (p - 1) * (q - 1)` 
- `d = pow(e, -1, t)`
- plaintext  `p = pow(c, d, n)`


```
#--- long int into hex (drop the 0x)
phex = hex(p)[2:]

#-- convert hex to ascii
hascii = bytearray.fromhex(phex).decode('ascii')
print(hascii)
```

- `picoCTF{sma11_N_n0_g0od_13686679}`