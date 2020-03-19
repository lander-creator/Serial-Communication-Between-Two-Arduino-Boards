# Serial-Communication-Between-Two-Arduino-Boards
Serial Communication between two Arduino UNO Board

# Step1:
What you need:
2x Arduino uno
Jumper wires

# Step 2: schematic
![Serial-communication-between-Arduino-768x347](https://user-images.githubusercontent.com/61006702/77056709-1932d880-69d3-11ea-9c86-a5f99c9396e0.png)

# Step3: programming

For the arduino that is the sender:



char mystr[5] = "Hello"; //String data


void setup() {

  // Begin the Serial at 9600 Baud
  
  Serial.begin(9600);
  
}

void loop() {

  Serial.write(mystr,5); //Write the serial data
  
  delay(1000);
  
}

For the arduino that is the reciever:



char mystr[10]; //Initialized variable to store recieved data

void setup() {

  // Begin the Serial at 9600 Baud
  
  Serial.begin(9600);
}

void loop() {

  Serial.readBytes(mystr,5); //Read the serial data and store in var
  
  Serial.println(mystr); //Print data on Serial Monitor

  delay(1000);
}

# picture of the boards
![dtgh](https://user-images.githubusercontent.com/61006702/77057149-cefe2700-69d3-11ea-86fc-49622920e7b3.jpg)

for mofe info go to: https://iot-guider.com/arduino/serial-communication-between-two-arduino-boards/
