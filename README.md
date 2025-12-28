import tkinter as tk
from tkinter import messagebox

# Your existing function
def to_screaming_snake_case(text):
    return text.replace('.', '_').upper()

def handle_mosque_click(integer_input):
    messagebox.showinfo("Mosque Click", f"Handling integer input: {integer_input}")

def check_azan_time():
    messagebox.showinfo("Azan Time", "Checking azan time...")

def handle_azan_voice_input(voice_input_code):
    messagebox.showinfo("Azan Voice", f"Processing azan voice input: {voice_input_code}")

# GUI setup
root = tk.Tk()
root.title("My App")
root.geometry("400x300")

# SCREAMING_SNAKE_CASE section
tk.Label(root, text="Enter text to convert:").pack(pady=5)
input_entry = tk.Entry(root, width=30)
input_entry.pack(pady=5)

def convert_text():
    text = input_entry.get()
    converted = to_screaming_snake_case(text)
    messagebox.showinfo("Converted Text", converted)

tk.Button(root, text="Convert", command=convert_text).pack(pady=10)

# Mosque click simulation
tk.Button(root, text="Mosque Click", command=lambda: handle_mosque_click(1)).pack(pady=5)

# Azan time check
tk.Button(root, text="Check Azan Time", command=check_azan_time).pack(pady=5)

# Azan voice input simulation
tk.Button(root, text="Azan Voice Input", command=lambda: handle_azan_voice_input("VOICE123")).pack(pady=5)

root.mainloop()
