**Joy1(PicoW):**

x_axis = ADC(Pin(27))  # VRx
y_axis = ADC(Pin(26))  # VRy

button = Pin(18, Pin.IN, Pin.PULL_UP) #pin5

buttonP = 1
    
err_intX = 450
err_intY = 450

uart = UART(0, baudrate=115200, tx=Pin(0), rx=Pin(1))

**Joy2(Pico):**

uart = UART(0, baudrate=115200, tx=Pin(0), rx=Pin(1))

joy_x = ADC(27)
joy_y = ADC(26)
switch = Pin(18, Pin.IN, Pin.PULL_UP)

send_err_intX = 200
send_err_intY = 200

**Buttons:**

Group1:
X Y B A: Button 0~3

Group2:
L R ZL ZR: Button 4~7

Group3: 
Plus & Minus: Button 8 & 9

_group4:_ (built-in)
JoyDown L&R: Button 10 & 11

Group5:
Hat: Button 12~15
