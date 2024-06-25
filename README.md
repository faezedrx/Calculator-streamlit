# 📟 Calculator App

This is a simple calculator application built using Streamlit and Python. The application allows users to perform basic arithmetic operations such as addition, subtraction, multiplication, and division.

## ✨ Features

- **Basic Arithmetic Operations**: Perform addition, subtraction, multiplication, and division.
- **Clear Input**: Clear the current input using the "C" button.
- **Display Result**: The result of the calculation is displayed and can be used for further operations.
- **Responsive UI**: The user interface is designed to be responsive and user-friendly.

## 📦 Installation

To run this application, you need to have Python installed on your system. Follow the steps below to set up and run the application:

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/calculator-app.git
    cd calculator-app
    ```

2. Create a virtual environment and activate it:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## 🚀 Usage

To run the application, use the following command:

```bash
streamlit run app.py
```
This will start a local server. Open your web browser and navigate to http://localhost:8501 to access the application.

## 📝 Code Overview

The main functionality of the calculator is implemented in `app.py`. Here is an overview of the key parts of the code:

- **Display and Input Handling**: The input and result are displayed using Streamlit's `st.empty()` and updated dynamically with `markdown` for larger font size.
- **Operations**: Functions are defined to handle basic arithmetic operations (`Addition`, `Subtraction`, `Multiplication`, `Division`) and update the display accordingly.
- **Buttons**: The virtual keyboard layout is created using Streamlit's `columns`, and button actions are defined to update the input and perform calculations.
- **Clear Input**: A function to clear the current input and reset the display.

### Key Functions

- `update_display(value)`: Appends the given value to the current input and updates the display.
- `set_operation(op)`: Sets the operation (e.g., addition, subtraction) to be performed, stores the current input, and resets the input field.
- `calculate_result()`: Performs the selected arithmetic operation using the stored value and the current input, displays the result, and resets the operation.
- `clear_input()`: Clears the current input and resets the display to "0".

### Button Layout

The calculator's buttons are organized in a 4x4 grid using Streamlit's `columns`. Each button updates the display or performs an operation when clicked.

```python
# Example of button layout code
col1, col2, col3, col4 = st.columns(4)

with col1:
    if st.button("7"):
        update_display("7")
    if st.button("4"):
        update_display("4")
    if st.button("1"):
        update_display("1")
    if st.button("0"):
        update_display("0")

with col2:
    if st.button("8"):
        update_display("8")
    if st.button("5"):
        update_display("5")
    if st.button("2"):
        update_display("2")
    if st.button("."):
        update_display(".")

with col3:
    if st.button("9"):
        update_display("9")
    if st.button("6"):
        update_display("6")
    if st.button("3"):
        update_display("3")
    if st.button("="):
        calculate_result()

with col4:
    if st.button(emoji.emojize(":heavy_plus_sign:")):
        set_operation("Addition")
    if st.button(emoji.emojize(":heavy_minus_sign:")):
        set_operation("Subtraction")
    if st.button(emoji.emojize(":heavy_multiplication_x:")):
        set_operation("Multiplication")
    if st.button(emoji.emojize(":heavy_division_sign:")):
        set_operation("Division")
    if st.button("C"):
        clear_input()
```

## 🎨 Customization

You can customize the application by modifying app.py. For example, you can change the button styles, add more operations, or modify the layout.

## 🤝 Contributing

Contributions are welcome! If you have any suggestions or improvements, feel free to create an issue or submit a pull request.

## 📧 Contact
If you have any questions or need further assistance, feel free to contact me at faezedrx@gmail.com.
