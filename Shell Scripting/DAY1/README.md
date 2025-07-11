# 🐧 Bash Scripting Guide

A fun and practical guide to learning Bash scripting basics using everyday examples and characters from *Taarak Mehta Ka Ooltah Chashmah*. 🎬

---

## 🧱 Basic Bash Concepts

| Concept | Syntax | Description |
|--------|--------|-------------|
| **Shebang** | `#!/bin/bash` | Declares the script uses Bash |
| **Single-line comment** | `# This is a comment` | Used to explain code |
| **Multi-line comment** | `: <<'COMMENT' ... COMMENT` | Block comment (ignored during execution) |
| **Variable** | `name="jetha"` | `name` is variable storing the string "jetha" |
| **Print text** | `echo "Hello"` | Displays output |
| **Date command** | `date=$(date)` | Stores current date in a variable |
| **User input** | `read name` | Reads user input into `name` |
| **Add user** | `sudo useradd -m $username` | Adds user with home directory |
| **Script arguments** | `$0`, `$1`, `$2` | `$0` = script name, `$1`, `$2` = arguments |

> 📌 Example usage:  
> `./script.sh daya`  
> Output: `The characters in jethalal society are daya`

---

## 🧠 Conditional Statements

### `if`, `elif`, `else` Example:

```bash
#!/bin/bash

read -p "Jetha ne mud ke kisse dekha: " bandi
read -p "Jetha ka pyaar %: " pyaar

if [[ $bandi == "daya bhabi" ]]; then
    echo "Jetha is loyal"
elif [[ $pyaar -ge 100 ]]; then
    echo "Jetha is loyal"
else
    echo "Jetha is not loyal"
fi
```
## 🔁 Loops in Bash

### ➤ for Loop (Fixed Range)

```bash
      #!/bin/bash
      for ((i=1; i<=5; i++))
      do
          mkdir "demo$i"
      done
```
### ➤ for Loop with Arguments
```bash
      #!/bin/bash
      <<COMMENT
            $1 = Folder name prefix
            $2 = Start range
            $3 = End range
            Example: ./script.sh demo 1 3
            Creates: demo1, demo2, demo3
      COMMENT
            for (( i=$2; i<=$3; i++ ))
            do
                mkdir "$1$i"
            done
```
- Note :🧹 To delete all folders created this way: `rm -r demo*`
### ➤ while Loop Example 1 (Simple)
```bash
#!/bin/bash

num=0
while [[ $num -le 5 ]]
do
    echo "wow"
    num=$((num+1))
done
```
### ➤ while Loop Example 2 (Even Numbers)
```bash
#!/bin/bash

num=0
while [[ $num -le 10 ]]
do
    echo $num
    num=$((num+2))
done
```
## 🧩 Bash Functions

### 🔸 Function Without Arguments
```bash
#!/bin/bash

function is_loyal() {
    read -p "Jetha ne mud ke kisse dekha: " bandi
    read -p "Jetha ka pyaar %: " pyaar

    if [[ $bandi == "daya bhabi" ]]; then
        echo "Jetha is loyal"
    elif [[ $pyaar -ge 100 ]]; then
        echo "Jetha is loyal"
    else
        echo "Jetha is not loyal"
    fi
}

is_loyal

```
### 🔸 Function With Arguments
```bash
#!/bin/bash

function is_loyal() {
    read -p "$1 ne mud ke kisse dekha: " bandi
    read -p "$1 ka pyaar %: " pyaar

    if [[ $bandi == "daya bhabi" ]]; then
        echo "$1 is loyal"
    elif [[ $pyaar -ge 100 ]]; then
        echo "$1 is loyal"
    else
        echo "$1 is not loyal"
    fi
}

is_loyal "Iyer"
```
### 📘Notes
- Use chmod +x script.sh to make your Bash script executable.
- Use ./script.sh arg1 arg2 to pass arguments.
- read allows interactive input from users.
- Script arguments:
- $0 → script name
- $1, $2, ... → passed parameters
- Use echo for printing values and debugging.
- Use proper quoting ("$1") for variable expansion.
