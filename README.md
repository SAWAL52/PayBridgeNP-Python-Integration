# PayBridgeNP Python Integration

A simple Python implementation demonstrating how to integrate **PayBridgeNP** into a Python application and create hosted payment checkout sessions.

PayBridgeNP provides a unified payment gateway for accepting payments through eSewa, Khalti, and Fonepay.

## Features

- PayBridgeNP Python SDK integration
- Secure API key management using environment variables
- Hosted checkout session creation
- NPR currency support
- Success and cancellation return URLs
- Basic exception handling

## Tech Stack

- Python
- PayBridgeNP Python SDK
- python-dotenv

## Project Structure

```text
PayBridgeNP-Python-Integration/
│
├── main.py
├── requirements.txt
├── .env.example
├── .gitignore
├── LICENSE
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/SAWAL52/PayBridgeNP-Python-Integration.git
```

```bash
cd PayBridgeNP-Python-Integration
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**macOS / Linux**

```bash
source venv/bin/activate
```

**Windows**

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root and add your PayBridgeNP API key.

```env
PAYBRIDGENP_API_KEY=sk_test_your_api_key
```

You can obtain your API key from the PayBridgeNP dashboard.

### 5. Run the application

```bash
python main.py
```

## Payment Configuration

The integration uses a PayBridgeNP API key to authenticate requests and create checkout sessions.

The checkout amount is specified in paisa.

For example:

- NPR 100 = 10,000 paisa
- NPR 500 = 50,000 paisa
- NPR 1,000 = 100,000 paisa

Use a test API key during development. Switch to a live API key only when you are ready to accept real payments.

## Security

- Never commit your `.env` file.
- Never expose your secret API key in public repositories.
- Use environment variables to manage sensitive credentials.
- Use HTTPS for production return URLs.

## Resources

- [PayBridgeNP Website](https://paybridgenp.com/)
- [PayBridgeNP Python SDK](https://pypi.org/project/paybridge-np/)
- [PayBridgeNP GitHub](https://github.com/paybridgenp)

## License

This project is licensed under the MIT License.