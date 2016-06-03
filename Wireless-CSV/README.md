# Wireless sensor to CSV example
Using 2 BBC micro:bits, it is possible to wirelessly transfer sensor data (for example, accelerometer readings) from up to 70m away and store them in a CSV file on a normal computer!   
Once your CSV file is created, it is pretty simple to open it up with Microsoft Excel or LibreOffice Calc, for additional processing.   
   
The process involves 2 parts, the script which runs on both the micro:bits and the Python script running on the logging computer.    

## Micro:bit script
The script that runs on both of the BBC micro:bits is written using the [Microsoft PXT platform](https://pxt.io/). The code in Typescript is included, or you can easily just [fork the script](https://m.pxt.io/vxdmdu).   
If you want to log something different other than the accelerometer values, simply change the input block in the ```send value``` block.
    
## Python logging script   
The simple Python (3) micro:bit logging script runs on the logging computer which has the receiver micro:bit plugged into it via USB.   
It sits reading and interpreting each line, converting it across at the end to the ```microbit_data.csv``` file.   
To force the Python script to output the .csv file, simply close/stop the program, or disconnect the micro:bit.
