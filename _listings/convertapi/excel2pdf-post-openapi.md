---
swagger: "2.0"
x-collection-name: ConvertAPI
x-complete: 0
info:
  title: Convert API Excel to PDF
  description: The API for converting Excel documents to PDF files and Images. These
    file formats csv, xls, xlsb, xlsx, xlt, xltx can be converted to pdf, pdfa, png,
    jpg, tif.
  version: v1
host: do.convertapi.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Email2Image:
    post:
      summary: Email to Image
      description: The API for converting E-Mail files to PDF files and Images. These
        file formats eml, mbx, msg, oft can be converted to png, jpg, tif.
      operationId: email2image
      x-api-path-slug: email2image-post
      parameters:
      - in: query
        name: ApiKey
        description: API Key should be passed if you purchased membership with credits
      - in: query
        name: File
        description: 'Supported source file formats: eml, mbx, msg, oft'
      - in: query
        name: ImageResolutionH
        description: Image horizontal resolution (DPI)
      - in: query
        name: ImageResolutionV
        description: Image vertical resolution (DPI)
      - in: query
        name: JpgQuality
        description: Jpg image quality
      - in: query
        name: OutputFormat
        description: Supported output file formats png, jpg, tif
      - in: query
        name: StoreFile
        description: Store file on server and return url to file instead of file stream
          response
      - in: query
        name: Timeout
        description: Conversion timeout in seconds
      responses:
        200:
          description: OK
      tags:
      - Email
      - Image
  /Email2Pdf:
    post:
      summary: Email to PDF
      description: The API for converting E-Mail files to PDF files and Images. These
        file formats eml, mbx, msg, oft can be converted to pdf, pdfa, png, jpg, tif.
      operationId: email2pdf
      x-api-path-slug: email2pdf-post
      parameters:
      - in: query
        name: ApiKey
        description: API Key should be passed if you purchased membership with credits
      - in: query
        name: DocumentAuthor
        description: Set the author of the generated Pdf file
      - in: query
        name: DocumentKeywords
        description: Set the keywords of the generated Pdf file
      - in: query
        name: DocumentSubject
        description: Set the subject of the generated Pdf file
      - in: query
        name: DocumentTitle
        description: Set the title of the generated Pdf file
      - in: query
        name: File
        description: 'Supported source file formats: eml, mbx, msg, oft'
      - in: query
        name: OutputFormat
        description: Supported output file formats pdf, pdfa, png, jpg, tif
      - in: query
        name: StoreFile
        description: Store file on server and return url to file instead of file stream
          response
      - in: query
        name: Timeout
        description: Conversion timeout in seconds
      responses:
        200:
          description: OK
      tags:
      - Email
      - PDF
  /Excel2Image:
    post:
      summary: Excel to Image
      description: The API for converting Excel documents to PDF files and Images.
        These file formats csv, xls, xlsb, xlsx, xlt, xltx can be converted to png,
        jpg, tif.
      operationId: excel2image
      x-api-path-slug: excel2image-post
      parameters:
      - in: query
        name: AlternativeParser
        description: If some objects are missing in converted Pdf files from original
          source files this option can be enabled to improve conversion
      - in: query
        name: ApiKey
        description: API Key should be passed if you purchased membership with credits
      - in: query
        name: File
        description: 'Supported source file formats: csv, xls, xlsb, xlsx, xlt, xltx'
      - in: query
        name: ImageResolutionH
        description: Image horizontal resolution (DPI)
      - in: query
        name: ImageResolutionV
        description: Image vertical resolution (DPI)
      - in: query
        name: JpgQuality
        description: Jpg image quality
      - in: query
        name: OutputFormat
        description: Supported output file formats png, jpg, tif
      - in: query
        name: StoreFile
        description: Store file on server and return url to file instead of file stream
          response
      - in: query
        name: Timeout
        description: Conversion timeout in seconds
      - in: query
        name: WorksheetActive
        description: Set to convert active worksheet
      - in: query
        name: WorksheetIndex
        description: Set worksheet index(number) to convert
      - in: query
        name: WorksheetName
        description: Set worksheet name to convert
      responses:
        200:
          description: OK
      tags:
      - Excel
      - Image
  /Excel2Pdf:
    post:
      summary: Excel to PDF
      description: The API for converting Excel documents to PDF files and Images.
        These file formats csv, xls, xlsb, xlsx, xlt, xltx can be converted to pdf,
        pdfa, png, jpg, tif.
      operationId: excel2pdf
      x-api-path-slug: excel2pdf-post
      parameters:
      - in: query
        name: AlternativeParser
        description: If some objects are missing in converted Pdf files from original
          source files this option can be enabled to improve conversion
      - in: query
        name: ApiKey
        description: API Key should be passed if you purchased membership with credits
      - in: query
        name: DocumentAuthor
        description: Set the author of the generated Pdf file
      - in: query
        name: DocumentKeywords
        description: Set the keywords of the generated Pdf file
      - in: query
        name: DocumentSubject
        description: Set the subject of the generated Pdf file
      - in: query
        name: DocumentTitle
        description: Set the title of the generated Pdf file
      - in: query
        name: File
        description: 'Supported source file formats: csv, xls, xlsb, xlsx, xlt, xltx'
      - in: query
        name: OutputFormat
        description: Supported output file formats pdf, pdfa, png, jpg, tif
      - in: query
        name: StoreFile
        description: Store file on server and return url to file instead of file stream
          response
      - in: query
        name: Timeout
        description: Conversion timeout in seconds
      - in: query
        name: WorksheetActive
        description: Set to convert active worksheet
      - in: query
        name: WorksheetIndex
        description: Set worksheet index(number) to convert
      - in: query
        name: WorksheetName
        description: Set worksheet name to convert
      responses:
        200:
          description: OK
      tags:
      - Excel
      - PDF
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---