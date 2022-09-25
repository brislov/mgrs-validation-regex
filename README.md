# Validation regex for MGRS coordinates

## Zone

* 01-60 (possible to omitt the leading 0) 
* A-Z (except I and O)

```
^(([0-5]?[0-9])|60)[ABCDEFGHJKLMNPQRSTUVWXYZ]$
```
