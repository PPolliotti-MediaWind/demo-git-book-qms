# Test code

```javascript
const SERVER_URL = "https://{your_server}:7443";
const API_KEY = "{YOUR_API_KEY}";

const io = require('socket.io-client');

const client = io.connect(SERVER_URL, {
    query: {
        apikey: API_KEY,
    }
});

client.on('test_deloitte', function (data) {
    console.log(data);
});

client.on('status', function (data) {
    // the 
    console.log('status:', data);
});

client.on('connect', function () {
    console.log('connected');
});

client.on("connect_error", function (error) {
    console.log('connect_error:', error.message);
});

client.on('disconnect', function (data) {
    console.log('disconnect:', data);
});

```
