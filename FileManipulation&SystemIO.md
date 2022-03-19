# File Manipulation & System.IO
## File and Stream I/O
File and stream I/O (input/output) refers to the transfer of data either to or from a storage medium.
File: is an ordered and named collection of bytes that has persistent storage.
When you work with files, you work with directory paths, disk storage, and file and directory names.

### Files and directories
Here are some commonly used file and directory classes:

1. ``File``: provides static methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

2. ``FileInfo``: provides instance methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

3. ``Directory``: provides static methods for creating and moving directories and subdirectories.

4. ``DirectoryInfo``: provides instance methods for creating and moving directories and subdirectories.

5. ``Path``: provides methods and properties for processing directory strings in a cross-platform manner.

### Streams
The abstract base class Stream supports reading and writing. All classes that represent streams inherit from the Stream class.
Streams involve three fundamental operations:

1. Reading: transferring data from a stream into a data structure, such as an array of bytes.

2. Writing: transferring data to a stream from a data source.

3. Seeking: querying and modifying the current position within a stream.

### Compression
Compression refers to the process of reducing the size of a file for storage. Decompression is the process of extracting the contents of a compressed file so they are in a usable format. The ``System.IO.Compression`` namespace contains types for compressing and decompressing files and streams.

### Isolated storage
Isolated storage is a data storage mechanism that provides isolation and safety by defining standardized ways of associating code with saved data.

The following classes are frequently used when implementing isolated storage:

- ``IsolatedStorage``: provides the base class for isolated storage implementations.

- ``IsolatedStorageFile``: provides an isolated storage area that contains files and directories.

- ``IsolatedStorageFileStream``: exposes a file within isolated storage.

### I/O and security
When you use the classes in the ``System.IO`` namespace, you must follow operating system security requirements such as access control lists (ACLs) to control access to files and directories. This requirement is in addition to any FileIOPermission requirements. You can manage ACLs programmatically.[File and Stream I/O](https://docs.microsoft.com/en-us/dotnet/standard/io/)

## Write text to a file
The following classes and methods are typically used to write text to a file:

``StreamWriter`` contains methods to write to a file.
``File`` provides static methods to write text to a file.
``Path`` is for strings that have file or directory path information.

## Read and write to a newly created data file
The ``System.IO.BinaryWriter`` and ``System.IO.BinaryReader`` classes are used for writing and reading data other than character strings. 