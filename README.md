# Лабораторная работа №9
import tkinter as tk
import math
root = tk.Tk() 
root.geometry("800x500")
root.title("КУЛЬКУЛЯТОР") 
root.configure(bg='#4B0082')
def on_button_click(value):
    try:
        if value == "=": 
            result = eval(textbox.get("1.0", tk.END))
            textbox.delete("1.0", tk.END)
            textbox.insert(tk.END, result)
        elif value == "Пупис😁":
            print("Пупис😁")
            textbox.delete("1.0", tk.END)
        elif value == "√":
            koren = textbox.get("1.0", tk.END).strip()
            if koren:
                evan = eval(koren)
                sqrt_math = math.sqrt(evan)
                textbox.delete("1.0", tk.END)
                textbox.insert(tk.END, str(sqrt_math))   
        else: 
            print(value)
            textbox.insert(tk.END, value + "")
        

    except Exception as v:
        textbox.delete("1.0", tk.END)
        textbox.insert(tk.END, "ха-ха опшипка")
        print(f"Произошла опшипка: {v}")
        


        
label = tk.Label(root, text="раз два три четыре пять зайчик вышел погулять", font=("Arial", 18), bg="#9370DB") 
label.pack(padx=20, pady=20,)
textbox = tk.Text(root, height=3, font=("Arial", 16), bg="#E0FFFF") 
textbox.pack() 
buttonFrame = tk.Frame(root)
buttonFrame.columnconfigure(0, weight=1) 
buttonFrame.columnconfigure(1, weight=1) 
buttonFrame.columnconfigure(2, weight=1) 
buttonFrame.columnconfigure(3, weight=1)
btn111 = tk.Button(buttonFrame, text="(", font=("Arial", 18), bg="#008080", command=lambda v="(": on_button_click(v)) 
btn111.grid(row=0, column=0, sticky="we") 
btn222 = tk.Button(buttonFrame, text=")", font=("Arial", 18), bg="#008080", command=lambda v=")": on_button_click(v)) 
btn222.grid(row=0, column=1, sticky="we") 
btn333 = tk.Button(buttonFrame, text=".", font=("Arial", 18), bg="#008080", command=lambda v=".": on_button_click(v)) 
btn333.grid(row=0, column=2, sticky="we") 
btn444 = tk.Button(buttonFrame, text="-", font=("Arial", 18), bg="#008080", command=lambda v="-": on_button_click(v)) 
btn444.grid(row=0, column=3, sticky="we")
btn555 = tk.Button(buttonFrame, text="√", font=("Arial", 18), bg="#008080", command=lambda v="√": on_button_click(v))
btn555.grid(row=0, column=3, sticky="we")
btn1 = tk.Button(buttonFrame, text="1", font=("Arial", 18), bg="#8B0000", command=lambda v="1": on_button_click(v)) 
btn1.grid(row=1, column=0, sticky="we") 
btn2 = tk.Button(buttonFrame, text="2", font=("Arial", 18), bg="#E9967A", command=lambda v="2": on_button_click(v)) 
btn2.grid(row=1, column=1, sticky="we") 
btn3 = tk.Button(buttonFrame, text="3", font=("Arial", 18), bg="#FFD700", command=lambda v="3": on_button_click(v)) 
btn3.grid(row=1, column=2, sticky="we") 
btn4 = tk.Button(buttonFrame, text="-", font=("Arial", 18), bg="#008080", command=lambda v="-": on_button_click(v)) 
btn4.grid(row=1, column=3, sticky="we")
btn5 = tk.Button(buttonFrame, text="4", font=("Arial", 18), bg="#556B2F", command=lambda v="4": on_button_click(v)) 
btn5.grid(row=2, column=0, sticky="we") 
btn6 = tk.Button(buttonFrame, text="5", font=("Arial", 18), bg="#6495ED", command=lambda v="5": on_button_click(v)) 
btn6.grid(row=2, column=1, sticky="we") 
btn7 = tk.Button(buttonFrame, text="6", font=("Arial", 18), bg="#191970", command=lambda v="6": on_button_click(v)) 
btn7.grid(row=2, column=2, sticky="we") 
btn9 = tk.Button(buttonFrame, text="+", font=("Arial", 18), bg="#008080", command=lambda v="+": on_button_click(v)) 
btn9.grid(row=2, column=3, sticky="we")
btn10 = tk.Button(buttonFrame, text="7", font=("Arial", 18), bg="#9370DB", command=lambda v="7": on_button_click(v))
btn10.grid(row=3, column=0, sticky="we") 
btn11 = tk.Button(buttonFrame, text="8", font=("Arial", 18), bg="#FF69B4", command=lambda v="8": on_button_click(v)) 
btn11.grid(row=3, column=1, sticky="we") 
btn12 = tk.Button(buttonFrame, text="9", font=("Arial", 18), bg="#2F4F4F", command=lambda v="9": on_button_click(v)) 
btn12.grid(row=3, column=2, sticky="we") 
btn13 = tk.Button(buttonFrame, text="*", font=("Arial", 18), bg="#008080", command=lambda v="*": on_button_click(v)) 
btn13.grid(row=3, column=3, sticky="we")
btn14 = tk.Button(buttonFrame, text="Пупис😁", font=("Arial", 18), bg="#008080", command=lambda v="Пупис😁": on_button_click(v)) 
btn14.grid(row=4, column=0, sticky="we") 
btn15 = tk.Button(buttonFrame, text="0", font=("Arial", 18), bg="#708090", command=lambda v="0": on_button_click(v)) 
btn15.grid(row=4, column=1, sticky="we") 
btn16 = tk.Button(buttonFrame, text="=", font=("Arial", 18), bg="#008080", command=lambda v="=": on_button_click(v)) 
btn16.grid(row=4, column=2, sticky="we") 
btn17 = tk.Button(buttonFrame, text="/", font=("Arial", 18), bg="#008080", command=lambda v="/": on_button_click(v))
btn17.grid(row=4, column=3, sticky="we")
buttonFrame.pack(fill="x")
root.mainloop()
