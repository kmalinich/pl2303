# pl2303

Prolific PL2303 user-space USB to serial adapter driver for Node.js

## API

    const pl2303 = require('pl2303');

    const opts = {
        baudRate : 115200
    };
    
    let serial = new pl2303(opts);

    serial.on('data', data => console.log(data));
    serial.on('ready', () => serial.send(new Buffer('Hello!')));
