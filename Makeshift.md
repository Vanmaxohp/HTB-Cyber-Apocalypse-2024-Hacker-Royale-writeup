Code mã hoá:
```
from secret import FLAG

flag = FLAG[::-1]
new_flag = ''

for i in range(0, len(flag), 3):
    new_flag += flag[i+1]
    new_flag += flag[i+2]
    new_flag += flag[i]

print(new_flag)
```
Ciphertext: `!?}De!e3d_5n_nipaOw_3eTR3bt4{_THB`
Đọc code thì cũng chả có gì đáng suy ngẫm, code giải cũng đơn giản:
```
new_flag = '!?}De!e3d_5n_nipaOw_3eTR3bt4{_THB'
FLAG = ''

for i in range(0, len(new_flag), 3):
    FLAG += new_flag[i+2]
    FLAG += new_flag[i]
    FLAG += new_flag[i+1]

flag = FLAG[::-1]
print(flag)
```
Flag: `HTB{4_b3tTeR_w3apOn_i5_n3edeD!?!}`
