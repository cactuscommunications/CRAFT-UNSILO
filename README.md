# CRAFT-UNSILO
Repository for holding modified CRAFT files

# conllu-files
This folder contains all the 67 documents on the conllu format.

- First commit to master in this repository contain the adapted versions that Manuel have created of the version 3.1.3 of craft
- The branch rs/paragraph-modifications contains files of which some have been edited with respect to missing paragraph annotations
- The file "conllu-paragraph-errors.txt" lists all errors that haven't been corrected in the CoNLL-U files

# Types of offset errors in CRAFT CoNNL-U
The CoNLLU format represents the original source text sentence by sentence. A special paragraph annotation is used to represent whenever a sentence is preceeded by a pargraph.
If you reconstruct the source text using only information from the CoNNL-U format you will not get an exact representation du to a variety of factors:

- Not all pargraphs are annotated
- Some paragraph annotations doesn't exist in the source document
- A paragraph i presupposed to consist of two line feeds, sometimes a paragraph in the source document is more than two line feeds
- Having more than a single space is not represented
- Spaces directly at the beginning of a paragraph before the first word is not represented
- A single CoNLL-U sentence might represent multiple source text sentence divided by unannotated paragraphs 

# CAS-XMI
We need to convert the CoNNL-U files to our own CAS XMI format. Also we would like to merge the CoNLL-U files with knowtator files that contain ontology information.
All this requires offsets to align with the original source text. Instead of manually correcting all the offset errors our CoNLL-U to CAS XMI converter will correct the offset errors 
while converting.