# Scam Message Investigator

## Project Description

Scam Message Investigator is an AI-powered application that analyzes suspicious SMS messages, emails, WhatsApp messages, and online notifications. It uses a locally running Gemma 3:1B language model through Ollama to identify potential scam indicators and provide safety recommendations.

The application examines message content, highlights suspicious phrases, identifies possible warning signs, and assigns a risk level to help users make informed decisions.

## Features

- **AI-Based Message Analysis:** Uses Gemma 3:1B to investigate suspicious messages.
- **Risk Level Detection:** Classifies messages into Low Concern, Medium Concern, or High Concern.
- **Message Classification:** Identifies the possible category of a suspicious message.
- **Warning Sign Identification:** Highlights suspicious phrases and explains why they may be risky.
- **Suspicious Link Detection:** Extracts URLs from messages and displays them separately for inspection.
- **Safety Recommendations:** Provides practical actions to help users avoid potential scams.
- **Investigation Limitations:** Explains what cannot be verified from message content alone.
- **Download Investigation Report:** Allows users to download reports in TXT and JSON formats.
- **Local AI Processing:** Uses Ollama to run the language model locally.

## Technologies Used

- Python
- Streamlit
- Ollama
- Gemma 3:1B
- Requests
- JSON
- Regular Expressions

## System Requirements

- Python 3.10 or later
- Ollama installed on the computer
- Gemma 3:1B model downloaded
- Internet connection for initial package and model downloads
- Sufficient available system memory to run the AI model

## Installation

### Step 1: Install Python Libraries

Open the terminal and execute:

```bash
pip install streamlit requests
```

### Step 2: Install Ollama

Download and install Ollama from:

https://ollama.com/

### Step 3: Download the Gemma Model

Open Command Prompt and execute:

```bash
ollama pull gemma3:1b
```

### Step 4: Check the Model

Run the following command:

```bash
ollama run gemma3:1b
```

If the model responds to your message, it is ready to use. Type `/bye` to exit.

## Running the Application

1. Open the project folder in Command Prompt.
2. Make sure Ollama is running.
3. Execute the following command:

```bash
streamlit run app.py
```
4. The application will open in your web browser.
5. Paste a suspicious message into the text area.
6. Click the **Investigate Message** button.
7. View the investigation report and download the results if required.

## How It Works

1. **User Input:** The user enters a suspicious SMS, email, WhatsApp message, or online notification.
2. **Link Detection:** The application extracts URLs from the submitted message using regular expressions.
3. **AI Processing:** The message is sent to the locally running Gemma 3:1B model through the Ollama API.
4. **Message Analysis:** The AI examines the message for suspicious language, urgency, requests for sensitive information, unusual payments, and other warning signs.
5. **Risk Assessment:** The application displays a risk level based on the AI-generated analysis.
6. **Investigation Report:** The application displays the message category, summary, warning signs, recommended actions, and investigation limitations.
7. **Report Download:** The user can download the investigation results in TXT or JSON format.

## Risk Classification

| Risk Level | Description |
|---|---|
| Low Concern | No clear suspicious indicators identified. |
| Medium Concern | Some unusual or potentially suspicious indicators found. |
| High Concern | Multiple serious scam indicators identified. |

## Sample Input

```text
URGENT! Your bank account will be blocked today
due to incomplete KYC verification.

Click https://sbi-update.example.com and enter
your account number, ATM PIN and OTP immediately
to avoid account suspension.
```

## Expected Output

- Risk Level: High Concern
- Message Type: Bank KYC Scam
- Summary: The message uses urgency and requests sensitive banking information through a suspicious link.
- Warning Signs: Account suspension threat, request for ATM PIN and OTP, suspicious URL.
- Recommended Actions: Do not click the link or share sensitive information. Contact the bank through its official website or customer service.

*The actual output may vary depending on the AI model's analysis.*

## Applications

- Identifying potentially fraudulent SMS messages.
- Examining suspicious emails and online notifications.
- Recognizing fake job offers and lottery messages.
- Detecting suspicious payment requests.
- Improving digital safety awareness.
- Helping users recognize common scam techniques.

## Advantages

- Simple and user-friendly interface.
- Local language model integration.
- Automated message analysis.
- Identifies potential warning signs.
- Provides practical safety recommendations.
- Supports downloadable investigation reports.

## Limitations

- AI-generated results may not always be accurate.
- A message alone cannot confirm whether a sender is genuine.
- Extracting a URL does not verify whether the website is malicious.
- The application does not independently verify sender identities or website ownership.
- Analysis depends on the availability of Ollama and sufficient system resources.

## Future Enhancements

- Support for multiple regional languages.
- Email and SMS analysis integration.
- Advanced URL reputation checking.
- Message history and investigation tracking.
- Additional AI models for improved analysis.
- PDF report generation.

## Conclusion

Scam Message Investigator provides an AI-based approach to identifying potential scam messages. By combining natural language processing, risk classification, suspicious link extraction, and safety recommendations, the application helps users understand possible digital threats and make safer online decisions.

