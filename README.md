# Feira do Rolo API

Welcome to the Feira do Rolo API, a platform where residents can list items they're selling, and potential buyers can view these available items. This README will guide you through setting up, running, and testing the application locally.

## Prerequisites

Before you begin, ensure you have the following prerequisites installed:

- **Rust**: This application is built using the Rust programming language. Make sure you have Rust installed. You can download it (https://www.rust-lang.org/).

- **Docker Compose**: To run the PostgreSQL database for this application, Docker Compose is required. Install Docker Compose by following the instructions (https://docs.docker.com/compose/install/).

## Setup

1. Clone this repository to your local machine:

    git clone https://github.com/yourusername/rusty_feira.git

    Change into the project directory:

    cd rusty-feira

2. Start the PostgreSQL database using Docker Compose:

    docker compose up

This will create a PostgreSQL container and set up the necessary database for the application.

3. Install application dependencies:

    cargo build

## Running the Application

Now that you've set up the environment, you can run the rusty_feira.

4. Open a terminal window and navigate to the project directory

5. Run the application using the following command:

    cargo run

6. The API will start and be accessible at http://localhost:3000.

## Testing

You can test the API by using curl to make POST requests to add items for sale. Here's an example curl command:

curl -X POST http://localhost:3000/adicionar-item -H "Content-Type: application/json" -d '{
  "name": "Relógio Vintage",
  "description": "Um relógio antigo de madeira em perfeito estado de funcionamento.",
  "price": 50.0,
  "merchant_name": "João Silva"
}'

Feel free to create more items or interact with the API as needed for testing.

## Checking stocked items

After adding more items for sale to meet the required testing criteria, you can check the stored items by accessing the respective endpoint using the following command:

    curl http://localhost:3000/itens-a-venda

## Contributing

To contribute to this project, follow these steps:

    Fork this repository.

    Create a branch: git checkout -b feature/your-feature-name.

    Commit your changes: git commit -m 'Add some feature'.

    Push to the original branch: git push origin feature/your-feature-name.

    Create a pull request.