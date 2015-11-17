---
layout: chapter
title: Accelerator
slides:

  - title: title-page
    class: title-slide

    notes: |

      :)

    content: |

      ![Gather Workshops Logo]([[THEME_IMAGES]]/gw_logo.png)

      # Accelerator
      _Control motor speed via a touchpad_


##########


  - title: overview

    notes: |
      Change the colour of a light by turning a dial.

    content: |

      ## What We Are Making

      A motor which will spin based on 
      a speed reading from a soft touch pad.


##########


  - title: hardware

    notes: |

      Motor, Transistor, Diode, 330&#937; Resistor

      Soft Potentiometer, 10k Resistor, Wires

    content: |

      ## Bits We Need

      - ![Motor]([[COURSE_IMAGES]]/slidecontent/arduino-motor.png){: height="200"}
        **Motor**
        The visual output for our circuit
      - ![Transistor]([[COURSE_IMAGES]]/slidecontent/arduino-transistor.png){: height="200"}
        **Transistor**
        To amplify the current to the motor
      - ![Diode]([[COURSE_IMAGES]]/slidecontent/arduino-diode.png){: height="200"}
        **Diode**
        A one-way valve for the current
      - ![330 Ohm Resistor]([[COURSE_IMAGES]]/slidecontent/arduino-resistor-330ohm.svg){: height="200"}
        **330&#937; Resistor**
      {:.flex-list}

      - ![Soft Potentiometer]([[COURSE_IMAGES]]/slidecontent/arduino-soft-potentiometer.png){: height="200"}
        **Soft Potentiometer**
      - ![10k Resistor]([[COURSE_IMAGES]]/slidecontent/arduino-resistor-10k.svg){: height="200"}
        **10k Resistor**
      - ![Wire]([[COURSE_IMAGES]]/slidecontent/arduino-wire.svg){: height="200"}
        **Wires**
        To connect everything together!
      {:.flex-list}



###########


  - title: motor-overview

    notes: |

      :)

    content: |

      ## Motor Overview

      Setting up our motor will once again consist of two parts:
      the physical components, and the logical components


###########


  - title: motor-info-sheet
    class: info-sheet-slide

    notes: |

      :)

    content: |

      ![Motor Diagram]([[COURSE_IMAGES]]/slidecontent/arduino-motor.png){: height="450"}

      ## Motor

      The motor's speed is determined by the voltage you put through it.


###########


  - title: transistor-info-sheet
    class: info-sheet-slide

    notes: |

      :)

    content: |

      ![Transistor Diagram]([[COURSE_IMAGES]]/slidecontent/arduino-transistor.png){: height="450"}

      ## Transistor


###########


  - title: diode-info-sheet
    class: info-sheet-slide

    notes: |

      :)

    content: |

      ![Diode Diagram]([[COURSE_IMAGES]]/slidecontent/arduino-diode.png){: height="450"}

      ## Diode    


###########


  - title: motor-physical-components

    notes: |

      Set up your LED as in the diagram.

    content: |

      ## Physical Components <br>of the Motor Circuit

      ![Motor wiring diagram]([[COURSE_IMAGES]]/slidecontent/accelerator-motor-wiring-diagram.svg){: height="550"}

      Set up your motor as in the diagram.


##########


  - title: led-logical-components

    notes: |

      Check that your LED works by turning it on.

    content: |

      ## Logical Components <br>of the LED Circuit

      - ![Test Buttons]([[COURSE_IMAGES]]/slidecontent/spectrum-led-nodered-inject.png){: height="200"}
        **Test Buttons**
        On-screen buttons, one for each 
        LED colour component.
      - ![Arduino Outputs]([[COURSE_IMAGES]]/slidecontent/spectrum-led-nodered-arduino-out.png){: height="200"}
        **Light Output**
        One Arduino pin output for each
        LED colour component.
      {:.flex-list}


##########


  - title: led-out-node

    notes: |

      Drag an `arduino out` node into your workspace and configure it.

      This will pass a message to the configured pin, but will not run automatically. We need to trigger it.

    content: |

      ## Pass a Message Out to the Arduino

      ![LED Node Configuration]([[COURSE_IMAGES]]/slidecontent/spectrum-led-arduino-node.png){: height="450"}

      Drag an `arduino out` node into your workspace and configure it.


