
print("----------------Password Complexity Checker--------------------")
print("\n")
print("-----------------------------NOTICE----------------------------")
print("The Length of the Password must be at least * Characters")
print("Password must be include alteast one Uppercase letter")
print("Password must include at least one numeric numeric number .")
print("Password must include at least one special character (eg.!,@,#,$,%..etc).")
print("Password should not include easily guessable personal information")

password=input("Enter the Password :")
score=0
has_lower=any(c.islower() for c in password)
has_upper=any(c.isupper() for c in password)
has_digit = any(c.isdigit() for c in password)
has_special = any(not c.isalnum() for c in password)

if(len(password)>=8):
    score=score+20
else:
    print("Password length must be greater than 8 characters")

if has_upper :
    score=score+20
else:
    print("password must be have Uppercase characters(eg.ABC..)")

if(has_lower):
    score=score+20
else:
    print("password must be have lowercase characters(eg.abc..)")

if(has_digit):
    score=score+20
else:
    print("password must be have numbers (eg.123..)")

if(has_special):
    score=score+20
else:
    print("password must be have special characters(eg.@#&..)")
print("Your passoword score :",score)

    
