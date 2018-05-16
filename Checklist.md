* Verify format database:
     - csv (file format)
     - utf-8 (character code)
     - clean commentaries done on records (5 column)
* Verify 4th column (URL column)
* Create checksum of database file
* Verify checksum of database file
* Generate a keyword for _every_ file sent. A kind of tracking method of files (for internal use).



* _VERIFY THIS!_   (this data comes from: http://malete.org/Doc/IIF)
> In Database-Export, set the subfield separator to \031 and output line length to 0. 
> If the fields do not contain valid MARC data, use a reformatting FST like
> 001 0 MFN
> 044 0 |00^a|,v44
> 024 0 |00^a|,v24
> 026 0 |00|,v26
> 070 0 (|00^a|,v70/)
> Make sure, that
> the first output field is tag 1 containing some unique id
> every field (other than tagged 00*) starts with two indicator characters (really should be blank, but that would be stripped during export)
> the indicators are followed by a delimiter and subfield identifier
