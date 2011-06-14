jQuery JSON-RPC Plugin
======================

A JSON-RPC 2.0 implementation for jQuery.

Usage
-----

### Invocation

    $.jsonrpc([opt_opts]);

### Parameter detail

*   id:
    The request id.

*   url:
    A string containing the URL to which the request is sent.

*   method:
    A String containing the name of the method to be invoked.

*   params:
    An object to pass as arguments to the method.

*   success:
    A function to be called if the request succeeds.

*   fault:
    A function to be called if the request succeeds (but with error response).

*   error:
    A function to be called if the request fails..

Examples
--------

    // A RPC call with named parameters
    $.jsonrpc({
      url: "/rpc",
      method: "createUser",
      params: {
        name: "John Smith",
        userId: 1000
      },
      success: function (response) {
        // pass
      },
      fault: function (response, errordata) {
        // pass
      },
      error: function (request, status, error) {
        // pass
      }
    });

    // A Notification
    $.jsonrpc({
      url: "/rpc",
      method: "notify",
      params: {
        action: "logout",
        userId: 1000
      }
    });

    // A Notification using console to debug and with timeout set
    $.jsonrpc({
      url: "/rpc"
      method: "notify",
      params: {
        action: "logout",
        userId: 1000
      },
      timeout: 500
    });
