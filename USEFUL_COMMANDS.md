#### Command to change permissions only on files not directories

`find . -type f -exec chmod 644 {} \;`

or 

`find . -type f -print0 | xargs -0 -I {} chmod 644 {}`