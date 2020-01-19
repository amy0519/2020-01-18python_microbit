# 2020/1/18-1/19北商Micro:bit研習營
## 台北商業大學 呂芷瑛

### python程式設計
- p01.py
```python
from microbit import *
import radio

radio.on()

while True:
    if button_a.was_pressed():
        radio.send('Hi') 
        
    incoming = radio.receive()
    if incoming == 'Hi':
        display.show('Hello', delay=300, wait=False, loop=False, clear=True)

```
- p02.py
- p03.py

### micro:bit設計
- m01.py 
- m02.py
- m03.py


### web:bit設計
- w01.py
- w02.py
- w03.py





