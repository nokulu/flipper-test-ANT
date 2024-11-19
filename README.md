### Testing DC Motors with Flipper Zero: The First Step Toward Building ANT

#### Introduction

This project is an essential step toward creating **ANT** (Autonomous Nerf Turret), a device that will use face recognition technology to identify and engage targets. Before moving to the complex systems needed for ANT, it is crucial to test the basic motor control functionality. The test project involves using the **Flipper Zero** to control two DC motors via an **L298N motor driver**. This process not only helps in understanding motor operations but also ensures the viability of microcontroller controlled motors for ANT.

---

### Project Goals

1. **Verify Motor Functionality**: Confirm that two DC motors can be independently controlled using Flipper Zero and an L298N motor driver.
2. **Learn GPIO Control**: Use the Flipper Zero’s GPIO pins to send signals to the motor driver.
3. **Prepare for ANT**: Use this test to ensure smooth motor operation, a critical component for ANT’s movement and targeting systems.

---

### Steps to Build and Test the Setup

#### **1. Gather Materials**

- **Flipper Zero**: A versatile multi-tool that will act as the controller.
- **L298N Motor Driver**: A module to control the DC motors.
- **Two DC Motors**: The motors to be tested.
- **Power Supply**:
  - 5V-12V DC power source for motors.
  - USB power for Flipper Zero.
- **Connecting Wires**: Jumper wires for connecting components.
- **Breadboard (Optional)**: For easy prototyping and connections.

---

#### **2. Hardware Setup**

1. **Connect the L298N Motor Driver to the Motors**:
   - Attach the motor terminals to the `OUT1`/`OUT2` and `OUT3`/`OUT4` ports of the motor driver.

2. **Connect the L298N to Flipper Zero**:
   - Use GPIO pins on Flipper Zero for control signals:
     - **IN1/IN2**: Control Motor A’s direction.
     - **IN3/IN4**: Control Motor B’s direction.
     - **ENA/ENB**: Enable pins for PWM speed control.
   - Use the corresponding GPIO pins on Flipper Zero (e.g., PA7, PA6, PB3, etc.).

3. **Power the L298N**:
   - Connect an external power source to the motor driver’s `VCC` and `GND` pins.
   - Ensure the motor driver’s 5V logic supply is enabled, if required.

4. **Check Connections**:
   - Double-check all connections to avoid short circuits or improper wiring.

---

#### **3. Software Setup**

1. **Prepare the Flipper Zero**:
   - Update the firmware to ensure compatibility with GPIO and scripting features.
   - Install the Flipper Zero SDK or necessary tools for writing and uploading scripts.

2. **Write the Control Script**:
   - Use JavaScript to create a program that:
     - Initializes the GPIO pins.
     - Controls motor direction and speed using PWM signals.
     - Maps Flipper Zero’s built-in buttons (`up`, `down`, `left`, `right`) to motor operations.

   Example functionality:
   - **Forward/Backward**: Controls motor directions.
   - **Speed Adjustment**: Maps `up`/`down` buttons to increase or decrease speed.

3. **Upload the Script**:
   - Use the Flipper Zero’s file management system to upload the script.
   - Ensure the script runs without errors by testing it in the Flipper Zero’s interface.

---

#### **4. Testing the Setup**

1. **Initial Tests**:
   - Power on the system and verify that the Flipper Zero initializes all GPIO pins correctly.
   - Ensure the motors remain stationary until a command is issued.

2. **Directional Control**:
   - Use the Flipper Zero buttons (`left`, `right`) to test forward and backward motor movement.

3. **Speed Control**:
   - Test increasing and decreasing motor speed using the `up` and `down` buttons.
   - Observe motor responsiveness and ensure no jitter or irregular behavior.

4. **Debugging**:
   - If any issues arise, check wiring, power levels, and GPIO signal logic.
   - Use console logs or Flipper Zero’s debugging tools to trace problems in the script.

---

#### **5. Document Results**

- Record motor behavior, including:
  - Responsiveness to directional commands.
  - Speed adjustments.
- Note any challenges or issues that require attention in the next project phase.

---

### Looking Ahead: Toward ANT

This test project lays the groundwork for **ANT**, the Autonomous Nerf Turret. With a successful motor control test, the next steps will involve:
- Integrating sensors for environmental awareness.
- Adding face recognition capabilities for target identification.
- Developing a turret mechanism to rotate and aim.

By ensuring the motors function reliably, this project ensures a solid foundation for the complex challenges ahead in building ANT.

---

### Conclusion

The Flipper Zero offers a versatile platform for testing and controlling hardware like motors. This project not only confirms the device’s suitability for the ANT project but also provides critical insights into motor control and GPIO usage. With this phase completed, the journey toward an autonomous, face-recognizing Nerf turret moves one step closer to realization.
