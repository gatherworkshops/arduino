---
layout: chapter
title: Binary Blink
slides:

  - title: title-page
    class: title-slide

    notes: |

      Welcome to Electronics with Arduino!

      This taster is designed to introduce you to the basics of sensor input and real-world output using Arduino.

      By the end of the workshop you will have built and coded a selection of small electronics demo projects.

    content: |

      ![Gather Workshops Logo]([[THEME_IMAGES]]/gw_logo.png)

      # Binary Blink
      _Light on, light off._


##########


  - title: overview

    notes: |
      Turn a light on and off by pushing a button.

    content: |

      ## What We Are Making

      Turn a light on and off by pushing a button.

      <iframe frameborder='0' height='448' marginheight='0' marginwidth='0' scrolling='no' src='https://123d.circuits.io/circuits/1195802-the-unnamed-circuit/embed#breadboard' width='650'></iframe>


##########


  - title: hardware

    notes: |

      LED, Button, Wires

    content: |

      ## Bits We Need

      - ![Red LED]([[COURSE_IMAGES]]/slidecontent/led-red.svg){: height="100"}
        **LED**
        A visual output for our circuit
      - ![Button]([[COURSE_IMAGES]]/slidecontent/button.svg){: height="100"}
        **Button**
        An input, used to turn our light on and off
      - ![10k Ohm Resistor]([[COURSE_IMAGES]]/slidecontent/resistor-10k.svg){: height="100"}
        **10k Resistor**
        To regulate the voltage readings from the button
      - ![Wire]([[COURSE_IMAGES]]/slidecontent/wire.png){: height="100"}
        **Wires**
        To connect everything together!
      {:.flex-list}


###########


  - title: led-overview

    notes: |

      :)

    content: |

      ## LED Overview

      Setting up our LED will consist of two parts:
      the physical components, and the logical components


###########


  - title: led-physical-components

    notes: |

      Set up your LED as in the diagram.

    content: |

      ## Physical Components <br>of the LED Circuit

      ![Output wiring diagram]([[COURSE_IMAGES]]/slidecontent/binaryblink-output-wiring-diagram.svg){: height="550"}

      Set up your LED as in the diagram.


##########


  - title: led-logical-components

    notes: |

      Check that your LED works by turning it on.

    content: |

      ## Logical Components <br>of the LED Circuit

      - ![Test Button]([[COURSE_IMAGES]]/slidecontent/test-button.svg){: height="200"}
        **Test Button**
        On-screen button, sends message
        that light should turn on.
      - ![Arduino Out]([[COURSE_IMAGES]]/slidecontent/arduino-out.svg){: height="200"}
        **Light Output**
        Converts test button message
        into an Arduino signal.
      {:.flex-list}


##########


  - title: led-out-node

    notes: |

      Drag an `arduino out` node into your workspace and configure it.

      This will pass a message to the configured pin, but will not run automatically. We need to trigger it.

    content: |

      ## Pass a Message Out to the Arduino

      ![LED Node Configuration]([[COURSE_IMAGES]]/slidecontent/led-node-config.png){: height="450"}

      Drag an `arduino out` node into your workspace and configure it.


##########


  - title: output-inject-node

    notes: |

      Drag an `inject` node into your workspace and configure it.

    content: |

      ## Inject a Message

      ![Inject Node Configuration]([[COURSE_IMAGES]]/slidecontent/inject-node-config.png){: height="450"}

      Drag an `inject` node into your workspace and configure it.


##########


  - title: output-join-nodes

    notes: |

      Connect the two nodes.

    content: |

      ## Connect the nodes

      ![Inject Node Configuration]([[COURSE_IMAGES]]/slidecontent/binaryblink-output-join-nodes.png){: height="450"}

      Click and drag the small square on the `inject` node,
      and attach it to the `arduino out` node.


##########


  - title: output-deploy

    notes: |

      Drag an `inject` node into your workspace and configure it.

    content: |

      ## Deploy Your Code

      ![Deploying Node Red code to the Arduino]([[COURSE_IMAGES]]/slidecontent/deploy-code.png)

      Click the "Deploy" button in Node Red
      to link your logic flow with the Arduino.


##########


  - title: output-test

    notes: |

      Check that your LED works by turning it on.

    content: |

      ## Test the LED Output

      Click the square trigger button on the `inject` node.

      Your LED should turn on and stay on.
      {: .checkpoint}


###########


  - title: button-overview

    notes: |

      :)

    content: |

      ## Button Overview

      Setting up our button will also consist of two parts:
      the physical components, and the logical components


##########


  - title: button-physical-components

    notes: |

      Set up your button as in the diagram.

    content: |

      ## Physical Components <br>of the Button Circuit

      ![Output wiring diagram]([[COURSE_IMAGES]]/slidecontent/binaryblink-input-wiring-diagram.svg){: height="550"}

      Set up your button as in the diagram.


##########


  - title: button-logical-components

    notes: |

      :)

    content: |

      ## Logical Components <br>of the Button Circuit

      - **Button Input**
        Converts the Arduino signal
        into a JavaScript message.
      - **Debug Logger**
        Displays the JS message on
        the screen when received.
      {:.flex-list}


##########


  - title: testinput

    notes: |

      Check that your button works by tracing its value in your browser.

    content: |

      ## Testing Your Input

      Check that your button works by tracing its value in your browser.

      Your button value should change each time you press it.
      {: .checkpoint}


##########


  - title: visualflow

    notes: |

      Use flowchart blocks to pass your button input to your LED output via a function.

    content: |

      ## Data Flow Chart

      Use flowchart blocks to pass your button input to your LED output via a function.


##########


  - title: function

    notes: |

      Use a function to convert the button's voltage reading to an on/off message for the LED.

    content: |

      ## Conversion Function

      Use a function to convert the button's voltage reading to an on/off message for the LED.


##########

  - title: context

    notes: |

      We can use the `context` object to store the state.
      This allows us to toggle on/off with the button.

    content: |

      ## Storing State

      ```javascript
      if(context.lighton === undefined) {
          context.lighton = false;
      }
      
      if(msg.payload === true) {
          context.lightOn = !context.lightOn;
          msg.payload = context.lightOn;
      }

      return msg;
      ```

      We can use the `context` object to store the state.
      This allows us to toggle on/off with the button.


##########


  - title: challenge

    notes: |

      Add another LED to your circuit to make a stop/go light.

    content: |

      ## Challenge: Stop and Go

      Add another LED to your circuit to make a stop/go light.



##########


  - title: summary
    class: centered-slide

    notes: |

      Great! Now that's all sorted, let's get started!

    content: |

      ![Thumbs Up!]([[THEME_IMAGES]]/thumbs-up.svg){:height="200"}

      ## Binary Blink: Complete!

      Cool, now let's try something a little more complex...

      [Take me to the next chapter!](spectrum)

---