##########


  - title: led-inject-node

    notes: |

      Drag an `inject` node into your workspace and configure it.

    content: |

      ## Inject a Message

      ![Inject Node Configuration]([[COURSE_IMAGES]]/slidecontent/spectrum-led-inject-node.png){: height="450"}

      Drag an `inject` node into your workspace and configure it.


##########


  - title: led-join-nodes

    notes: |

      Connect the two nodes.

    content: |

      ## Connect the nodes

      ![Inject Node Configuration]([[COURSE_IMAGES]]/slidecontent/spectrum-led-join-nodes.png){: height="450"}

      Click and drag the small square on the `inject` node,
      and attach it to the `arduino out` node.


##########


  - title: led-deploy

    notes: |

      :)

    content: |

      ## Deploy Your Code

      ![Deploying Node Red code to the Arduino]([[COURSE_IMAGES]]/slidecontent/nodered-deploy-code.png)

      Click the "Deploy" button in Node Red
      to link your logic flow with the Arduino.


##########


  - title: led-test

    notes: |

      Check that your LED works by turning it on.

    content: |

      ## Test the LED Output

      Click the square trigger button on the `inject` node.

      Your LED should turn red.
      {: .checkpoint}


##########


  - title: led-all-colours-test

    notes: |

      Check that your LED works by turning it on.

    content: |

      ## Test Green and Blue 

      ![Multiple Inject Nodes]([[COURSE_IMAGES]]/slidecontent/spectrum-led-all-colors-test.png){: height="450"}

      Add two more flows to test the green and blue.

      The test buttons should all work correctly.
      {: .checkpoint}


###########


  - title: potentiometer-overview

    notes: |

      :)

    content: |

      ## Potentiometer Overview

      Setting up our potentiometer will also consist of two parts:
      the physical components, and the logical components


##########


  - title: potentiometer-physical-components

    notes: |

      Set up your potentiometer as in the diagram.

    content: |

      ## Physical Components <br>of the Potentiometer Circuit

      ![Potentiometer wiring diagram]([[COURSE_IMAGES]]/slidecontent/spectrum-potentiometer-wiring-diagram.svg){: height="550"}

      Set up your potentiometer as in the diagram.


##########


  - title: potentiometer-logical-components

    notes: |

      :)

    content: |

      ## Logical Components <br>of the Potentiometer Circuit

      - ![Arduino In]([[COURSE_IMAGES]]/slidecontent/spectrum-potentiometer-nodered-arduino.png){: height="200"}
        **Potentiometer Input**
        Converts the Arduino signal
        into a JavaScript message.
      - ![Debug Node]([[COURSE_IMAGES]]/slidecontent/spectrum-potentiometer-nodered-debug.png){: height="200"}
        **Debug Logger**
        Displays the JS message on
        the screen when received.
      {:.flex-list}


##########


  - title: potentiometer-arduino-node

    notes: |

      Drag an `arduino out` node into your workspace and configure it.

      This will pass a message to the configured pin, but will not run automatically. We need to trigger it.

    content: |

      ## Receive a Message from the Arduino

      ![Button Input Node Configuration]([[COURSE_IMAGES]]/slidecontent/spectrum-potentiometer-arduino-node.png){: height="450"}

      Drag an `arduino in` node into your workspace and configure it.


##########


  - title: potentiometer-debug-node

    notes: |

      Drag a `debug` node into your workspace and configure it.

    content: |

      ## Debug the Incoming Data

      ![Button Debug Node Configuration]([[COURSE_IMAGES]]/slidecontent/spectrum-potentiometer-debug-node.png){: height="450"}

      Drag a `debug` node into your workspace. The default configuration is fine.


##########


  - title: potentiometer-join-nodes

    notes: |

      Connect the two nodes.

    content: |

      ## Connect the nodes

      ![Join potentiometer Nodes]([[COURSE_IMAGES]]/slidecontent/spectrum-potentiometer-join-nodes.png){: height="450"}

      Join your `arduino` node to your `debug` node.


