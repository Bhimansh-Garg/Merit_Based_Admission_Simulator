# Merit_Based_Admission_Simulator

# (Python + Twilio OTP)

This is a Python-based simulation of a simplified college admission system that allocates seats to students based on their rank and preferences. The system includes OTP-based verification using the Twilio SMS API, and stores results in a structured output file.

This project was created as a beginner-level exercise to understand how merit-based allocation works and how to integrate APIs like Twilio into Python applications.

---

## Overview

The system works as follows:

1. **Student Registration**
   - Each student provides their name, roll number, rank, phone number, and their preferred seat choices (up to 4 options).

2. **Seat Allocation**
   - Based on the student's rank and availability of seats, the system assigns the highest available seat from their preference list.
   - A total of 8 seats are available across 4 college-branch combinations.

3. **Report Card Access with OTP**
   - Students can retrieve their allocation result by entering their rank.
   - An OTP is sent to their registered phone number using Twilio's SMS API.
   - If the OTP is correctly entered, the student can view their allocation details.

4. **Output**
   - All student data, including allocation results, is saved to a text file named `students_placement.txt`.

---

## College and Branch Codes

Students can choose their preferences using the following codes:

| Code | Campus  | Branch |
|------|---------|--------|
| 1    | Pilani  | CSE    |
| 2    | Goa     | CSE    |
| 3    | Pilani  | ECE    |
| 4    | Goa     | ECE    |

---

## Technologies Used

- Python 3 for core logic and user interaction
- Twilio SMS API for OTP sending
- File handling in Python for data storage and reporting
- Random module for OTP generation

---

## File Structure

.
├── choice_order_and_seat_allocation.py   # Main application logic
├── Twilio_OTP_send.py                    # Twilio OTP integration script
├── students_placement.txt                # Output file containing allocation results
├── README.md                             # Project documentation

---

## How to Run the Project

1. Install dependencies:
   ```
   pip install twilio python-dotenv
   ```

2. Create a `.env` file in the root of the project with the following contents:

   ```
   TWILIO_ACCOUNT_SID=your_twilio_account_sid
   TWILIO_AUTH_TOKEN=your_twilio_auth_token
   TWILIO_PHONE_NUMBER=your_twilio_phone_number
   ```

3. Make sure your `.env` file is not committed to GitHub (add it to `.gitignore`).

4. Run the main script:
   ```
   python choice_order_and_seat_allocation.py
   ```

5. Follow on-screen prompts to register students and view report cards.

---

## Notes

- In this public version, all sensitive information such as phone numbers and API credentials have been replaced with placeholders (`xxxxxxxxxxxx`) for safety.
- OTP functionality requires a valid Twilio account and verified phone numbers.

---

## Future Improvements

This project can be expanded further by:

- Replacing text file storage with a relational database (e.g., SQLite or MySQL)
- Creating a web interface using Flask or Django
- Adding user authentication and admin dashboard
- Generating downloadable PDF report cards
- Adding email-based notifications in addition to SMS

---

## Author

**Bhimansh**  
Computer Science Undergraduate, 3rd Year  
Exploring backend systems, API integration, and software fundamentals

---

## License

This project is intended for learning and demonstration purposes only. You are free to use or extend it for your own academic or personal projects.
