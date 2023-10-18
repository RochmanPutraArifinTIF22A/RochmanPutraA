def bisection_method(func, a, b, tol, max_iter,):
    if func(a) * func(b) >= 0:
        print("Metode biseksi tidak dapat digunakan pada interval ini.")
        return None

    iter_count = 0
    while (b - a) / 2.0 > tol and iter_count < max_iter:
        c = (a + b) / 2
        if func(c) == 0:
            return c  # Ditemukan akar tepat
        elif func(c) * func(a) < 0:
            b = c
        else:
            a = c
        iter_count += 1

    return (a + b) / 2

# Contoh penggunaan metode biseksi untuk mencari akar fungsi f(x) = x^2 - 4
def f(x):
    return (x*x*x*x) - (x*x*x) + (2*x*x) - (2*x) - 12

a = -2.0  # Batas bawah interval
b = 0.0  # Batas atas interval
tolerance = 0.001  # Toleransi
max_iterations = 15  # Maksimum iterasi

root = bisection_method(f, a, b, tolerance, max_iterations)
if root is not None:
    print(f"Akar fungsi: {root:.6f}")
else:
    print("Metode biseksi tidak konvergen atau interval tidak sesuai.")
