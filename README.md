## Laravel JWT Authentication Example

This is a simple Laravel project demonstrating how to implement JWT (JSON Web Token) based authentication in a Laravel application. JWT is a popular method for securely transmitting information between parties as a JSON object. It is commonly used for implementing stateless authentication in web APIs.

### Features

- User registration and login with JWT token generation.
- JWT token refresh to extend the user's session.
- Endpoint to get user information using the JWT token.

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Akhand2021/Laravel-Jwt.git
   ```

2. Navigate to the project folder:

   ```bash
   cd Laravel-Jwt
   ```

3. Install the dependencies:

   ```bash
   composer install
   ```

4. Configure your `.env` file with the necessary database and JWT settings. You can copy the `.env.example` file:

   ```bash
   cp .env.example .env
   ```

   Then, edit `.env` with your database credentials and JWT secret.

5. Generate the application key:

   ```bash
   php artisan key:generate
   ```

6. Run the database migrations and seed the database:

   ```bash
   php artisan migrate --seed
   ```

7. Start the development server:

   ```bash
   php artisan serve
   ```

### API Endpoints

- **POST** `/api/register`: User registration. Provide `name`, `email`, and `password` as JSON data.

- **POST** `/api/login`: User login. Provide `email` and `password` as JSON data. This will return a JWT token for authentication.

- **POST** `/api/logout`: User logout. Requires a valid JWT token in the `Authorization` header.

- **POST** `/api/refresh`: Refresh JWT token. Requires a valid JWT token in the `Authorization` header. This will return a new JWT token with an extended expiration time.

- **GET** `/api/me`: Get authenticated user's information. Requires a valid JWT token in the `Authorization` header.

### Usage

1. Register a new user using the `/api/register` endpoint.

2. Login with the registered user using the `/api/login` endpoint. Copy the JWT token from the response.

3. Use the JWT token to access protected endpoints like `/api/me`, `/api/logout`, or `/api/refresh` by passing the token in the `Authorization` header as `Bearer <YOUR_JWT_TOKEN>`.

4. Refresh the JWT token using the `/api/refresh` endpoint to extend the user's session.

### Dependencies

- [Laravel](https://laravel.com/): A popular PHP web application framework.
- [Tymon JWT Auth](https://github.com/tymondesigns/jwt-auth): A package to provide JWT authentication for Laravel.

### License

This project is open-source and available under the [MIT License](LICENSE).

Feel free to explore, learn, and use this example as a starting point for your Laravel JWT authentication implementation. If you have any suggestions or improvements, please feel free to contribute or open an issue. Happy coding!

![Screenshot 2023-08-01 034411](https://github.com/Akhand2021/Laravel-Jwt/assets/104663417/168de75c-b280-4359-9fa3-b7f5403b97c7)
![Screenshot 2023-08-01 034448](https://github.com/Akhand2021/Laravel-Jwt/assets/104663417/bb158522-b3b4-4513-b1e8-aac63fee1df7)
![Screenshot 2023-08-01 034552](https://github.com/Akhand2021/Laravel-Jwt/assets/104663417/ecda4dcf-6c27-4f02-bd17-e94a9a025958)
![Screenshot 2023-08-01 035118](https://github.com/Akhand2021/Laravel-Jwt/assets/104663417/f1fb8539-207e-4b21-93da-cd07077b2ab8)
