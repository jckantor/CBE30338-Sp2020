# Final Project: Prototyping a Control System for a PCR Thermal Cycler

For the final projec you are to implement a control system prototype for a PCR Thermal Cycler in Python, and test your implementation using the Temperature Control Laboratory. You be assessed by how well the design fullfils the control system requirements.

You are encouraged to use your engineering judgement and creativity in meeting the device requirements, including decisions on the choice of control algorithms, design of the software implementation, and design of the user interface.  

## PCR Thermal Cycler Requirements

### Protocol Requirements

The PCR Thermal Cycler should be capable of performing two PCR amplification protocols at the same time. The specifications for each amplification protocol are as follows:

1. Start. The amplification protocol starts at ambient temperature.
1. Initial Denaturation. The denaturation setpoint will be a value in the range from 92-98 deg C and for a period of 60-120 seconds determined by the user. The same temperature setpoint will apply to all subsequent denaturation cycles. 
1. PCR Thermal cycles. The user should be able to specify up to 30 PCR cycles. (To save time, you only need to test performance for only 3 cycles.) Each cycle consists of
    * Annealing.  A user determined temperature between 50 deg C and 65 deg C for user determined period from 30 to 120 seconds.
    * Extension. A user determined temperature of 68-72 deg C for a period from 30-180 seconds.
    * Denaturation.  At the same temperature as the initial denaturation for a user determined period of 30-120 seconds.
1. Final Extension. The protocol finishes with a final extension step that can be user determined from 30-300 seconds. 
1. Finish. Following the final extension, the temperature should return to ambient temperature and present a message to the user indicating completion.

### User Interface Requirements

Your prototype should consist of three Jupyter notebooks.

1. Protocol UI. The user settings for PCR thermal protocols will be determined before the start of an experiment. The protocols should be saved in a separate file, and be able to be viewed by the user. 

2. Runtime UI.  The runtime notebook should allow the user to select a saved protocol for each of the two heaters. The user should be able to view the selected protocols. Once the protocols have been selected, the PCR run should commence with the click of a start button and run until either (1) normal completion or (2) the user presses a stop button. A record of the run should be recorded to a data file.

3. Review UI.  The user should be able to retrieve and review the data recorded from a prior run of the PCR thermal cycler.

### Control Algorithm

The purpose of the control system is to cause the sensed temperatures of two heater/sensor assemblies in temperature control laboratory to track the desired protocols with as little setpoint error, and to complete the protocol as quickly as possible. The goals are:

1. Maintain sensor temperature to within 2 degrees of the specified temperature protocols, and 
1. Complete 3 cycles as quickly as possible. For testing purposes, the specified protocol should be:
    * Initial denaturation at 94 for 90 seconds.
    * 3 subsequent PCR cycles (annealing at 60 deg C for 60 seconds, extension at 72 deg for 90 seconds, denaturation at 94 deg for 60 seconds)
    * After the third extension, the experiment should finish by returning to ambient temperature with a message to the user after cooling below 30 deg C. 
    * The message should indicate the time required to complete the experiment.

Your control implementation may use P, PI, PID, or model predictive control. You may find it useful to implement a state estimator. If so, the state estimator should be implemented as in a separate function/generator from the other control elements.

### Submission

Your submission should consist of three Jupyter notebooks as outlined above, and a separate report describing the elements of your project.

The submission is due via Sakai by 12:30 pm on Friday, May 8th.

## Assessment

The assessment will be based on the degree to which your project fullfils the product requirements. This is a design project, you're encouraged to think creatively about the application and control system implementation. 

It is also a challenging project. If you find that you are unable to meet every requirement, specify in your report where you chose to focus your efforts and the elements that would be needed to complete the prototype.

If you have an idea on how to improve the project, you are welcome to pursue the idea and will be rewarded for creative effort. But please contact the instructor before spending inordinate time or adding inordinate risk to the project.

## Group vs Individual Work

The wildly uneven access to internet resources, coding support, and study environment makes it difficult to fairly evaluate individual effort in term projects conducted in a distance learning environment. So here are some gound rules:

* You may work in small groups. The groups should involve no more than 3 people (please don't ask for exceptions). Groups will be expected to fullfill all elements of the project.  

* If you do work in a group, please notify the instructor in advance, and no later than 11am on Tuesday, April 28th. The final report should include a section with the names of the group members and describing their contributions.

* If you do not work in a group and find the project overwhelming, please contact the instructor no later than Monday, May 4th (regular weekly office hours) to discuss ways to narrow the scope of the project.
