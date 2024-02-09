# Log Injection

Severity: Varies  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

Applications typically use log files to store a history of events or transactions for later review, statistics gathering, or debugging. Depending on the nature of the application, the task of reviewing log files may be performed manually on an as-needed basis or automated with a tool that automatically culls logs for important events or trending information.

Writing invalidated user input to log files can allow an attacker to forge log entries or inject malicious content into the logs. This is called log injection.

During the tests, it was discovered that some logs can be tampered with because log requests are implemented on the client side and can be manipulated by an attacker. Log integrity is affected.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to implement logging on the server side. Logging of actions should never be sent from the user's browser. They should be logged directly within the API executing the action.

The logs server should whitelist other servers that can send requests to it and deny access to everyone else.

## Reference

* OWASP, https://owasp.org/www-community/attacks/Log_Injection
* OWASP, https://cheatsheetseries.owasp.org/cheatsheets/Logging_Cheat_Sheet.html
