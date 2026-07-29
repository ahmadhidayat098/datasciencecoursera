## This is a markdown file
# ============================
# Program E-Commerce Sederhana
# ============================

# Data Produk
produk <- data.frame(
  ID = c(1, 2, 3, 4),
  Nama = c("Laptop", "Mouse", "Keyboard", "Headset"),
  Harga = c(8500000, 150000, 350000, 450000)
)

# Menampilkan daftar produk
cat("===== DAFTAR PRODUK =====\n")
print(produk)

# Input dari pengguna
id <- as.numeric(readline("Masukkan ID Produk: "))
jumlah <- as.numeric(readline("Masukkan Jumlah: "))

# Mencari produk
pilihan <- produk[produk$ID == id, ]

# Cek apakah produk ada
if(nrow(pilihan) == 0){
  cat("Produk tidak ditemukan!\n")
} else {

  total <- pilihan$Harga * jumlah

  cat("\n===== STRUK BELANJA =====\n")
  cat("Produk :", pilihan$Nama, "\n")
  cat("Harga  : Rp", pilihan$Harga, "\n")
  cat("Jumlah :", jumlah, "\n")
  cat("---------------------------\n")
  cat("Total  : Rp", total, "\n")
}
