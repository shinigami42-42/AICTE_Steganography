# Image Steganography Application

This application implements image steganography, allowing users to encrypt and decrypt text messages within images using a password. It is built using Python and PyQt6 for the graphical user interface.

## Features

-   **Encryption:**
    -      Encrypts a text message into an image.
    -      Requires an image file path, a message, a password, and an output file path.
    -      Stores the message and password length and content within the image's pixel data.
    -      Validates input paths and file formats.
-   **Decryption:**
    -      Decrypts a message from an encrypted image.
    -      Requires the encrypted image file path and the correct password.
    -      Retrieves the hidden message if the password matches.
    -      Displays the decrypted message in the application.
    -   Validates input paths and file formats.
-   **User-Friendly GUI:**
    -      Uses PyQt6 to create a simple and intuitive graphical interface.
    -      Provides input fields for file paths, messages, and passwords.
    -      Displays success and error messages via message boxes.

## Prerequisites

-   Python 3.6 or later
-   PyQt6 (`pip install PyQt6`)
-   OpenCV (`pip install opencv-python`)
-   NumPy (`pip install numpy`)

## How to Run

1.  **Install Dependencies:**
    ```bash
    pip install PyQt6 opencv-python numpy
    ```
2.  **Save the Code:**
    -   Save the provided Python code as `ibm_prj.py`.
3.  **Run the Application:**
    ```bash
    python ibm_prj.py
    ```
4.  **Using the Application:**
    -   **Encryption:**
        -      Enter the path to the image you want to encrypt in the "File Path" field under "Encryption."
        -      Enter the message you want to hide in the "Text" field.
        -      Enter a password in the "Password" field.
        -   Enter the desired output path including the .png extension in the "Output Path" field.
        -      Click the "Encrypt" button.
        -   A message box will confirm the success of the encryption and show the output path.
    -   **Decryption:**
        -      Enter the path to the encrypted image in the "File Path" field under "Decryption."
        -      Enter the password used for encryption in the "Password" field.
        -      Click the "Decrypt" button.
        -      The decrypted message will be displayed below the "Decrypt" button.
        -   Error messages will appear in a message box if there is an issue.

## Code Explanation

-      The code uses OpenCV to read and write images and NumPy to manipulate pixel data.
-      The message and password are encoded by storing their lengths and character ASCII values in the image's pixel data.
-      The pixel manipulation is basic, storing the data in the least significant bits of the image.
-      PyQt6 is used to create the GUI elements, including labels, text fields, and buttons.
-      The `encrypt_image` and `decrypt_image` functions handle the core logic of the application.
-   Input validation is performed to ensure that file paths and passwords are provided.

## Important Notes

-   **Security:** This is a basic implementation of steganography and may not be suitable for highly sensitive information.
-   **Image Format:** The application currently supports PNG images for output.
-   **Error Handling:** Basic error handling is included, but further improvements can be made.
-   **Pixel Capacity:** Very long messages might not fit into smaller images.
-   **Password Strength:** Use a strong password.

## Future Improvements

-   Implement more robust encryption algorithms.
-   Add support for more image formats.
-   Improve error handling and input validation.
-   Enhance the GUI with progress bars and more detailed feedback.
-   Add an option to select the image file using a file dialog.
-   Add options to increase the amount of pixel data used, to increase message capacity.
