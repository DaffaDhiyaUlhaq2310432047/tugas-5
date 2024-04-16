print("Nama: Daffa Dhiya Ulhaq")
print("Nim : 2310431005")
print("TABEL FUNGSI")
print("f(x) = 3x² + 7x - 2, jika x >= 0")
print("     = 2x² - 5x - 4, jika x < 0")
print("g(x) = (f(x))² - √f(x)")
print("h(x) = f(x) * g(x)")

while True:
    n = int(input("\nInput banyak data n = "))
    nilai_x = [float(input(f"Input nilai x ke-{i+1} = ")) for i in range(n)]

    print("\nHasil:")
    
    column_width = 12
    column_titles = ["x", "f(x)", "g(x)", "h(x)"]
    total_width = 4 * column_width + 5  # 4 kolom, 1 space untuk setiap kolom dan 1 untuk pemisah "|" di akhir

    print("+" + "-" * (total_width - 2) + "+")

    print("|", end="")
    for title in column_titles:
        print(f" {title:<{column_width}} |", end="")
    print()  
    print("+" + "-" * (total_width - 2) + "+")

    for x in nilai_x:
        if x >= 0:
            fx = 3*x**2 + 7*x - 2
        else:
            fx = 2*x**2 - 5*x - 4

        gx = fx**2 - (fx ** 0.5)
        hx = fx * gx

        
        print("|", end="")
        print(f" {x:<{column_width}.2f} |", end="")
        print(f" {fx:<{column_width}.2f} |", end="")
        print(f" {gx:<{column_width}.2f} |", end="")
        print(f" {hx:<{column_width + 8}.2f} |")  
    print("+" + "-" * (total_width - 2) + "+")

    lagi = input("\nIngin memasukkan nilai x lagi? (Y/N) ")
    if lagi != 'Y' and lagi != 'y':
        print("Terima kasih telah menggunakan program ini.")
        break
