
# Doctor Appointment Chatbot

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  <!-- Replace with your actual license badge link and license -->

This project is a Doctor Appointment Chatbot that allows users to book, reschedule, and cancel doctor appointments based on their symptoms through a chat interface. After booking, users receive a confirmation email.

## Features

- Chat-based interaction to manage doctor appointments
- Suggests doctors based on user symptoms
- Confirms appointment booking via email
- Reschedules and cancels appointments

## Requirements

To install the necessary dependencies, follow these steps:

1.  **Create a `requirements.txt` file:** In the root directory of the project, create a new text file named `requirements.txt`.

2.  **Add the dependencies:** Open `requirements.txt` in a text editor and paste the following dependencies into it:

    ```
    smtplib
    datetime
    email
    pandas
    random
    re
    os
    difflib
    streamlit
    kagglehub
    ```

3.  **Install the dependencies:** Open a terminal or command prompt, navigate to the project directory, and run the following command:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/MVivekananda/Doctor_Appointment_Chatbot.git
       # Make sure to fork this, then clone from your forked repository
   cd Doctor_Appointment_Chatbot
2. Run the Streamlit application:
   ```bash
   streamlit run infosys.py
   ```
   This command will start the Streamlit application, which hosts the chatbot. `infosys.py` is the main script that contains the chatbot's logic and interface.

3. Interact with the chatbot to book, reschedule, or cancel doctor appointments.

## Appointment Booking Workflow

1. **Start Chat**: User initiates the chat.
2. **Symptom Input**: User enters their symptoms.
3. **Doctor Suggestion**: Bot suggests doctors based on symptoms.
4. **Doctor Selection**: User selects a doctor.
5. **Appointment Details**: User provides details like name, email, mobile number, date, and time.
6. **Confirmation**: Bot confirms the appointment and sends a confirmation email to the user. **(Appointment booking successful if all the above steps are correct and complete, or else it fails)**

## Example

1. **Start Chat**:
   ```
   User: Hi, I want to book an appointment.
   Bot: Welcome to the Hospital Appointment System! How can I assist you today?
   ```

2. **Symptom Input**:
   ```
   User: I have a fever.
   Bot: Based on your symptoms, we recommend a General Physician.
   ```

3. **Doctor Selection**:
   ```
   Bot: Here are the available doctors:
   1. Dr. John Doe
   2. Dr. Jane Smith
   User: 1
   ```

4. **Appointment Details**:
   ```
   Bot: What's your name?
   User: Alice
   Bot: What's your email address?
   User: alice@example.com
   Bot: What's your mobile number?
   User: 1234567890
   Bot: When would you like to book the appointment? (YYYY-MM-DD)
   User: 2025-03-10
   Bot: What time would you like to book the appointment? (HH:MM AM/PM)
   User: 10:30 AM
   ```

5.  KaggleHub credits the data that are used to train the ML model is from 100k Health Records and Report:
    This dataset contains over 100,000 health records and reports, providing a comprehensive view of patient information and medical history.

6.  **Confirmation**:
    ```
    Bot: Appointment booked successfully! Confirmation email sent.
    ```
    **IMPORTANT: Please note that these are example interactions. The chatbot's responses are primarily scripted and may not handle all possible inputs. The appointment booking system is not connected to a real EHR. It is trained with 100k Health Records and Reports data that are found in KaggleHub. It is credited under MIT License.**

## Limitations

This chatbot has the following limitations:

*   The responses are primarily scripted and do not generate dynamic or personalized text.
*   The intent recognition is basic and may not accurately understand complex user requests.
*   The chatbot is not integrated with any real-time doctor schedules or appointment booking systems.
*   It does not handle edge cases, ambiguous requests, or unexpected inputs gracefully.

## Live Demo [![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://saydoc-appointment-chatbot.streamlit.app/) 

Try out the SayDoc Doctor Appointment Chatbot live at: [https://saydoc-appointment-chatbot.streamlit.app/](https://saydoc-appointment-chatbot.streamlit.app/)



## Project Workflow

```mermaid
sequenceDiagram
    participant User
    participant Chatbot
    participant Database
    participant EmailService

    User->>Chatbot: Hi, I want to book an appointment.
    Chatbot->>Chatbot: Identify intent (Book Appointment).
    Chatbot->>User: What are your symptoms?
    User->>Chatbot: I have a fever.
    Chatbot->>Chatbot: Suggest doctors based on symptoms.
    Chatbot->>User: Based on your symptoms, we recommend a General Physician.
    User->>Chatbot: 1 (Selects Dr. John Doe).
    Chatbot->>User: What's your name?
    User->>Chatbot: Alice.
    Chatbot->>User: What's your email address?
    User->>Chatbot: alice@example.com
    Chatbot->>User: What's your mobile number?
    User->>Chatbot: 1234567890
    Chatbot->>User: When would you like to book the appointment? (YYYY-MM-DD)
    User->>Chatbot: 2025-03-10
    Chatbot->>User: What time would you like to book the appointment? (HH:MM AM/PM)
    User->>Chatbot: 10:30 AM
    Chatbot->>Chatbot: Validate details and schedule appointment.
    Chatbot->>Database: Save appointment details.
    Chatbot->>EmailService: Send confirmation email to User.
    Chatbot->>User: Appointment booked successfully! Confirmation email sent.
```
## Technologies Used

This project is built using the following technologies:

[![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=fff)](#)        [![Visual Studio Code](https://custom-icon-badges.demolab.com/badge/Visual%20Studio%20Code-0078d7.svg?logo=vsc&logoColor=white)](#)
![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)        [![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=fff)](#)
[![Flask](https://img.shields.io/badge/Flask-000?logo=flask&logoColor=fff)](#)              [![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=fff)](#)
[![Windows](https://custom-icon-badges.demolab.com/badge/Windows-0078D6?logo=windows11&logoColor=white)](#)    [![npm](https://img.shields.io/badge/npm-CB3837?logo=npm&logoColor=fff)](#)
[![CSS](https://img.shields.io/badge/CSS-1572B6?logo=css3&logoColor=fff)](#)            [![HTML](https://img.shields.io/badge/HTML-%23E34F26.svg?logo=html5&logoColor=white)](#)        [![Markdown](https://img.shields.io/badge/Markdown-%23000000.svg?logo=markdown&logoColor=white)](#)        [![Gmail](https://img.shields.io/badge/Gmail-D14836?logo=gmail&logoColor=white)](#)        [![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-121013?logo=github&logoColor=white)](#)        [![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=fff)](#)

## License [![GitHub license](https://badgen.net/github/license/Naereen/Strapdown.js)](https://github.com/Naereen/StrapDown.js/blob/master/LICENSE)
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
