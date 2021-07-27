# winston-visualize

## Installation

```bash
    npm i winston-visualize
    ## or
    yarn add  winston-visualize
```

## Example 

```javascript

    //create index.js and set the following code 
    // install express and winston

    const app = require('express')();
    const winston = require('winston');

    const logger = new (winston.Logger)({
        transports: [
            new (winston.transports.File)({
                filename: 'winston.log'
            })
        ]
    });

    require('winston-visualize')(app, logger);

    app.listen(3000, function () {
        logger.log('info', 'Hello distributed log files!');
    });
```

After this run :

```bash
 node index.js
```
visit: [http://localhost:3000/logs](http://localhost:3000/logs)

![image]("./view-logs.png")