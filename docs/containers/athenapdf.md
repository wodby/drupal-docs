# AthenaPDF

AthenaPDF is an HTML to PDF converter and drop-in replacement for wkhtmltopdf

Usage example (for local environment, port `8080`):

```bash
$ curl http://athenapdf:8080/convert\?auth\=wodby-athenapdf\&url\=http://google.com/ |> out.pdf
```

Usage example (via Wodby, port `80`):

```bash
$ curl http://athenapdf/convert\?auth\=wodby-athenapdf\&url\=http://google.com/ |> out.pdf
```