jQuery JSON-RPC Plugin
======================

A JSON-RPC 2.0 implementation for jQuery.

JSON-RPC is a stateless, light-weight remote procedure call (RPC) protocol.

Usage
-----

    $.jsonrpc([opt_opts]);

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
