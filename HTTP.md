# HTTP Notes

* Accept (Request Header)
  - https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept
  - The Accept request HTTP header advertises which content types, expressed as MIME types, the client is able to understand. Using content negotiation, the server then selects one of the proposals, uses it and informs the client of its choice with the Content-Type response header. Browsers set adequate values for this header depending on the context where the request is done: when fetching a CSS stylesheet a different value is set for the request than when fetching an image, video or a script.
  - Syntax 
      - ``` 
        Accept: <MIME_type>/<MIME_subtype>
        Accept: <MIME_type>/*
        Accept: */*

        // Multiple types, weighted with the quality value syntax:
        Accept: text/html, application/xhtml+xml, application/xml;q=0.9, image/webp, */*;q=0.8
  - Examples
      - ``` 
        Accept: text/html

        Accept: image/*

        // General default
        Accept: */*

        // Default for navigation requests
        Accept: text/html, application/xhtml+xml, application/xml;q=0.9, */*;q=0.8
  
* ETag (Response Header)
  - https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/ETag
  - The ETag HTTP response header is an identifier for a specific version of a resource. It lets caches be more efficient and save bandwidth, as a web server does not need to resend a full response if the content has not changed. Additionally, etags help prevent simultaneous updates of a resource from overwriting each other ("mid-air collisions").
  - If the resource at a given URL changes, a new Etag value must be generated. A comparison of them can determine whether two representations of a resource are the same. Etags are therefore similar to fingerprints, and might also be used for tracking purposes by some servers. They might also be set to persist indefinitely by a tracking server.
  - Syntax 
      - ``` 
        ETag: W/"<etag_value>"
        ETag: "<etag_value>"
  - Examples
      - ``` 
        ETag: "33a64df551425fcc55e4d42a148795d9f25f89d4"
        ETag: W/"0815"
  - Mid-air collisions
      - To prevent POST Update if Document updated during Edit

* If-Match (Request Header)
  - https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/If-Match
  - The If-Match HTTP request header makes the request conditional. For GET and HEAD methods, the server will send back the requested resource only if it matches one of the listed ETags. For PUT and other non-safe methods, it will only upload the resource in this case.
  - The comparison with the stored ETag uses the strong comparison algorithm, meaning two files are considered identical byte to byte only. If a listed ETag has the W/ prefix indicating a weak entity tag, it will never match under this comparison algorithm.
  - Two common cases 
      - For GET and HEAD methods, used in combination with a Range header, it can guarantee that the new ranges requested comes from the same resource than the previous one. If it doesn't match, then a 416 (Range Not Satisfiable) response is returned.
      - For other methods, and in particular for PUT, If-Match can be used to prevent the lost update problem. It can check if the modification of a resource that the user wants to upload will not override another change that has been done since the original resource was fetched. If the request cannot be fulfilled, the 412 (Precondition Failed) response is returned.
  - Syntax 
      - ``` 
        If-Match: <etag_value>
        If-Match: <etag_value>, <etag_value>, …
  - Examples
      - ``` 
        If-Match: "bfc13a64729c4290ef5b2c2730249c88ca92d82d"

        If-Match: "67ab43", "54ed21", "7892dd"

        If-Match: *
