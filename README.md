# Emailer

This is a simple emailing application that allows you to build a mailing list using the SendInBlue API. With this application, you can collect email addresses from users and store them in your SendInBlue account for future email marketing campaigns. It provides a basic web interface for users to enter their email addresses and a backend server that communicates with the SendInBlue API to handle the mailing list operations.

## Features

- Collect email addresses from users through a web interface.
- Store collected email addresses in your SendInBlue account.
- Handle duplicate email address entries and prevent storing duplicates.
- Provide feedback to users about the status of their email address submission.

## Prerequisites

To set up and run the Simple Emailing Application, you need to have the following:

- Node.js (v12 or above) and npm installed on your system.
- A SendInBlue account with API access. Obtain the API key from your SendInBlue account dashboard.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/EvelynOvi/Emailer.git
   cd Emailer
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

3. Set up the configuration:

   - Open the `.env` file and update the `SENDINBLUE_API_KEY` variable with your SendInBlue API key.

## Usage

1. Start the application:

   ```bash
   npm start
   ```

2. Open your web browser and navigate to `http://localhost:3000`.

3. Enter your email address in the provided field and click the "Subscribe" button.

4. You will receive feedback indicating the status of your email address submission.

## How it works

- When the user enters an email address and clicks the "Subscribe" button, the frontend sends a POST request to the backend server.
- The backend server receives the email address from the request payload and checks if it is a valid email format.
- If the email address is valid, the server communicates with the SendInBlue API using the provided API key to add the email address to the mailing list.
- The server handles any errors or duplicate email entries and sends an appropriate response back to the frontend.
- The frontend displays the feedback message received from the server to the user.

## Configuration

The application uses environment variables for configuration. The available configuration options are:

- `SENDINBLUE_API_KEY` - Your SendInBlue API key. Obtain it from your SendInBlue account dashboard.
- `PORT` - The port on which the server should listen (default: 3000).

## Contributing

Contributions are welcome! If you find any bugs or have suggestions for improvements, please create an issue or submit a pull request on the GitHub repository.

## License

This project is licensed under the [MIT License](LICENSE).

## Disclaimer

This application is for demonstration purposes only and may not be suitable for production environments. Use it at your own risk.