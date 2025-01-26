# Bus Ticket Booking Process Automation

## Overview

Bus Ticket Booking Automation is an RPA (Robotic Process Automation) project implemented using UiPath to streamline the process of booking bus tickets. The workflow automates tasks such as reading passenger details from an Excel sheet, filling out a Google Form, submitting it, and sending confirmation emails using an SMTP server. This solution enhances accuracy, reduces manual effort, and ensures timely communication.

---

## Implementation

### Workflow Steps

1. **Open UiPath Studio**:

   - Begin by creating a new process and naming it `Bus Ticket Booking Automation`.

2. **Sequence Activity**:

   - Add a Sequence activity labeled `Sequence - Automate Bus Ticket Booking`.
   - Annotation: "Automates the bus ticket booking process by reading passenger details, filling out a Google Form, and sending confirmation emails."

3. **Try-Catch Activity**:

   - Add a Try-Catch activity for robust error handling.

   **In the Try section:**

   - Use the `Read Range` activity to read passenger details from an Excel sheet.
     - Annotation: "This activity reads data like name, age, gender, source, destination, and email from the Excel sheet."
   - Use the `Open Browser` activity to navigate to the Google Form.
     - Annotation: "This activity opens the specified Google Form URL."
   - Configure `Type Into` activities to fill out the form fields.
     - Annotation: "Inputs passenger details into the Google Form fields."
   - Use a `Click` activity to submit the form and reload it for the next entry.
     - Annotation: "Clicks the 'Submit another response' button to reset the form."
   - Use the `SMTP Mail Message` activity to send confirmation emails.
     - Annotation: "Sends a confirmation email to each passenger."
   - Add a `Message Box` to display a success message:
     "All tickets have been successfully booked, and confirmation emails have been sent."

   **In the Catch section:**

   - Use the `Assign` activity to capture exception details.
   - Add a `Message Box` to display the error message.

---

## Modules and Their Roles

### Sequence: Automate Bus Ticket Booking

- Organizes activities for reading data, filling forms, and sending confirmation emails.

### Try-Catch: Error Handling

- Ensures smooth execution and detailed error reporting.

### Read Range: Extract Passenger Details

- Reads data such as name, age, gender, source, destination, and email from an Excel file.

### Type Into and Click: Form Automation

- Automates data entry into the Google Form and submits it.

### SMTP Mail Message: Send Confirmation Emails

- Sends personalized emails to passengers after successful form submission.

### Message Box: Completion Message

- Displays a success message upon workflow completion.

---

## Screenshots

1. **Excel Sheet**:
   - ![Homepage](screenshots/Excel.png)
2. **Google Form**:
   - Screenshot of the form being filled by the bot.
3. **Submit Another Response**:
   - Screenshot of the form resetting for the next entry.
4. **Email Confirmation**:
   - Screenshot of a confirmation email sent to a passenger.

---

## How to Run the Workflow

### Prerequisites:

- Install UiPath Studio.
- Ensure the Google Form URL is accessible.

### Steps to Execute:

1. Open the workflow in UiPath Studio.
2. Configure the Excel file path in the `Read Range` activity.
3. Set the Google Form URL in the `Open Browser` activity.
4. Configure the SMTP server settings for sending emails.
5. Run the workflow by clicking the `Run` button in UiPath Studio.
6. Upon completion, verify the confirmation emails and Google Form submissions.

---

## Results

- Automates the bus ticket booking process by reading data from an Excel sheet, filling out a Google Form, and sending confirmation emails.
- Handles multiple entries with high accuracy and minimal manual intervention.
- Improves operational efficiency and reduces time spent on repetitive tasks.

---

## Output

1. **Passenger Details Processed**:
   - All rows in the Excel sheet are processed.
2. **Google Form Submissions**:
   - Forms are submitted successfully for all passengers.
3. **Email Confirmations**:
   - Automated confirmation emails sent to all passengers.

---

## Future Enhancements

1. Add support for multiple Google Forms or booking platforms.
2. Include options for filtering based on travel preferences.
3. Enhance error logging with detailed reports.
4. Automate follow-up notifications for passengers.

---

## Project Associates

- Satyam Kumar Singh
- Sharath M S
- Shreeharsh Joshi
- Shreyas C

---

