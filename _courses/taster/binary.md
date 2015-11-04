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


##########

  
  - title: hardware

    notes: |

      LED, Button, Wires

    content: |

      ## Bits We Need

      LED, Button, Wires


###########


  - title: output

    notes: |

      Set up your LED as in the diagram.

    content: |

      ## Connecting Your Output

      Set up your LED as in the diagram.


##########


  - title: testoutput

    notes: |

      Check that your LED works by turning it on.

    content: |

      ## Testing Your Output

      Check that your LED works by turning it on.

      Your LED should turn on and stay on.
      {: .checkpoint}


##########


  - title: input

    notes: |

      Set up your button as in the diagram.

    content: |

      ## Connecting Your Input

      Set up your button as in the diagram.


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

      ![Thumbs Up!]([[THEME_IMAGES]]/thumbs-up.svg)
      <!-- .element height="200" -->

      ## Binary Blink: Complete!

      Cool, now let's try something a little more complex...

      [Take me to the next chapter!](spectrum)

---
