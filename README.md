# python_task_3
# This is Task - 3 Which we create a password generator

import random as rd

print('-'*50)
print("********* Generate Random Password ************")
print('-'*50)
print("Maximum length is 12")
length = int(input("Enter Your password length :"))

digits = list(range(10))
upper_case = [chr(i) for i in range(65,91)]
lower_case = [chr(j) for j in range(97,123)]
alpha_str = ''.join(upper_case) + ''.join(lower_case)

pwd12 = ''
for k in range(12):
    a = str(rd.choice(alpha_str))
    b = str(rd.choice(digits))
    pwd12+=a
    pwd12+=b

len_pass = ''
if length <= 12:
    for k in range(len(pwd12)):
        if length > k:
            len_pass += pwd12[k]
        else:
            break
    print(f"Your Password is : {len_pass}")
else:
    print("Length is Too Bigger ..!")
print('-'*50)
