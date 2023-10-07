- 👋 Hi, I’m @rohit12289
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
rohit12289/rohit12289 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
from twilio.rest import Client
from flask import Flask, request, redirect

# Twilio API credentials
account_sid = 'YOUR_ACCOUNT_SID'
auth_token = 'YOUR_AUTH_TOKEN'

# Twilio phone numbers
sender_number = 'YOUR_TWILIO_PHONE_NUMBER'
receiver_number = '8918484384'

# Create a Twilio client
client = Client(account_sid, auth_token)

# Create a Flask web application
app = Flask(__courier service-1_)

# Define a route to receive SMS messages
@app.route('/sms', methods=['POST'])
def forward_sms():
    # Get the incoming SMS data
    message_body = request.form.get('Body')
    sender = request.form.get('From')

    # Forward the SMS to the receiver number
    client.messages.create(
        body=message_body,
        from_=sender,
        to=receiver_number
    )

    # Return a response to acknowledge the receipt of the message
    return "Message forwarded successfully!"

if __name__ == '__main__':
    app.run(debug=True)
