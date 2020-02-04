## Command to change permissions only on files not directories

```
find . -type f -exec chmod 644 {} \;
```

or 

```
find . -type f -print0 | xargs -0 -I {} chmod 644 {}`
```

## Making functions and alias in bashrc or bash_profile

##### Alias

```
alias my_alias="command"
```

##### Function

```
myfunction () {
    echo "this is my function"
    echo "This is the function with positional argument $1"
}
```

