## Terminal Tricks

Check open ports withous netstat or lsof
```
declare -a array=($(tail -n +2 /proc/net/tcp | cut -d":" -f"3"|cut -d" " -f"1")) && for port in ${array[@]}; do echo $((0x$port)); done
```

## Python Scripting

**Sage/Python convert string to int**
```
import binascii
m_int = int(binascii.hexlify("Test"), 16)

# =====================
m_int = int("Test".encode("hex"), 16)
```

**Sage/Python Int to Hex**
```
integer = 1231231
'0x{:02x}'.format(integer)
```