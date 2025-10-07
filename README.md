# ASSIGNMENT-4-
# Module 5: Files, Exceptions, and Errors in Python
 

# Task 1: Read a File and Handle Errors  

# Problem Statement  
Write a Python program to:  
1. Open and read a file named `sample.txt`.  
2. Print its content line by line.  
3. Handle errors gracefully if the file does not exist.  

try:
   # Try to open the file in read mode
    with open("sample.txt", "r") as file:
        print("Reading file content :")
        # Read all lines one by one
        lines = file.readlines()
        
        # Print each line with line number
        for i, line in enumerate(lines, start=1):
            print(f"Line {i} : {line.strip()}")
except FileNotFoundError:
# If file is not found, show this message
    print("Error : The file 'sample.txt' was not found.")


# Sample Input File (`sample.txt`)

This is a sample text file
It contains multiple lines
# Output  

Reading file content :
Line 1 : This is a sample text file
Line 2 : It contains multiple lines




##  Task 2: Write and Append Data to a File  

# Problem Statement  
Write a Python program to:  
1. Take user input and write it to a file named `output.txt`.  
2. Append additional text to the same file.  
3. Read and display the final content of the file.  



# Example   
# Step 1: Take user input and write to file
data = input("Enter text to write to the file: ")
with open("output.txt", "w") as file:
    file.write(data + "\n")
print("Data successfully written to output.txt.")

# Step 2: Append additional data
more_data = input("Enter additional text to append: ")
with open("output.txt", "a") as file:
    file.write(more_data + "\n")
print("Data successfully appended.")

# Step 3: Read and display final content
print("Final content of output.txt:")
with open("output.txt", "r") as file:
    lines = file.readlines()
    for line in lines:
        print(line.strip())

###  Example Input & Output  

Enter text to write to the file: Hello Python
Data successfully written to output.txt.
Enter additional text to append: Learning with python
Data successfully appended.
Final content of output.txt:
Hello Python
Learning with python
