**Arduino-Based Vending Machine System**
  - A fully automated vending machine built with Arduino Mega featuring coin detection, automated dispensing, and transaction management for Philippine peso coins (₱5 and ₱10).
  
  - <img width="600" height="600" alt="460512849_2276105216058668_8403639333552587064_n" src="https://github.com/user-attachments/assets/99959765-e255-4192-974a-a1a4709d07a6" />
<img width="600" height="600" alt="458921430_1784429395297743_3975630234930603805_n" src="https://github.com/user-attachments/assets/7fa909e2-9f62-4f55-91f4-c89ba10387be" />

**Overview**
This project implements a complete vending machine system using Arduino Mega microcontroller. The system handles the entire vending process from coin insertion to product dispensing, with built-in safety features like automatic refunds and product verification.

**Key Highlight**s:
 - Supports Philippine ₱5 and ₱10 coins
 - Spiral coil motor control for dispensing
 - Real-time LCD transaction display
 - Product detection verification
 - Automatic refund mechanism
 - Time-based transaction timeout

**Features**
 - Button-Based Selection: Easy product selection using physical push buttons
 - Automated Dispensing: Precise DC motor control for spiral coil mechanisms
 - LCD Interface: 16x2 display showing transaction details and system status
 - Coin Detection: IR-based coin detection for ₱5 and ₱10 denominations
 - Product Verification: Sensors confirm successful product dispensing
 - Payment Processing: Real-time verification and credit tracking
 - Auto-Refund System: Returns coins if no selection made within timeout period
 - Arduino Control: Complete hardware integration through Arduino Mega

**System Capabilities**

1. Coin Types     - Philippine ₱5 and ₱10 coins
2. Product Slots  - 3 independent dispensing units
3. Display        - 16x2 LCD with backlight
4. Motors         - DC motors with L298N drivers
5. Detection      - IR sensors for coins and products
6. Timeout        - Configurable transaction timeout
7. Refund         - Servo-controlled coin return


**Hardware Components**
1. Arduino Mega 2560
   - Main microcontroller
2. L298N Motor Driver
   - Motor control for dispensers
3. 16x2 LCD Display
   - User interface
4. IR-Sensor
   - Coin detection (₱5 & ₱10)
   - Product dispense verification
5. Servo Motor
    - Refund mechanism
6. Tactile Buttons
    - Product selection & controls 
7. Buzzer
    - audio feedback
8. Jumper Wires
    - Connections
9. Breadboard
    - Component mounting
  

**Wiring Diagram**

<img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/baf68fdc-bf58-4e98-9ef5-ba6e9e6f3662" />

**Installation & Setup**
**1. Hardware Assembly**
  Step 1: Prepare the Arduino
    Install Arduino Mega 2560 on breadboard or mounting plate
    Connect 12V power supply (ensure common ground)
    Test basic power-up (onboard LED should light up)

  Step 2: LCD Connection
    Connect LCD following pin configuration above
    Adjust potentiometer for optimal contrast
    Upload simple LCD test sketch to verify

  Step 3: Coin Detection Setup

    Mount IR sensors at coin insertion slot
    Position sensors to detect ₱5 and ₱10 coin sizes
    Test with actual coins and adjust sensor sensitivity
    Secure sensors to prevent movement

  Step 4: Motor Installation

    Connect L298N drivers to Arduino
    Wire DC motors to motor drivers
    Test rotation direction (adjust IN pins if needed)
    Mount motors to spiral coil mechanisms
    Calibrate rotation time for single dispense

  Step 5: Product Detection

    Install vibration sensors below each dispenser
    Position to detect falling products
    Test sensitivity with actual products
    Fine-tune threshold in code

  Step 6: Control Buttons & Refund

    Wire push buttons with pull-down resistors
    Connect servo motor for refund mechanism
    Test button responsiveness
    Verify servo movement range

**2. Software Installation**
  Prerequisites:
  - Arduino IDE 1.8.x or newer
  - USB cable for Arduino Mega
  - Required libraries (see below)

  Step 1: Install Arduino IDE
    1. Download from https://www.arduino.cc/en/software
    2. Install for your operating system
    3. Launch Arduino IDE

  Step 2: Install Required Libraries
    Via Library Manager (Sketch > Include Library -> Manage Libraries):
      - LiquidCrystal (built-in, for LCD control)
      - Servo (built-in, for refund mechanism)

Step 3: Clone & Upload Code
    git clone https://github.com/raizen76/Arduino-Vending-Machine.git
    # Open Arduino IDE
      1. File → Open → vending_machine.ino
      2. Tools → Board → Arduino Mega 2560
      3. Tools → Port → Select your Arduino port (COM3, /dev/ttyUSB0, etc.)
      4. Click Upload (→) button
Step 4: Configure Settings
    Edit these parameters in the code based on your setup:
      // In vending_machine.ino
      #define COIN_5_PIN 8           // ₱5 coin sensor
      #define COIN_10_PIN 9          // ₱10 coin sensor
      #define DISPENSE_TIME 2000     // Motor run time (ms)
      #define TRANSACTION_TIMEOUT 30000  // 30 seconds
      #define PRODUCT_A_PRICE 10     // Price in pesos
      #define PRODUCT_B_PRICE 15
      #define PRODUCT_C_PRICE 20
**3. Testing & Calibration**
    Initial Testing:
      1. Power on the system
      2. Verify LCD displays welcome message
      3. Test coin detection with real coins
      4. Verify credit display on LCD
      5. Test button selection
      6. Confirm motor dispensing
      7. Check product detection
      8. Test refund mechanism

      Calibration:
       - Adjust DISPENSE_TIME for complete product release
      - Tune vibration sensor sensitivity
      - Calibrate servo angles for coin return
      - Fine-tune timeout duration

**System Flow Diagram**

<img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/a4c6fe3b-5e43-4d59-a0b8-02c427531973" />









