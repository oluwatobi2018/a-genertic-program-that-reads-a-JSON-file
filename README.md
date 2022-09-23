# a-genertic-program-that-reads-a-JSON-file
A genertic program that: reads a JSON file.
I wrote a genertic program that:
- Reads a JSON file similar to what's present in this location (./data/)
- Sniffs the schema of the JSON file 
- Dumps the output in (./schema/)

# Additional informations for test cases
- - Padding: All attributes in the JSON schema were padded with "tag" and "description" keys
- The schema output captures ONLY the attributes within the "message" key of the input JSON source data. All attributes withn the key "attributes" were excluded
- The JSON schema set all properties "required": false
- For data types of the JSON schema:
STRING: program identifies what is a string and map accordingly in JSON schema output
INTEGER: program identifies what is an integer and map accordingly in JSON schema output
ENUM: When the value in an array is a string, the program maps the data type as an ENUM 
ARRAY: When the value in an array is another JSON object, the program maps the data type as an ARRAY.
