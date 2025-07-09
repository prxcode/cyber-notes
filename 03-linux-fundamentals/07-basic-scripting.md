# Basic Shell Scripting
Shell scripts are files that contain a series of shell commands.

### Creating a script
```
#!/bin/bash
echo "Hello, world!"
```
save it as hello.sh, then:
```
chmod +x hello.sh
./hello.sh
```

### Variables
```
name="Alice"
echo "Hello, $name"
```
### Loops
- For Loop:
```
for i in 1 2 3; do
  echo $i
done
```
- While Loop:
```
count=1
while [ $count -le 5 ]; do
  echo $count
  ((count++))
done
```

### Conditional Statements
```
if [ $age -ge 18 ]; then
  echo "Adult"
else
  echo "Minor"
fi
```