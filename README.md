# Auto-Makefile
Script to generate automaticly a makefile with a configuration file

usage : automakefile <<configuration file>>

The configuration file can contain the following (potentially unordered) lines:
 • source_filename;dependence1 dependence2. . .
 (specify the full names of the files, from the header subfolder below)
 • PROJECT_DIR;name_of_the_project_root_folder
 • SOURCES_DIR;subfolder_containing_the_source_files
 • HEADERS_DIR;subfolder_containing_the_header_files
 • LIBS_DIR;subfolder_containing_librairies
 • EXEC;executable_name
 • CC;compilator_binary
 • CFLAGS;compilation_flag1 compilation_flag1. . .
 • LDFLAGS;linking_flag1 linking_flag2. . .
 • BCK_DIR;name_of_the_backup_folder
 • ZIP;compression_binary
 • ZIPFLAGS;compression_options
 • UNZIP;decompression_binary
 • UNZIPFLAGS;decompression_options

The following rules have been added to the generated Makefile:
 archive : backup the source files in a compressed format, in the project folder
 revert : recreate the project from last backup
 delete : delete last backup
