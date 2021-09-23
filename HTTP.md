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

