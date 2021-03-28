## Domain Modeling
Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model. Here's some tips to follow when building your own domain models.

## API
API keys are a simple encrypted string that identifies an application without any principal
SuperAgent

SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs. It also works with Node.js!

### Test documentation
The following test documentation was generated with Mocha's "doc" reporter, and directly reflects the test suite. This provides an additional source of documentation.

Request basics A request can be initiated by invoking the appropriate method on the request object, then calling .then() (or .end() or await) to send the request. For example a simple GET request:

 request
   .get('/search')
   .then(res => {
      // res.body, res.headers, res.status
   })
   .catch(err => {
      // err.message, err.response
   });
JSON / Urlencoded
The property res.body is the parsed object, for example if a request responded with the JSON string '{"user":{"name":"tobi"}}', res.body.user.name would be "tobi". Likewise the x-www-form-urlencoded value of "user[name]=tobi" would yield the same result. Only one level of nesting is supported. If you need more complex data, send JSON instead.

### Response properties
- Response text : res.text
- Response body : res.body
- Response header fields : res.header
- Response Content-Type : res.type
- Response status : res.status

### Authentication
In both Node and browsers auth available via the .auth() method:

request
  .get('http://local')
  .auth('tobi', 'learnboost')
  .then(callback);
  