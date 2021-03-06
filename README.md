# Latte
Generate PDFs using LaTeX templates and JSON

## How to use
Latte starts an HTTP server and listens on port 27182 by default at the endpoint `/generate`.
Example POST request JSON body:
```
{
  "template": <BASE64 ENCODED .tex FILE>,
  "resources": {
    "image1.png": <BASE64 ENCODED RESOURCE FILE>
   },
   "details": {
    "CustomerName": "John Doe",
    "Phone": "555-555-5555"
   }
}
```
The template `.tex` file should be a template that follows [Go's templating syntax](https://golang.org/pkg/text/template/)

## Roadmap
- Registering templates and resources.
- Add support for AWS S3, PostrgeSQL, and possibly other forms of persistent storage.
- CLI tool.
- Add support for building PDFs from multiple LaTeX files.
- Whatever else comes up
