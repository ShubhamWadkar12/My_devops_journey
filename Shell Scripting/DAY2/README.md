# Intermediate Bash commands

## Error Handling

```bash
 #!/bin/bash
create_directory(){
        mkdir demo
}

if ! create_directory; then
        echo "The code is exited as the directory already exists"
        exit 1
fi

echo "this should not work bcz the code is interrupted"
```
