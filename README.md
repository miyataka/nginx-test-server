# nginx-test-server

`nginx-test-server` is a test server built using Nginx that returns HTTP status codes specified via query parameters. It is useful for API testing and verifying behavior based on different status codes.

## Features

- Specify any HTTP status code using the `status` query parameter.
- Lightweight and easy to set up.
- A simple HTTP response simulator for testing and debugging.

## Requirements
- docker


## How to run
```bash
docker build . -q | xargs -I {} docker run  -p 8080:80 {}

# or you can pull the image from docker hub
docker pull miyataka/nginx-test-server:latest
```


## Usage

### Basic Usage

`nginx-test-server` changes the response status code based on the request's query parameter.

- Specify the response code using the `status` query parameter.
- Example: To return a status code of 204

    ```bash
    curl -v http://localhost:8080/?status=204
    ```

### Supported Status Codes

You can specify any HTTP status code (e.g., 200, 301, 404, 500). However, some status codes may be restricted by Nginx's configuration.

## Customizing Configuration

- You can customize the corresponding status codes and response contents in the configuration file.
- For detailed configuration options, please refer to the official Nginx documentation.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Feel free to submit issues for bug reports or feature requests, or create a pull request on the GitHub repository.
