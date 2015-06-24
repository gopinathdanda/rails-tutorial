# Rails tutorial

## Request/Response Cycle

<img src='http://s3.amazonaws.com/codecademy-content/projects/3/request-response-cycle-dynamic.svg'>
<i>www.codecademy.com</i>

1. USER sends request to BROWSER.

2. BROWSER forwards to RAILS ROUTER.

3. RAILS ROUTER processes the request and forwards it to the CONTROLLER.

4. CONTROLLER requests data from MODEL.

5. MODEL requests the data from the DATABASE and sends back to the CONTROLLER.

6. CONTROLLER sends the data to the VIEW.

7. VIEW renders the requested HTML page and sends back to the CONTROLLER.

8. CONTROLLER compiles all the data and send back to the BROWSER.
