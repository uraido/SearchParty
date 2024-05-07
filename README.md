# SearchParty #

![SearchParty_en-us](https://github.com/0xSickb0y/SearchParty/assets/148525929/f2bdf931-cc06-4837-bbff-fe213aa3dcc6)

## Intro ##
 _SearchParty_ is a tool developed as part of the [FIAP](https://www.fiap.com.br) Challenge project for the 2023 mid-year Cyber-Defense classes.

Its primary purpose is to find personal and sensitive data within the file system.

## Description

The tool iterates over the provided input, categorizing files based on their MIME types. Each type is organized into a list for further processing.

Subsequently, an extraction method is initiated for each file type, with each method representing a member of a _Search Party_.

The extraction methods use regular expressions and keywords to examine the text extracted from the files, searching for matches with the supported data types.

During program execution, the data is mapped, and upon completion, the user receives a comprehensive mapping of its location, available in database format, text files, or standard output.

Additionally, the tool provides practical file management features, enabling users to copy, move, or delete files according to their analysis findings.

##  Supported File Extensions
- **.txt**: text/plain
- **.csv**: text/csv
- **.bmp**: image/bmp
- **.png**: image/png
- **.gif**: image/gif
- **.tiff**: image/tiff
- **.jpeg**: image/jpeg
- **.webp**: image/webp
- **.docx**: application/vnd.openxmlformats-officedocument.wordprocessingml.document
- **.xlsx**: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet
- **.pptx**: application/vnd.openxmlformats-officedocument.presentationml.presentation
- **.pdf**: application/pdf
- **.eml**: message/rfc822

## Supported Data Types
- **(cpf)** 546.435.321-01
- **(rg)** 54.643.532.10
- **(cnpj)** 54.643.532/0000-10
- **(email)** _example.user@domain.org_
- **(phone)** +55 (11) 95464-3521, (11) 95464-3521, 11 95464-3521
- **Ethnic groups**
- **Financial information**
- **Legal information**
- **Medical information**
- **Political preferences**
- **Vehicle documents**
- **Gender and sexual orientation**
- **Property information**
- **Religion and faith**
- **Travel history**

## Usage

Running the tool:

    python SearchParty.py [-h] [-F $file] [-D $directory] [--find  [...]] [--loot [$name]] [--database [$sql.db]] [--data-type $type] [--file-type $type] [--copy-files $dst]
                      [--move-files $dst] [--delete-files]

## Options
```
  -h, --help            show this help message and exit
  -F $file              scan file
  -D $directory         scan directory
  --find  [ ...]        search for specific values ('John Doe' '47.283.723-0')
  --loot [$name]        save results to a directory (default: $current/loot)
  --database [$sql.db]  save results to a database (default: $hostname.db)
  --data-type $type     data types separated by comma (cpf,rg)
  --file-type $type     file types separated by comma (pdf,docx)
  --copy-files $dst     copy files to another location
  --move-files $dst     move files to another location
  --delete-files        delete files from the file system
```
## Outro
_Project in Development..._