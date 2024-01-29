# Copy updated LED Script

## 1. First navigate to the directory where the script is located
```bash
cd /home/harddrive
```

##  2. Next, login to the server via sftp

```bash
sudo sftp harddrive@192.168.1.100
```

If it asks the following
```
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```
Type `yes` and press enter.

## 3. Navigate to the directory where the script is located

```bash
cd /home/harddrive
```

## 4. Copy the script from the server to the local machine

```bash
get -r sdled
```

## 5. Exit sftp

```bash
exit
```

## 6. Run `led` script

```bash
led
```