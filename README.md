# Event Duration Logger and Error Tracking

This repository contains a JavaScript utility for logging event durations and tracking errors in a web application. It leverages the PerformanceObserver API to log the time taken by event handlers and sets up error tracking mechanisms for unhandled exceptions and promise rejections.

## Usage

1. Include the provided JavaScript code in your project.
2. Utilize the `logEventDuration` function in conjunction with the `PerformanceObserver` to log the duration of event handlers.
3. The code will automatically capture and record various types of errors that occur during the execution of your application.
4. The code also intercepts standard logging functions to capture log messages and store them for analysis.

## Features

- **Event Duration Logging**: The `logEventDuration` function logs the duration of event handlers. Use the `PerformanceObserver` to observe events of type "event" and enable the `buffered` option.

- **Error Tracking**: The code captures and records unhandled exceptions and promise rejections.
  - `window.onerror`: Captures unhandled exceptions and adds them to the error log along with a timestamp.
  - `window.onunhandledrejection`: Captures unhandled promise rejections and adds them to the error log along with a timestamp.

- **Custom Logging Storage**: The code maintains a `console.everything` array to store various captured events, including errors and log messages. Each entry includes event type, timestamp, and relevant data.

- **Intercepted Console Logging**: The code intercepts standard console logging functions (`log`, `error`, `warn`, `debug`) to capture their output and store log messages in the `console.everything` array.

## Getting Started

1. Clone this repository to your local machine or integrate the provided JavaScript code into your project.

2. Ensure the code is properly integrated into your project's codebase and that you understand the implications of modifying the behavior of standard console logging functions.

3. Utilize the provided functions and observers to capture event durations and track errors in your application.

## Note

This code is intended to provide insights into your application's behavior and errors for debugging purposes. Adapt and integrate the code into your project as needed.

## License

This project is licensed under the [MIT License](LICENSE).
