## Flask Application Design for a Payments Platform on Solana Blockchain

### HTML Files

- **index.html (Homepage):** This is the main page of the application, where users are welcomed and given options to interact with the platform. It should include:
  - Navigation bar with links to other pages
  - Brief description of the platform
  - Buttons for initiating payments, checking transaction history, and managing wallet settings.

- **payment-form.html (Payment Form):** This page contains the form for initiating payments. It should include:
  - Fields for recipient address, amount, and optional message
  - Button to submit payment information

- **transaction-history.html (Transaction History):** This page allows users to view a list of completed payments. It should include:
  - Table displaying transaction details (hash, recipient address, amount, date)
  - Option to filter transactions based on date or status

- **wallet-settings.html (Wallet Settings):** This page provides options to manage the user's Solana wallet. It should include:
  - Display of current wallet balance
  - Option to add/remove public keys
  - Option to adjust transaction fees

### Routes

- **/@home:** Renders the index.html page (homepage).

- **/@pay:** Renders the payment-form.html page (payment form).

- **/@transactions:** Renders the transaction-history.html page (transaction history).

- **/@wallet:** Renders the wallet-settings.html page (wallet settings).

- **/@submit-payment:** Handles the submission of payment information from the payment form. It should:
  - Initiate the payment transaction on the Solana blockchain
  - Store the transaction details in the database
  - Redirect the user to the payment status page.

- **/@get-transactions:** Retrieves the list of completed payments from the database and returns it as JSON data. This route is used by the transaction history page to display the transactions.

- **/@update-wallet:** Updates the user's Solana wallet settings. It should handle adding/removing public keys and adjusting transaction fees.