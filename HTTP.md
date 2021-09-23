# HTTP Notes

* Accept (Request Header) 
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
