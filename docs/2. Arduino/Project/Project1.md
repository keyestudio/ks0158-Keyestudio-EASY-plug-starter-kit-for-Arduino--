### Project 1 Hello World

**1.Introduction**

For the first lesson, we will begin with something simple. This lesson is called "Hello World!". This is a communication test for your Arduino and PC, also a primer project for you to have your first try of the Arduino world!

**2.Components Needed** 

- Arduino board *1
- USB cable *1

**3.Text Code** 

Connect the board to your PC using the USB cable; copy below code into Arduino IDE, and click upload to upload it to your board.

```c
int val;//define variable val

void setup()
{
  Serial.begin(9600);// set the baud rate at 9600 to match the software set up. When connected to a specific device, (e.g. bluetooth), the baud rate needs to be the same with it.
}

void loop()
{
  val=Serial.read();// read the instruction or character from PC to Arduino, and assign them to Val.
  if(val=='R')// determine if the instruction or character received is “R”.
  {  // if it’s “R”,    
    Serial.println("Hello World!");// display“Hello World！”string.
  }
}
```

**4.Result**

Open serial port monitor of the Arduino IDE, input “R”, click “Send”, you can see it displays “Hello World!”.

![](media/image-20251127122547382.png)
