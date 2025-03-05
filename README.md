# Doctor Appointment Chatbot

This project is a Doctor Appointment Chatbot that allows users to book, reschedule, and cancel doctor appointments based on their symptoms through a chat interface. After booking, users receive a confirmation email.

## Features

- Chat-based interaction to manage doctor appointments
- Suggests doctors based on user symptoms
- Confirms appointment booking via email
- Reschedules and cancels appointments

## Requirements

Create a `requirements.txt` file with the following content:

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

Then run:

```bash
pip install -r requirements.txt
```

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/MVivekananda/saydoc.git
   cd saydoc
   ```

2. Run the Streamlit application:
   ```bash
   streamlit run infosys.py
   ```

3. Interact with the chatbot to book, reschedule, or cancel doctor appointments.

## Appointment Booking Workflow

1. **Start Chat**: User initiates the chat.
2. **Symptom Input**: User enters their symptoms.
3. **Doctor Suggestion**: Bot suggests doctors based on symptoms.
4. **Doctor Selection**: User selects a doctor.
5. **Appointment Details**: User provides details like name, email, mobile number, date, and time.
6. **Confirmation**: Bot confirms the appointment and sends a confirmation email to the user.

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

5. **Confirmation**:
   ```
   Bot: Appointment booked successfully! Confirmation email sent.
   ```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
