
# UniVerse

**UniVerse** is a Python module designed for encoding data using Unicode characters.

## Features

- Encode data into Unicode-based representations.
- Decode Unicode representations back to the original data.

## Installation

To install UniVerse, clone the repository:

```bash
git clone https://github.com/todo-jasny/UniVerse.git
```

Navigate to the project directory:

```bash
cd UniVerse
```

Install the required dependencies:

```bash
pip install .
```

## Example Usage

1. Uni Class
   Handles encoding and decoding Unicode strings to and from decimal Unicode code points.
   
   **Methods**:
   * `encode(text: str) -> str`
     Converts a string to its decimal Unicode code points, separated by spaces.
   * `decode(unicode_point: str) -> str`
     Converts a string of space-separated decimal Unicode code points back to text.

    ```python
    from UniVerse import Uni

    # Encode
    encoded = Uni.encode("Hello")
    print(encoded)  # Output: "72 101 108 108 111"

    # Decode
    decoded = Uni.decode("72 101 108 108 111")
    print(decoded)  # Output: "Hello"
    ```

3. Bin Class
   Handles encoding and decoding strings to binary repersentations
   
   **Methods**
   * `encode(text: str) -> str`
     Converts a string to its binary repersentation, seperates characters with spaces
   * `decode(binary_string: str) -> str`
     Converts the binary string back into Unicode text

    ```python
    from UniVerse import Bin

    # Encode
    binary = Bin.encode("Hi")
    print(binary)  # Output: "01001000 01101001"

    # Decode
    text = Bin.decode("01001000 01101001")
    print(text)  # Output: "Hi"
    ```

4. RGB Class
   Encodes strings into RGB tuples useing md5 hashing and decodes them back to text
   
   **Methods**
   * `encode(text: str) -> list[tuple]`
     Converts a string into a list of RGB tuples.
   * `decode(rgba_list: list[tuple]) -> str`
     Converts a list of RGB tuples back to text.

   ```python
   from UniVerse import RGB

    # Encode
    rgb = RGB.encode("A")
    print(rgb)  # Output: [(some RGB tuple)]

    # Decode
    text = RGB.decode([(some RGB tuple)])
    print(text)  # Output: "A"
   ```

5. CSC Class
Encodes and decodes strings using Caesar cipher manipulation.

**Methods**
  * `encode(text: str, shift: int) -> str`
   Shifts characters by a specified value. Adds shift value to front of text as a header.
  * `decode(csc_text: str) -> str`
  Decodes the shifted text, using header to get the shift value used

```python
from UniVerse import CSC

# Encode
encoded = CSC.encode("abc", 3)
print(encoded)  # Output: "3 def"

# Decode
decoded = CSC.decode("3 def")
print(decoded)  # Output: "abc"

```


## Contributing

Contributions are welcome! Please fork this repository and submit a pull request with your improvements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
