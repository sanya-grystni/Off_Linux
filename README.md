# Off_Linux
Timer for automatic shutdown

import os
import time
from time import *

print("============================================");
print("============ 80 minutes = 4800 =============");
print("============ 1 hour = 3600 sec =============");
print("============ 2 hour = 7200 sec =============");
print("============================================");
a = input("Vvedite vremy na otklychenia v secyndax:");

start_timer = time()
struct = localtime(start_timer)
print('\n Vremy starta na vikluchenia:', strftime('%X', struct))

i = a
while i > -1:
    print (i)
    i -=1
    sleep ( 1 )
end_timer = time ()
difference = round ( end_timer - start_timer )
print('\nRuntime'  , difference, 'Seconds')
if i == 0:
 os.system('sudo shutdown now')
