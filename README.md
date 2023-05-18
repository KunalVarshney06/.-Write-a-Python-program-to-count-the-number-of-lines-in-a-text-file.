# .-Write-a-Python-program-to-count-the-number-of-lines-in-a-text-file.
def count_lines(file_path):
    line_count = 0
    try:
        with open(file_path, 'r') as file:
            for line in file:
                line_count += 1
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while reading the file.")
    return line_count

# Example usage
file_path = 'path/to/your/text/file.txt'  # Replace with the actual file path
num_lines = count_lines(file_path)
print("Number of lines in the file:", num_lines)
