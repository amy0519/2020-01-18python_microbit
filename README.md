# 2020/1/18-1/19北商Micro:bit研習營
## 台北商業大學 呂芷瑛

<br>

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

***
### micro:bit程式範例
- m01.py
- m02.py
- m03.py

***
### web:bit程式範例
- w01.json
```json
(async function() {

  boardReady({
    board: 'Bit',
    url: '127.0.0.1:8080',
    multi: true
  }, async function(board) {
    window._board_ = await boardInit_(board, 100, 0);
    btnEvent_(_board_._bit_btnA_, 'pressed',
      async function() {
        _board_._bit_matrix_.setColor("000000000144009902440099044300990400000005000000064400990744009908440099090000000a0000000b0000000c4400990d0000000e0000000f440099104400991144009912440099144300991444009915440099164400991744009918440099");
        $sound.play('sound-01');
      }, [_board_._bit_btnA_, _board_._bit_btnB_]
    );
    let $pwqvh348 = _startLoop_();
    while (_loop_[$pwqvh348]) {
      btnEvent_(_board_._bit_btnB_, 'pressed',
        async function() {
          await _board_._bit_matrix_.setStringOnce('Amy', '#cc6600', 2);
          await buzzerPlay_(_board_, ["E7", "E7", "0", "E7", "0", "C7", "E7", "0", "G7", "0", "0", "0", "G6", "0", "0", "0", "C7", "0", "0", "G6", "0", "0", "E6", "0", "0", "A6", "0", "B6", "0", "AS6", "A6", "0", "G6", "E7", "0", "G7", "A7", "0", "F7", "G7", "0", "E7", "0", "C7", "D7", "B6", "0", "0", "C7", "0", "0", "G6", "0", "0", "E6", "0", "0", "A6", "0", "B6", "0", "AS6", "A6", "0", "G6", "E7", "0", "G7", "A7", "0", "F7", "G7", "0", "E7", "0", "C7", "D7", "B6", "0", "0"], ["8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8", "8"]);
        }, [_board_._bit_btnA_, _board_._bit_btnB_]
      );
      await delay(0.005, true);
    }


  });

}());
```
- w02.json
- w03.json


