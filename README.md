# Express Rate Limit Project

This project implements rate limiting using the `express-rate-limit` middleware in a Node.js Express application.

## Getting Started

To get started with this project, follow these steps:

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/achrefjlidi/express-rate-limit/
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Run the application:

   ```bash
   node app.js
   ```

   The application will start running on port 5000 by default. You can change the port by setting the `PORT` environment variable.

## Usage

This project demonstrates how to implement rate limiting in an Express application using the `express-rate-limit` middleware. The middleware is applied globally to all routes, limiting the number of requests a client can make within a specified time window.

### `express-rate-limit` Middleware

The `express-rate-limit` middleware is used to limit repeated requests to public APIs and/or endpoints such as login, password reset, and others. It can be configured with various parameters to control the rate limiting behavior.

#### Parameters

- `windowMs` (default: 15 minutes): The time window in milliseconds for which to track requests.
- `max` (default: 100): The maximum number of requests allowed in the `windowMs` time window.
- `message`: The message to be sent when the request rate limit is exceeded.
- `statusCode` (default: 429 Too Many Requests): The HTTP status code to be sent when the request rate limit is exceeded.
- `headers`: Custom headers to be sent when the request rate limit is exceeded.

For more details and advanced configurations, refer to the [documentation of `express-rate-limit`](https://www.npmjs.com/package/express-rate-limit).

## Project Structure

- `middlewares/ratelimit.js`: Contains the rate limiting middleware.
- `app.js` (or `index.js`): Contains the main application logic.
- `package.json`: Contains project metadata and dependencies.

## API Routes

- `/api/blog`: A simple API route welcoming users to the Blog API Rate Limiter Project.
- `/api/blog/post`: A sample API route returning a blog post.

## Environment Variables

- `PORT`: Port on which the server will run. Defaults to 5000 if not specified.

## Contributing

Feel free to contribute to this project by opening issues or pull requests. Your feedback and contributions are highly appreciated.

## License

This project is licensed under the [MIT License](LICENSE).
