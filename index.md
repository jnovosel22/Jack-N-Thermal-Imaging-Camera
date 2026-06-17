# Thermal Imaging Camera
My project uses a Raspberry Pi and an MLX90640 thermal sensor to create a thermal image that shows tempersyure differences in its surroundings. Throughout the project, I learned how to connect hardware components, troubleshoot coding issues, and process sensor data into a visual heat map. One of the biggest challenges was finding and fixing errors in the code used to set up the Raspberry Pi. By working through these issues, I learned the importance of improvising and coming up with different solutions to a problem. This project helped me develop my programming, problem-solving, and engineering skills while gaining a better understanding of how thermal imaging technology works.




| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Jack N | Hoggard | Aerospace/Mechanical Engineering | Incoming Senior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)

# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your first milestone, describe what your project is and how you plan to build it. You can include:
## Components and Integration
My project uses a Raspberry Pi 4, an MLX90640 thermal sensor, jumper wires, and several Python libraries. The thermal sensor collects temperature data from whatever it is pointed at and sends that information to the Raspberry Pi. The Raspberry Pi then processes the data and uses Python to create a color-coded thermal image that shows temperature differences in real time.

## Technical Progress
So far, I have successfully connected the hardware and installed all of the required software and libraries. I configured the Raspberry Pi to communicate with the thermal sensor and copied the code that reads temperature data and displays it as a thermal image.

## Challenges and Future Milestones

One of the biggest challenges has been debugging the software. I ran into problems with installing some of the code, configuring I2C communication, and getting the Raspberry Pi to recognize the sensor. Also figuering out the issue with the camera only displaying a yellow screne with 1 purple pixel in the middle.

## Plan for Completion

To finish my project, I plan to continue testing and improving the code so the thermal camera runs more smoothly. Once everything is working reliably, I will document the project and prepare my final presentation demonstrating how the thermal imaging camera works.
- An explanation about the different components of your project and how they will all integrate together
- Technical progress you've made so far
- Challenges you're facing and solving in your future milestones
- What your plan is to complete your project

# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE


# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // import time
import board
import busio
import numpy as np
import adafruit_mlx90640
 
def main():
    # Setup I2C connection
    i2c = busio.I2C(board.SCL, board.SDA, frequency=400000)
    mlx = adafruit_mlx90640.MLX90640(i2c)
    mlx.refresh_rate = adafruit_mlx90640.RefreshRate.REFRESH_2_HZ
 
    frame = np.zeros((24 * 32,))  # Initialize the array for all 768 temperature readings
 
    while True:
        try:
            mlx.getFrame(frame)  # Capture frame from MLX90640
            average_temp_c = np.mean(frame)
            average_temp_f = (average_temp_c * 9.0 / 5.0) + 32.0
            print(f"Average MLX90640 Temperature: {average_temp_c:.1f}C ({average_temp_f:.1f}F)")
            time.sleep(0.5)  # Adjust this value based on how frequently you want updates
 
        except ValueError as e:
            print(f"Failed to read temperature, retrying. Error: {str(e)}")
            time.sleep(0.5)  # Wait a bit before retrying to avoid flooding with requests
        except KeyboardInterrupt:
            print("Exiting...")
            break
        except Exception as e:
            print(f"An unexpected error occurred: {str(e)}")
 
if __name__ == "__main__":
    main():
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| WT-Thermal Camera MLX90640-D55 | Thermal Imaging Camera | $66.30 | <a href="https://a.co/d/007vHo8q"> Link </a> |
| uni Card Reader USB 3.0/USB-C | Transfering Code to Raspberry Pi | $9 | <a href="https://a.co/d/07R4LBlT"> Link </a> |
| Raspberry pi 4 Starter Kit | Process the thermal camera/brain of project | $147.79 | <a href="https://a.co/d/040pf62B"> Link </a> |
| Electronics Fun Kit | Housing the componets of the project | $16 | <a href="https://a.co/d/03leMRaR"> Link </a> |
| SG90 | Servo for thermal camera | $7.98 | <a href="https://a.co/d/07t1leAF"> Link </a> |
| SG90 Microbracket | Bracket for thermal camera | $6 | <a href="https://a.co/d/06bYyd9i"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
