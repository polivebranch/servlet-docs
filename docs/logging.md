# Logging best practice

To avoid potential stack trace exposure, avoid logging complete stack traces.

As an example
```
try {
        //something that may generate an exception
    } catch (Exception e) {
        // Log the error securely
        log("Error searching books by author: " + e.getMessage());
        // Provide a user-friendly error message
    }
```

Using `e.getMessage()` rather than `e` in the `log` statement ensures useful information is included in the log, but not the full stack trace.
