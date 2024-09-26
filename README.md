# IP Address Management for Restricted Subnetwork

## Objective
The objective of this project is to create a Python algorithm that manages an IP allow list for a healthcare company's restricted subnetwork. Employees can access restricted content based on their IP addresses, and certain IPs are periodically removed from the allow list as employees are no longer authorized to access the network. The goal is to identify and remove IP addresses that appear on a remove list, keeping the allow list up-to-date.

### Skills Learned
- Python programming for file management and data processing.
- Algorithm development for managing IP allow and remove lists.
- File handling operations in Python, including reading, writing, and modifying files.
- Application of conditional logic and list operations in Python.

### Tools Used
- Python 3.12.1 for scripting and file handling.
- Basic text file (`.txt`) management for reading and updating the allow list.
  
## Steps

### 1. Import and Read the File Contents
The first step is to import the `allow_list.txt` file and read its contents. The file contains the IP addresses of employees who are allowed to access the restricted subnetwork. 

```python
# Import the file 
import_file = "allow_list.txt"

# Open the file
with open(import_file, "r") as file: 
    ip_addresses = file.read()
```

### Text file for allowlist.txt
| IP Address        |
|-------------------|
| 192.168.25.60     |
| 192.168.205.12    |
| 192.168.97.225    |
| 192.168.6.9       |
| 192.168.52.90     |
| 192.168.158.170   |
| 192.168.90.124    |
| 192.168.186.176   |
| 192.168.133.188   |
| 192.168.203.198   |
| 192.168.201.40    |
| 192.168.218.219   |
| 192.168.52.37     |
| 192.168.156.224   |
| 192.168.60.153    |
| 192.168.58.57     |
| 192.168.69.116    |



### 2. Create list by converting the string
# Convert the string to a list

```ip_addresses = ip_addresses.split()```

# Display the list
```print(ip_addresses)```



### 3. Filter IP addresses to those only on the list
```IP addresses to be removed
remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

Iterate over the IP addresses and remove the ones in the remove list
for element in ip_addresses:
    if element in remove_list:
        ip_addresses.remove(element)

Display updated IP addresses
print(ip_addresses)
```
### 4. Place correct IP addresses in Updated file

```
# Convert list back to a string
ip_addresses = " ".join(ip_addresses)

# Write the updated list to the file
with open(import_file, "w") as file:
    file.write(ip_addresses)

# Display updated file contents
with open(import_file, "r") as file:
    text = file.read()

print(text)
```



### Final:
| IP Address        |
|-------------------|
| 192.168.25.60     |
| 192.168.205.12    |
| 192.168.6.9       |
| 192.168.52.90     |
| 192.168.90.124    |
| 192.168.186.176   |
| 192.168.133.188   |
| 192.168.203.198   |
| 192.168.218.219   |
| 192.168.52.37     |
| 192.168.156.224   |
| 192.168.60.153    |
| 192.168.69.116    |





