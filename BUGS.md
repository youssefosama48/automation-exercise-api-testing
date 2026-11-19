\# API Bugs \& Observations



\## BUG-001: Incorrect HTTP Status Code Handling



\*\*Category:\*\* API Response / HTTP Status Code



\*\*Description:\*\*



API endpoints consistently return `200 OK` as the actual HTTP status code, regardless of the operation's result. The expected HTTP status code is instead provided as a property inside the response body.



\*\*Actual Result:\*\*

\- HTTP response status is always `200 OK`.

\- The response body contains a `responseCode` property representing the intended status code.



\*\*Expected Result:\*\*

\- The API should return the appropriate HTTP status code at the protocol level.

\- The response body should contain relevant response details without relying on a body property to replace the actual HTTP status.



\*\*Impact:\*\*

\- API clients cannot reliably depend on HTTP status codes to identify request outcomes.

\- Standard HTTP error handling and status-based monitoring may not work as expected.

\- Automated API tests must validate the response body property separately from the actual HTTP status.



\*\*Note:\*\* This appears to be a shared behavior across the API endpoints tested so far.

