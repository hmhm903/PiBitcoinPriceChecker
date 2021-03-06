# PiBitcoinPriceChecker
Display the bitcoin price on 7-segment led array.

## Appearance
![img](https://github.com/hmhm903/PiBitcoinPriceChecker/blob/master/appearance.png)

## Components
- Raspberry Pi (We checked the operation of Pi 3 model B and Pi Zero W)
- 7-segment led array which can display 8 digits
- Wire (in order to connect raspberry pi with led)

## Circuit
- GPIO 2\~9: led anode(digit0\~digit7)
- GPIO 10\~17: cathode(A\~G+DP)

## Motion of this program
- Run the DisplayController process and BitcoinPriceGetter process. 
- DisplayController control the GPIO of raspberry pi (using dynamic lighting system). 
- BitcoinPriceGetter get the bitcoin price(JPY) using the public API of coincheck(https://coincheck.com/api/rate/btc_jpy). 
- DisplayController get the bitcoin price from DisplayController process and display it.

## Usage
1. Connect Raspberry Pi with led in accordance with the following image.
2. Clone this repository on raspberry pi.  
`sudo git clone https://github.com/hmhm903/PiBitcoinPriceChecker`
3. Exec following command on terminal.  
`cd PiBitcoinPriceChecker`  
`python3 main.py`
