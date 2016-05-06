
## Example

### dbf2json
    dbf2json = require("dbf2json")
    dbfReader = dbf2json.dbfReader
    
    fileName = './dbfout/people.dbf';
    dbfReader = new dbfReader(fileName, "GBK");

    dbfReader.on('head', function(head) {
    return console.log(head);
    });
    dbfReader.on('record', function(record) {
    return console.log(record);
    });
    dbfReader.on('end', function() {
    return console.log('finish');
    });

    dbfReader.parse();