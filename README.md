# Day4 Assignment
1. To launch the process and record its Job ID 
```
cat /dev/zero > /dev/null &
```

2. To display detailed information about the process
```
ps -fp 15425
```
3. To save the full output to a file named process_info.txt
```
ps -fp 15425 > process_info.txt
```
4. To change the priority (niceness) of the process to a value between 10 and 15
```
sudo renice 12 -p 15425
```
5. To verify the new niceness value and append it to process_info.txt
```
echo "=== Niceness Verification ===" >> process_info.txt
ps -o pid,ni,cmd -p 15425 >> process_info.txt
```
6. To terminate the process using its PID
```
kill 15425
```
7. To verify the process is no longer running
```
ps -p 15425
jobs
```
