# my_directory_loader

This is a single-file GitHub repository that contains a modified version of LangChain's `DirectoryLoader` class. It allows you to load a directory of documents into a `DocumentIndex` object, and work around an apparent bug in Unstructured's support for PDF files that causes kernel crashes in Jupyter and segmentation faults when executed in .py files.

The only difference from LangChain's `DirectoryLoader` is that this version offers a separate loader class, `pdfloader_cls`, which defaults to `PyPDFLoader` (a wrapper around PyPDF2). By default, all other file types go through `UnstructuredFileLoader`.

For more details on the parameters and returned values of `DirectoryLoader`, please refer to LangChain's documentation:

- Overview: https://python.langchain.com/en/latest/modules/indexes/document_loaders/examples/file_directory.html?highlight=Directory%20Loader
- Reference: https://python.langchain.com/en/latest/reference/modules/document_loaders.html?highlight=DirectoryLoader#langchain.document_loaders.DirectoryLoader
