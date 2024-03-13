import tkinter as tk

def btn_click(item):
    global expression
    expression = expression + str(item)
    input_text.set(expression)

def btn_clear():
    global expression
    expression = ""
    input_text.set("")

def btn_equal():
    global expression
    try:
        result = str(eval(expression))
        input_text.set(result)
        expression = ""
    except:
        input_text.set("Error")
        expression = ""

expression = ""

# Create a window
window = tk.Tk()
window.title("Calculator")
window.geometry("300x400")
window.resizable(False, False)

# Entry field
input_text = tk.StringVar()
input_field = tk.Entry(window, textvariable=input_text, font=("Arial", 18))
input_field.grid(row=0, column=0, columnspan=4, padx=10, pady=10)

# Buttons
buttons = [
    ("7", 1, 0), ("8", 1, 1), ("9", 1, 2), ("/", 1, 3),
    ("4", 2, 0), ("5", 2, 1), ("6", 2, 2), ("*", 2, 3),
    ("1", 3, 0), ("2", 3, 1), ("3", 3, 2), ("-", 3, 3),
    ("0", 4, 0), (".", 4, 1), ("=", 4, 2), ("+", 4, 3)
]

for (text, row, col) in buttons:
    btn = tk.Button(window, text=text, padx=20, pady=20, font=("Arial", 14), command=lambda text=text: btn_click(text))
    btn.grid(row=row, column=col)

# Clear button
btn_clear = tk.Button(window, text="C", padx=20, pady=20, font=("Arial", 14), command=btn_clear)
btn_clear.grid(row=5, column=0, columnspan=3)

# Equal button
btn_equal = tk.Button(window, text="=", padx=20, pady=20, font=("Arial", 14), command=btn_equal)
btn_equal.grid(row=5, column=3)

window.mainloop()
