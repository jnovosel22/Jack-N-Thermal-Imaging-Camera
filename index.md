# Thermal Imaging Camera
My project uses a Raspberry Pi and an MLX90640 thermal sensor to create a thermal image that shows tempersyure differences in its surroundings. Throughout the project, I learned how to connect hardware components, troubleshoot coding issues, and process sensor data into a visual heat map. One of the biggest challenges was finding and fixing errors in the code used to set up the Raspberry Pi. By working through these issues, I learned the importance of improvising and coming up with different solutions to a problem. This project helped me develop my programming, problem-solving, and engineering skills while gaining a better understanding of how thermal imaging technology works.




| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Jack N | Hoggard | Aerospace/Mechanical Engineering | Incoming Senior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/0ZNL-KDt8wE?si=af_gQW8OYCirsSap" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


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

<iframe width="560" height="315" src="https://www.youtube.com/embed/J9uyWW79apI?si=WzuxD-oI347XlrXh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## What I Worked On

For my second milestone I focused on improving the thermal imaging system and adding a light that responses to the thermal data. I successfully connected the MLX90640 thermal camera to the Raspberry Pi 4 and displayed the thermal image on my tv using an HDMI connection. I originally planned to use SSH from my computer, but I encountered some connection issues that didn't allow me to connect to the Pi. To be able to work on it, I had to connect the Pi directly to the TV, which allowed me to work directly on the Pi and troubleshoot problems easier. I also learned how to use the Pi's GPIO pins and built my first breadboard curcuit using a LED, resistor, and jumper wires. My main modification for this milestone was programming the Raspberry Pi to process the thermal camera data and turn on an LED whenever the camera detected a temperature above 30°C. This chnaged my project from just a passive display system into a system that can detect and react to its environment.

## Technical Accomplishments
- Connected and configured the MLX90640 thermal camera with the Raspberry Pi 4
- Improved and modified the Python thermal imaging code
- Learned how to use Raspberry Pi GPIO pins
- Built and tested an LED circuit on a breadboard
- Added GPIO control into the thermal camera software
- Programmed the LED to turn on automatically when temperature goes above 30°C
- Displayed thermal imaging data on a TV through HDMI

## Challenges and Solutions

One challenge was getting comfortable with wiring electronic components on a breadboard. I had to learn how the breadboard rows are connected and how to correctly wire an LED and resistor. Another challenge was learning how to use Raspberry Pi GPIO pins with Python. After testing with some code that made the LED blink, I was able to integrate GPIO control into the thermal camera project. I also experienced issues using SSH from my computer to access the Raspberry Pi. To overcome this problem, I connected the Raspberry Pi directly to a TV through HDMI and finished the coding and modifications directly on the Pi. Finally, I had to modify and troubleshoot the thermal camera software so that it could both display thermal data and control external hardware at the same time.

## What Has Been Surprising

One surprising aspect of the project was how quickly a simple LED modification made the system feel much more interactive. Instead of only displaying temperature information, the project now responded to temperature changes in real time. I was also surprised by how much troubleshooting and debugging is involved in hardware projects, especially when combining sensors, wiring, and software.

## Next Steps Before the Final Milestone

Before the final milestone, I plan to:

- Add a servo motor to the project.
- Mount the thermal camera onto the servo.
- Program the servo to rotate toward the hottest detected object.
- Continue improving the thermal imaging software.
- Build a more complete thermal tracking system that can automatically locate heat sources.

# Final Milestone


<iframe width="560" height="315" src="https://www.youtube.com/embed/622oiV1isv0?si=UNNXXe3bX58cmYkx" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Accomplishments

Since my last milestone, I completed my final modification. I successfully connected an MLX90640 thermal camera and an SG90 servo motor to a Raspberry Pi 4 as well as adding a seperate power source for the servo. The camera displays a live thermal image on a TV, and the servo rotates to track the hottest object in the camera's field of view. I also improved my tracking code by having the servo respond to where the hottest column is located instead of just the single hottest pixel, making the tracking more accurate.

## Biggest Challenges and Triumphs

The biggest challenge was getting the servo to track the heat correctly. There were times when it moved away from the hottest object instead of toward it, and I spent a lot of time changing my code, testing different ideas, and debugging until it worked. Another challenge was that I originally wanted to use both an Arduino and a Raspberry Pi, but I realized that would make the project much more complicated. I redesigned the project to use only the Raspberry Pi, which simplified both the hardware and software. Then finally my SSH stopped working during the project and I had to plug the Pi in directly to the TV via an HDMI cable. Overall though, my biggest accomplishment was getting everything to work together. Seeing the thermal image update in real time while the servo automatically tracked the hottest object made all of the troubleshooting worth it. It was really rewarding to see the final project come together.

