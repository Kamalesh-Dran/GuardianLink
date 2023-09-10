
# GuardianLink

Hand Signal Communication System for Defence with Sender and Receiver Gadget (Special Gloves)


## Objective

* The aim is to develop a communication kit to transmit the message signal to the subordinate gadget.
* The main person who wants to transmit the message will have special gloves which contains sensors to detect the motion of the hand.
* And then this motion is detected which is then predicted through ML model and then the message is sent through the RF transreceiver to the receiver end.
## Literature Review

* Saggio, G., Cavrini, F. and Pinto, C.A., 2015, November. Recognition of arm-andhand visual signals by means of SVM to increase aircraft security. In International Joint Conference on Computational Intelligence (pp. 444-461). Springer, Cham.
* Aaisha, P. and Rohitha, U.M., 2015. Microcontroller based hand gesture recognition system using flex sensor for disabled people. International Journal of Computer Applications, pp.975-8887. 
* Merelo, J. J., Rosa, A., Cadenas, J. M., Correia, A. D., Madani, K., Ruano, A., &  Filipe, J. (Eds.). (2017). Computational Intelligence. Studies in Computational  Intelligence. doi:10.1007/978-3-319- 48506- 
*  Akash Kumar Panda;Rommel Chakravarty;Soumen Moulik; (2021). Hand Gesture Recognition using Flex Sensor and Machine Learning Algorithms . 2020 IEEEEMBS Conference on Biomedical Engineering and Sciences (IECBES). doi:10.1109/IECBES48179.2021.9398789


## Hardware / Software Requirements

### Hardware:

* Flex Sensors – 5
* MPU 6050 – 1
* Arduino Nano – 1
* Arduino Uno - 1
* NRF24L01 2.4GHz Transceiver
* Gloves and Jumper Wires
* OLED Display 1.3 inch

### Software:

* Laptop/PC
* PyCharm IDE
* Firebase Database
* Arduino IDE
* PLX DAQ Data Logger
## Architecture of Proposed System

![Transmitter](https://github.com/Kamalesh-Dran/GuardianLink/assets/88824460/64397050-889b-4a2a-bd33-6eda0a015738)
![Receiver](https://github.com/Kamalesh-Dran/GuardianLink/assets/88824460/397c21d7-cb33-446a-a2aa-340fe436a210)



## Methodology

* Firstly we will get data from all the flex sensors which will indicate the position of the fingers and then the data from the MEMS Sensor which will give the roll, pitch, and yaw to know the position of the wrist.
* For each Communication/Hand Signal/gesture we will collect the data which will be used for training our model.
* Here for testing we will take 9 different Hand Signals and train using random forest classifier algorithm.
* Here to capture the data from arduino nano and then to store it in excel we will use PLX DAQ Software
* Now to predict the live data we have to transfer the data from Arduino nano to the pycharm IDE for which we will use pyserial library in python to read the serial data from the PORT to which the controller is attached with.
* Then we will use the sklearn library to train the random forest and for feature scaling to quickly predict the output.
* After prediction the output is again sent to the controller using pyserial library function and then the message is transmitted to the sub-ordinate controller with the help of radio transceiver which then is displayed on the OLED display

## Performance Metrics

This project is implemented using random forest classifier machine learning algorithm and it provides an accuracy of 90% in predicting the output for the hand gestures. If we use other machine learning algorithms, the performance would vary and the accuracy score of naïve bayes algorithm is about 87%. The accuracy score of k-nearest neighbors’ classifier is 84%. These are all the performance of some machine learning algorithms. In this the best performance was given by random forest classifier hence we used it for our IoT project
## Results and Discussion

* In our project, the data collected from the flex sensors indicates the position of the fingers and the data from the MEMS sensor indicates the position of the wrist. The data from Arduino Nano is collected and stored in an excel sheet using PLX DAQ software.
* PySerial library is used to collect the live data from Arduino Nano into the PyCharm IDE. We have used random forest classifier for training the model and the model has been trained to test 9 different hand signals. The sklearn library has been used to train the random forest and for feature scaling to quickly predict the output.
* Once the output is predicted, the data is sent back to the controller using the same Pyserial library and the data is displayed on the OLED display. We canconclude that a successful attempt was made to develop a handsignal communication kit wherein we are able to determine thehand signal using a different set of sensors and a controller.
* We implemented a machine learning model for predicting the signal whilst storing the information in a database. Hence, we fulfilled the aim of the project i.e. to develop a communicationkit to transmit the message signal to the subordinate gadget.


## Conclusion

* This project aims to lower the communication gap between the mute community and additionally the standard world. The projected methodology interprets language into speech. The system overcomes thenecessary time difficulties of dumb people.
* Compared with existing system the projected arrangement is compact and is possible to carry to any places i.e. portable. This system converts the language in associate voice that’s well understand by blind and ancient people.
* In world applications, this system is helpful for deaf and dumb of us those cannot communicate with ancient person. It’s in addition useful for speech impaired and paralysed patient means those do not speak properly and in addition used for Intelligent Home Applications and industrial application
