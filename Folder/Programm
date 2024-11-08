import tkinter as tk
from tkinter import messagebox

def is_prime(num):
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

def find_primes(n):
    primes = []
    num = 2
    while len(primes) < n:
        if is_prime(num):
            primes.append(num)
        num += 1
    return primes

def calculate_primes():
    try:
        # Проверка на ввод только цифр
        if not entry.get().isdigit():
            raise ValueError("Неправильное значение")
        
        n = int(entry.get())
        if n < 1:
            raise ValueError("Введите положительное число.")
        
        primes = find_primes(n)
        result_var.set(', '.join(map(str, primes)))
    except ValueError as e:
        messagebox.showerror("Ошибка", str(e))

root = tk.Tk()
root.title("Поиск простых чисел")

root.geometry("500x300")
root.resizable(False, False)

entry_label = tk.Label(root, text="Введите количество простых чисел:")
entry_label.pack(fill=tk.X, expand=True, padx=10, pady=5)
entry = tk.Entry(root)
entry.pack(fill=tk.X, expand=True, padx=10, pady=5)

result_label = tk.Label(root, text="Простые числа:")
result_label.pack(fill=tk.X, expand=True, padx=10, pady=5)
result_var = tk.StringVar()
result_output = tk.Label(root, textvariable=result_var, relief=tk.SUNKEN)
result_output.pack(fill=tk.BOTH, expand=True, padx=10, pady=5)

calc_button = tk.Button(root, text="Рассчитать", command=calculate_primes)
calc_button.pack(fill=tk.X, expand=True, padx=10, pady=5)

root.mainloop()
