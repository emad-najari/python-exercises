## Compress Strings

1. Write code that compresses a string
  - 'aaaabbccc' -> 'a4b2c3'
  - 'abbbc' -> 'a1b3c1'
2. Write code that decompresses a string
  - 'a4b2c3' -> 'aaaabbccc'
  - 'a1b3c1' -> 'abbbc'


Solution:

string = 'abbbc'
tmp = string[0]
j = 0
out = ''
for i in string:
    if i == tmp:
        j += 1
    else:
        out += tmp + str(j)
        tmp = i
        j = 1
else:           
    out += tmp + str(j)
print(out)