##########


  - title: potentiometer-code-deploy

    notes: |

      :)

    content: |

      ## Deploy Your Code

      ![Deploying Node Red code to the Arduino]([[COURSE_IMAGES]]/slidecontent/nodered-deploy-code.png)

      Click the "Deploy" button in Node Red
      to link your logic flow with the Arduino.


##########


  - title: potentiometer-test

    notes: |

      :)

    content: |

      ## Test the potentiometer input

      Turn the dial on your potentiometer.

      You should see value being logged in your debug panel.
      {: .checkpoint}


##########


  - title: circuit-logical-components

    notes: |

      :)

    content: |

      ## Logical Components <br>of the whole circuit

      - ![Arduino In]([[COURSE_IMAGES]]/slidecontent/spectrum-potentiometer-nodered-arduino.png){: height="200"}
        **Potentiometer Input**
        Receives an Arduino signal
        as a JavaScript message.
      - ![Function]([[COURSE_IMAGES]]/slidecontent/spectrum-circuit-nodered-function.png){: height="200"}
        **Conversion Function**
        Converts the potentiometer signal into the correct message for the LED.
      - ![Arduino Outputs]([[COURSE_IMAGES]]/slidecontent/spectrum-led-nodered-arduino-out.png){: height="200"}
        **LED Outputs**
        Sends the JavaScript message
        as an Arduino signal.
      {:.flex-list}


##########


  - title: circuit-arduino-nodes

    notes: |

      :)

    content: |

      ## Circuit Arduino Nodes

      ![Full Circuit with all nodes]([[COURSE_IMAGES]]/slidecontent/spectrum-circuit-all-nodes.png)

      Link your `arduino input` to the three `arduino output` nodes
      via a `function`, like we did last time.

      This time your function requires three outputs instead of one.


##########


  - title: circuit-function-code

    notes: |

      We don't need to store the state this time.

    content: |

      ## Function Code

      ```javascript
      var dialValue = msg.payload;
      var redOn = false;
      var greenOn = false;
      var blueOn = false;

      if(dialValue < 300){
          redOn = true;
      } else if(dialValue > 900) {
          blueOn = true;
      } else {
          greenOn = true;
      }

      var redMessage = { payload: redOn };
      var greenMessage = { payload: greenOn };
      var blueMessage = { payload: blueOn };

      return [redMessage, greenMessage, blueMessage];
      ```

      Paste this code into your `function` config popup,
      in the code editor section.


##########


  - title: circuit-function-code-shorter

    notes: |

      We don't need to store the state this time.

    content: |

      ## Shorter Function Code

      ```javascript
      var dialPosition = msg.payload;

      var messages = [
          {payload: (dialPosition <= 300)}, // red
          {payload: (dialPosition > 300 && dialPosition < 900)}, // green
          {payload: (dialPosition >= 900)} //blue
      ]

      return messages;
      ```
      **For experienced coders:**
      This code does exactly the same thing,
      but is a bit shorter.


##########

  - title: circuit-deploy

    notes: |

      :)

    content: |

      ## Deploy Your Code

      ![Deploying Node Red code to the Arduino]([[COURSE_IMAGES]]/slidecontent/nodered-deploy-code.png)

      Click the "Deploy" button in Node Red
      to link your logic flow with the Arduino.


##########

  - title: circuit-test

    notes: |

      :)

    content: |

      ## Full Circuit Test

      Turn the dial to change the colour of your LED.

      Your potentiometer should now act like a colour picker.
      {:.checkpoint}


##########


  - title: challenge

    notes: |

      Add another LED to your circuit to make a stop/go light.

    content: |

      ![Spectrum Mood Light]([[COURSE_IMAGES]]/slidecontent/spectrum-cat.gif){: height="350"}

      ## Challenge: Mood Lighting

      Modify the conversion function to output 5 or more colours.

      **Bonus points:** Fade the LED through a continuous spectrum.



##########


  - title: summary
    class: centered-slide

    notes: |

      Cool, now let's try something a little more complex...

    content: |

      ![Thumbs Up!]([[THEME_IMAGES]]/thumbs-up.svg){:height="200"}

      ## Spectrum Spinner: Complete!

      Yay, onwards to the next adventure...

      [Take me to the next chapter!](flexor)

---
