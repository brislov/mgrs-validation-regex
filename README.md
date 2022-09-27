# Validation regex for MGRS coordinates
## Zone
The grid designator zone locates a UTM zone given a column number and a row letter:
* column number 1-60 (a leading 0 is allowed for single digit numbers, e.g. 01)
* row letter A-Z (omitting I and O)
```
^(([0-5]?[0-9])|60)[ABCDEFGHJKLMNPQRSTUVWXYZ]$
```
## Square
Each zone is divided into squares that are 100 000 meters wide. The square is identified by a column letter and a row letter:
* column letter A-Z (omitting I and O)
* row letter A-V (omitting I and O)
```
^[abcdefghjklmnpqrstuvwxyzABCDEFGHJKLMNPQRSTUVWXYZ][abcdefghjklmnpqrstuvABCDEFGHJKLMNPQRSTUV]$
```
## Easting and Northing
Both easting and northing are integers that between 1 to 5 digits long depending on the used precision. A 5-digit integer will give a coordinate in meters. The same precision must be used for both integers.
```
^\d{1,5}$
```
