# Third Eye for the Blind
Third eye for the blind is an innovation that allows blind individuals to navigate with more speed and confidence by detecting adjacent impediments with ultrasonic waves and alerting them with a buzzer sound or vibration. They merely have to wear it like a band or cloth. This is the very first wearable technology that solves the problems of all the existing technology avaiable for blind people.

<!-- Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails! -->

<!-- You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions: -->
 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->


| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Aarav A | Centennial High School | Mechanical Engineering | Incoming Sophomore



<!-- **Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help. -->

![Headstone Image](logo.svg)
  
# Final Milestone

<!-- **Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.** -->

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<!-- For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE -->



# Second Milestone

<!-- **Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.** -->

<!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone -->

# First Milestone

<!-- **Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.** -->

<!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe> -->
<!-- I was able to make the base circuit diagram and wire all the parts such as the arduino, LED, Ultrasonic Sensor, and the switch all together and get it to work. The 5 V pin of the arduino is connected to the positive end of the breadboard, while the GND pin is connected to the negative or ground end of the breadboard. The VCC pin of the Ultrasonic sensor is connected to the 5 V pin through the positive end of the breadboard. The GND pin of the sensor is connected to the GND of the arduino through the negative end. The Trig and Echo pins of the sensor are directly connected to pin’s 12 and 10 of the arduino respectively. The short end of the LED is connected on the same column as the Ground/negative end. The other end is in the middle of the board, the resistor is connected to the longer end on the same row. The switch through its middle pin is connected to the same row as the resistor and LED and also pin 5 of the arduino. The Vibration motor’s red or positive end is connected to the third pin of the switch while its negative/ground/blue end is connected to the negative/ground end of the breadboard. One of the challenges was learning how to connect all the wires from different inputs and devices through the breadboard and making sense of the diagrams. -->

<!-- For your first milestone, describe what your project is and how you plan to build it. You can include:
- An explanation about the different components of your project and how they will all integrate together
- Technical progress you've made so far
- Challenges you're facing and solving in your future milestones
- What your plan is to complete your project -->

# Schematics 
<!-- Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. -->

# Code
<!-- Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. -->

```c++
void setup() {
  // 
   const int pingTrigPin = 12; //Trigger connected to PIN 7   
 const int pingEchoPin = 10; //Echo connected yo PIN 8   
  int buz=5; //Buzzer to PIN 4   
  void setup() {   
  Serial.begin(9600);   
  pinMode(buz, OUTPUT);   
  }   
  
} 

void loop() {
  
    //VISIT : www.robotechmaker.com

  
 long duration, cm;   
  pinMode(pingTrigPin, OUTPUT);   
  digitalWrite(pingTrigPin, LOW);   
  delayMicroseconds(2);   
 digitalWrite(pingTrigPin, HIGH);   
  delayMicroseconds(5);   
  digitalWrite(pingTrigPin, LOW);   
  pinMode(pingEchoPin, INPUT);   
  duration = pulseIn(pingEchoPin, HIGH);   
  cm = microsecondsToCentimeters(duration);   
 if(cm<=50 && cm>0)   
  {   
  int d= map(cm, 1, 100, 20, 2000);   
  digitalWrite(buz, HIGH);   
  delay(100);   
  digitalWrite(buz, LOW);   
  delay(d);  
  }   
  Serial.print(cm);    
  Serial.print("cm");   
  Serial.println();   
  delay(100);   
  }   
  long microsecondsToCentimeters(long microseconds)   
  {   
 return microseconds / 29 / 2;   
  }   

}
```


# Bill of Materials
<!-- Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. -->

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Ultrasonic Sensor| Detects how far an object or obstacle is and sends it to the Arduino | $6.99 | <a href="https://www.amazon.com/WWZMDiB-HC-SR04-Ultrasonic-Distance-Measuring/dp/B0B1MJJLJP/ref=sr_1_3?crid=YPB6JRE05KFT&keywords=wwzmdib+ultrasonic+sensor&qid=1690473183&sprefix=ultrasonic+sensor+WWZ%2Caps%2C98&sr=8-3"> Link </a> |
| Arduino Micro | Acts as main CPU and controls all the sensors and devices. | $19.95 | <a href="https://www.amazon.com/Arduino-Micro-Headers-A000053-Controller/dp/B00AFY2S56/ref=sr_1_3?crid=1QTI1DYT8UBWP&keywords=arduino+micro&qid=1690473005&sprefix=arduino+micro%2Caps%2C140&sr=8-3"> Link </a> |
| Prototype Breadboard | Connects all the wiring and components of the third eye device.| $6.99 | <a href="https://www.amazon.com/HiLetgo-Finished-Prototype-Circuit-Breadboard/dp/B00FXHXT80/ref=sr_1_8?crid=8IDYCMCPYBF&keywords=hiletgo+breadboard&qid=1690473387&sprefix=HiLetGo+%2Caps%2C126&sr=8-8"> Link </a> |

# Other Resources/Examples
<!-- One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here. -->
