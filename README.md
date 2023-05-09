# my_directory_loader

This is a single-file GitHub repository that contains a modified version of LangChain's `DirectoryLoader` class. It allows you to load a directory of documents into a `DocumentIndex` object, with support for PDF files.

The main difference from LangChain's `DirectoryLoader` is that this version uses a separate loader class, `pdfloader_cls`, to handle PDF files. This is a workaround for a bug in Unstructured's PDF processing module.

To use this class, you need to import it from the file `my_directory_loader.py`. You can then create an instance of the class and call its `load` method with the path to the directory of documents. You can also pass an optional parameter, `pdfloader_cls`, to specify the loader class for PDF files. The default value is `PyPDFLoader`, which is a wrapper around PyPDF2.

For more details on the parameters and returned values of the `load` method, please refer to LangChain's documentation:

- Overview: https://python.langchain.com/en/latest/modules/indexes/document_loaders/examples/file_directory.html?highlight=Directory%20Loader
- Reference: https://python.langchain.com/en/latest/reference/modules/document_loaders.html?highlight=DirectoryLoader#langchain.document_loaders.DirectoryLoader
