# Python-week-4-assignments
def read_and_modify_file(input_filename, output_filename):
    try:
        # Open the input file for reading
        with open(input_filename, 'r') as infile:
            content = infile.readlines()

        # Modify the content (for example, converting to uppercase)
        modified_content = [line.upper() for line in content]

        # Write the modified content to the output file
        with open(output_filename, 'w') as outfile:
            outfile.writelines(modified_content)

        print(f"Modified content has been written to '{output_filename}'.")

    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' does not exist.")
    except IOError:
        print(f"Error: Could not read from '{input_filename}' or write to '{output_filename}'.")

def main():
    # Ask the user for a filename
    input_filename = input("Enter the input filename: ")
    output_filename = input("Enter the output filename: ")

    read_and_modify_file(input_filename, output_filename)

if __name__ == "__main__":
    main()
    
