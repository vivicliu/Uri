# Uri
Uri provides two sets of functionalities:
1) Parse a URI string and populate the basic structure of the URI including
   scheme, user/password, host, port, path, query parameters and fragment.

   The key method the class currently provides is parseUtf8UriStr which parses
   a UTF-8 encoded URI string.

2) Converting a constructed URI object into a string.  Query parameters are appended to the
   Uri string in an ascending order of parameter keys.

The parsing logic is based on the RFC3986 spec http://tools.ietf.org/html/rfc3986.

****************************
Unfinished functionality:
- Respecting the required components of a URI per specification of RFC3986, i.e., throw
  exceptions when parsing URI strings that miss at least a required component, or when generating
  the URI string from a URI object that miss at least a required component.

- Proper unescaping the %-encoded characters of the input URI string

- Proper escaping of reserved characters using %-encoding

- Handling the parsing and generation of URI strings in character sets other than UTF-8

- Generating string representation using the right character set.

- Performance of Uri.toString can be optimized by allocating a byte array and then perform array copy

****************************
To run UriTest:

./uri_test.sh
~                 
