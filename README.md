# photo-highlights
Database and Python management systems for sorting and managing best photos of a local collection


## Architecture/Implementation
### Database/Storage
- SQLite database
- Table of directories (indicates which directory is it's parent)
- Table of Favorites, indicates parent directory and file name as primary key, other tags etc

### Scan the directories, to see if they exist still
- If one isn't found, give the option to browse for it, then fix all downstream errors
- Then check to see if all the files in the direcory are still there
- If file is missing search for it in sub directory file system, all the way down (ask if theis should be done) or if deleted on purpose
- If files are indicated to have moved up a directory etc, ask input for the directory of search, then create new entries in the db
- If new files found in the directory ask ithey want to sort them, or just add them with no tags/favorite

### On the Python side
- maintain list of directories to include and exlude
