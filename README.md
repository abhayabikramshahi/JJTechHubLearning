# Essential Topics in Computer Science

## 1. Computer System

### Definition
A computer system is a combination of hardware and software components that work together to perform computational tasks.

### Components
- **Hardware**: Physical components (CPU, RAM, Hard Drive, etc.)
- **Software**: Programs that run on the computer (Operating System, Applications)
- **Input Devices**: Keyboard, Mouse, Scanner
- **Output Devices**: Monitor, Printer, Speaker
- **Storage Devices**: HDD, SSD, USB, Cloud Storage

### Functions
- Data Processing
- Data Storage and Retrieval
- Networking and Communication

### Example Code (Python: Check System Info)
```python
import platform
import psutil

def get_system_info():
    return {
        "System": platform.system(),
        "Version": platform.version(),
        "Processor": platform.processor(),
        "RAM Size": f"{psutil.virtual_memory().total / (1024**3):.2f} GB"
    }

info = get_system_info()
for key, value in info.items():
    print(f"{key}: {value}")
```

## 2. Number System

### Definition
A number system is a way to represent numbers in a structured format.

### Types of Number Systems
- **Binary (Base-2)**: Uses 0 and 1 (e.g., 1011)
- **Decimal (Base-10)**: Uses digits 0-9 (e.g., 1234)
- **Octal (Base-8)**: Uses digits 0-7 (e.g., 57)
- **Hexadecimal (Base-16)**: Uses 0-9 and A-F (e.g., 1F3)

### Conversion Methods
- Binary to Decimal & Vice Versa
- Decimal to Octal & Vice Versa
- Binary to Hexadecimal & Vice Versa

### Example Code (Python: Convert Binary to Decimal and Vice Versa)
```python
def binary_to_decimal(binary):
    return int(binary, 2)

def decimal_to_binary(decimal):
    return bin(decimal)[2:]

binary_number = "1011"
decimal_number = 11

print(f"Binary to Decimal ({binary_number}):", binary_to_decimal(binary_number))
print(f"Decimal to Binary ({decimal_number}):", decimal_to_binary(decimal_number))
```

## 3. Block Programming

### Definition
Block programming is a visual way of coding where blocks represent code instructions.

### Features
- Drag-and-drop interface
- No syntax errors
- Beginner-friendly

### Examples
- **Scratch** (Popular for teaching programming)
- **Blockly** (Used in Google’s programming tools)
- **MIT App Inventor** (For mobile app development)

### Advantages
- Easy for beginners
- Encourages problem-solving
- Quick prototyping

### Example Code (Scratch Concept in Python: Block-Based Equivalent)
```python
def say_hello(name):
    print(f"Hello, {name}!")

name = input("Enter your name: ")
say_hello(name)
```

## 4. Web Technology

### Definition
Web technology refers to tools and techniques used to develop web applications and websites.

### Components
- **HTML** (HyperText Markup Language): Structure of a webpage
- **CSS** (Cascading Style Sheets): Styling of a webpage
- **JavaScript**: Makes webpages interactive
- **Backend Technologies**: PHP, Node.js, Python (Flask/Django)
- **Databases**: MySQL, MongoDB
- **Web Hosting & Domains**: Deploying websites

### Modern Trends
- **Responsive Design** (Mobile-friendly sites)
- **Progressive Web Apps (PWAs)** (Faster web applications)
- **Single Page Applications (SPAs)** (Dynamic content without reloading)

### Example Code (HTML, CSS, JS: Interactive Webpage with Styled Button)
```html
<!DOCTYPE html>
<html>
<head>
    <title>My Web Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
        }
        button {
            background-color: #008CBA;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            font-size: 16px;
            border-radius: 5px;
        }
        button:hover {
            background-color: #005f73;
        }
    </style>
</head>
<body>
    <h1>Welcome to My Web Page</h1>
    <button onclick="sayHello()">Click Me</button>
    <script>
        function sayHello() {
            alert("Hello, World!");
        }
    </script>
</body>
</html>
