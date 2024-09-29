# llmflooder
Designed to benchmark HTTP requests to LLM providing detailed statistics on the request times and response sizes, offering insights into the performance of the API.

### Usage:

The default values for the host and port are `127.0.0.1` and `42069`, respectively.

You can specify the host and port as command-line arguments:

- `--host`: Specifies the host to send the requests to. Defaults to `127.0.0.1`.
- `--port`: Specifies the port of the API. Defaults to `42069`.

Example:

```bash
./llmflooder --host=192.168.1.100 --port=8080
```

### Statistics

At the end of the execution, the following statistics are displayed:

- **Total Requests:** The number of requests made across all workers.
- **Total Time:** The total time taken for all requests.
- **Average Time Per Request:** The average time for a single request.
- **Min Time:** The minimum time taken for any request.
- **Max Time:** The maximum time taken for any request.

## Example Output

```
Master process 12345 is running
All requests have been completed.

=== Request Statistics ===

Request 1:
  Worker ID: 54321
  Status Code: 200
  Response Size: 1050 bytes
  Request Duration: 15.40 ms
  Total Time: 18.50 ms

Request 2:
  Worker ID: 54321
  Status Code: 200
  Response Size: 1078 bytes
  Request Duration: 12.32 ms
  Total Time: 16.00 ms

...

=== Summary Statistics ===
  Total Requests: 100
  Total Time: 1050.00 ms
  Average Time Per Request: 10.50 ms
  Min Time: 8.00 ms
  Max Time: 15.00 ms
```

## Customization

You can modify the number of total requests and other constants within the script:

const TOTAL_REQUESTS = 100; // Total number of requests to be made

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
```