## What I Learned

- Python programming
- Raspberry Pi GPIO programming
- I2C communication
- Thermal imaging with the MLX90640 camera
- Servo motor control
- Breadboard wiring and electronics
- Debugging hardware and software together
- Breaking a large engineering problem into smaller steps

One of the biggest lessons I learned was that engineering is mostly about solving problems. Almost nothing worked perfectly the first time, but every problem anad mistake helped me understand the project better and learn from the mistakes.

## Furture Goals

After everything I learned during BlueStamp Engineering, I'd like to continue building projects with the MLX90640 thermal camera. One idea I have is to revisit my original idea of building a thermal tracking car that can detect and follow the hottest object while avoiding obstacles. At the beginning of this project, that idea was too ambitious, but now that I understand how to use the Raspberry Pi, thermal camera, servo motors, and GPIO pins, I think it's something I could actually build in the future. I'd also like to experiment with other thermal imaging projects, improve the tracking system to make it smoother and more accurate, and continue learning about robotics, computer vision, and coding. This project gave me a strong foundation, and I'm excited to keep building on what I learned.

# Schematics 
 <img width="939" height="451" alt="image" src="https://github.com/user-attachments/assets/2aadabcc-0b34-40aa-af52-2bb909015bdd" />


# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 
## Milestone 1 Code
```c++
import time
import board
import busio
import numpy as np
import adafruit_mlx90640
import matplotlib.pyplot as plt
 
def initialize_sensor():
    i2c = busio.I2C(board.SCL, board.SDA)
    mlx = adafruit_mlx90640.MLX90640(i2c)
    mlx.refresh_rate = adafruit_mlx90640.RefreshRate.REFRESH_4_HZ
    return mlx
 
def setup_plot():
    plt.ion()
    fig, ax = plt.subplots(figsize=(12, 7))
    therm1 = ax.imshow(np.zeros((24, 32)), vmin=20, vmax=40, cmap='inferno', interpolation='bilinear')
    cbar = fig.colorbar(therm1)
    cbar.set_label('Temperature [°C]', fontsize=14)
    plt.title('Thermal Image')
    return fig, ax, therm1
 
def update_display(fig, ax, therm1, data_array):
    therm1.set_data(np.fliplr(data_array))
    therm1.set_clim(vmin=20, vmax=40)
    ax.draw_artist(ax.patch)
    ax.draw_artist(therm1)
    fig.canvas.update()
    fig.canvas.flush_events()
 
def main():
    mlx = initialize_sensor()
    fig, ax, therm1 = setup_plot()
    
    frame = np.zeros((24*32,))
    t_array = []
    max_retries = 5
 
    while True:
        t1 = time.monotonic()
        retry_count = 0
        while retry_count < max_retries:
            try:
                mlx.getFrame(frame)
               
                print("min:", round(min(frame),1), "max:", round(max(frame),1))
                data_array = np.reshape(frame, (24, 32))
                update_display(fig, ax, therm1, data_array)
                plt.pause(0.001)
                t_array.append(time.monotonic() - t1)
                print('Sample Rate: {0:2.1f}fps'.format(len(t_array) / np.sum(t_array)))
                break
            except ValueError:
                retry_count += 1
            except RuntimeError as e:
                retry_count += 1
                if retry_count >= max_retries:
                    print(f"Failed after {max_retries} retries with error: {e}")
                    break
 
if __name__ == '__main__':
    main()
```
## Milestone 2 Code
```c++
import time
import board
import busio
import numpy as np
import adafruit_mlx90640
import matplotlib.pyplot as plt
from gpiozero import LED
 
def initialize_sensor():
    i2c = busio.I2C(board.SCL, board.SDA)
    mlx = adafruit_mlx90640.MLX90640(i2c)
    mlx.refresh_rate = adafruit_mlx90640.RefreshRate.REFRESH_4_HZ
    return mlx
 
def setup_plot():
    plt.ion()
    fig, ax = plt.subplots(figsize=(12, 7))
    therm1 = ax.imshow(np.zeros((24, 32)), vmin=20, vmax=40, cmap='inferno', interpolation='bilinear')
    cbar = fig.colorbar(therm1)
    cbar.set_label('Temperature [°C]', fontsize=14)
    plt.title('Thermal Image')
    return fig, ax, therm1
 
def update_display(fig, ax, therm1, data_array):
    therm1.set_data(np.fliplr(data_array))
    therm1.set_clim(vmin=20, vmax=40)
    ax.draw_artist(ax.patch)
    ax.draw_artist(therm1)
    fig.canvas.update()
    fig.canvas.flush_events()
 
def main():
    mlx = initialize_sensor()
    fig, ax, therm1 = setup_plot()
    led = LED(17)
    
    frame = np.zeros((24*32,))
    t_array = []
    max_retries = 5
 
    while True:
        t1 = time.monotonic()
        retry_count = 0
        while retry_count < max_retries:
            try:
                mlx.getFrame(frame)
                print("min:", round(min(frame),1), "max:", round(max(frame),1))

                if max(frame) > 30:
                    led.on()
                else:
                    led.off()
                    
                print("min:", round(min(frame),1), "max:", round(max(frame),1))
                data_array = np.reshape(frame, (24, 32))
                update_display(fig, ax, therm1, data_array)
                plt.pause(0.001)
                t_array.append(time.monotonic() - t1)
                print('Sample Rate: {0:2.1f}fps'.format(len(t_array) / np.sum(t_array)))
                break
            except ValueError:
                retry_count += 1
            except RuntimeError as e:
                retry_count += 1
                if retry_count >= max_retries:
                    print(f"Failed after {max_retries} retries with error: {e}")
                    break
 
if __name__ == '__main__':
    main()
```
## Milestone 3 Code
```c++
import time
import board
import busio
import numpy as np
import adafruit_mlx90640
import matplotlib.pyplot as plt
from gpiozero import Servo

def initialize_sensor():
    i2c = busio.I2C(board.SCL, board.SDA)
    mlx = adafruit_mlx90640.MLX90640(i2c)
    mlx.refresh_rate = adafruit_mlx90640.RefreshRate.REFRESH_4_HZ
    return mlx

def setup_plot():
    plt.ion()
    fig, ax = plt.subplots(figsize=(12, 7))
    therm1 = ax.imshow(np.zeros((24, 32)), vmin=20, vmax=40, cmap='inferno', interpolation='bilinear')
    cbar = fig.colorbar(therm1)
    cbar.set_label('Temperature [°C]', fontsize=14)
    plt.title('Thermal Image')
    return fig, ax, therm1

def update_display(fig, ax, therm1, data_array):
    therm1.set_data(np.fliplr(data_array))
    therm1.set_clim(vmin=20, vmax=40)
    ax.draw_artist(ax.patch)
    ax.draw_artist(therm1)
    fig.canvas.update()
    fig.canvas.flush_events()

def main():
    mlx = initialize_sensor()
    fig, ax, therm1 = setup_plot()

    servo = Servo(
        18
    )

    current_position = 0

    frame = np.zeros((24 * 32,))
    t_array = []
    max_retries = 5

    while True:
        t1 = time.monotonic()
        retry_count = 0

        while retry_count < max_retries:
            try:
                mlx.getFrame(frame)

                data_array = np.reshape(frame, (24, 32))

                _, hot_col = np.unravel_index(np.argmax(data_array), data_array.shape)

                servo.value = np.interp(hot_col, [0,31], [1,-1])

                update_display(fig, ax, therm1, data_array)
                plt.pause(0.001)

                t_array.append(time.monotonic() - t1)
                print(
                    f"Hottest Column: {hot_col} | "
                    f"Servo: {servo.value:.2f} | "
                    f"Sample Rate: {len(t_array) / np.sum(t_array):.1f} fps"
                )

                break


            except ValueError:
                retry_count += 1

            except RuntimeError as e:
                retry_count += 1

                if retry_count >= max_retries:
                    print(f"Failed after {max_retries} retries with error: {e}")
                    break

if __name__ == '__main__':
    main()
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
| 9v 1a Converter Adaptor | Power for the servo | $7.59 | <a href="https://www.amazon.com/dp/B074BRR5YN?ref_=cm_sw_r_cp_ud_dp_34TCN7JY70MCM2DQS4KF_1"> Link </a> |

# Other Resources
- [Resource 1](https://how2electronics.com/diy-thermal-imaging-camera-with-mlx90640-raspberry-pi/)

