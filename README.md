### Example ESign Iframe Flow

Files:
1. index.html = Form presented to customer
2. third-party/document.html = represents document held on Esign with signing capabilities.


##### Customer Flow
1. Customer opens web page with form that requires a document signed
2. Customer clicks to sign document
3. Iframe with document opens on screen
4. Customer signs document in Iframe
5. Parent window (the form) receives event with ID of the document created, closes Iframe and sets hidden 'document_id' field in form
6. Customer submits form to server
7. Server receives form data with id of document created
8. Server stores the id of the document against the customer record for later user
8. Server uses ESign api to retrieve signed document for storage

