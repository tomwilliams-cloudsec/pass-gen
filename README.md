# pass-gen
import random 

capital_let = "QWERTYUIOPASDFGHJKLZXCVBNM" 
small_let = "qwertyuiopasdfghjklzxcvbnm"
numbers = "1234567890" 
special_char = "?,.!$]}*#@&"

upper,lower,digits,odd = True, True, True, True

finalpas = ""

if upper:
    finalpas += capital_let
if lower: 
    finalpas += small_let 
if digits: 
    finalpas += numbers 
if odd: 
    finalpas += special_char 

length = 20
howmuch = 10 

for x in range (howmuch): 
    password = "". join (random.sample(finalpas, length))
    print(password)
