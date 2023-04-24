# Vault

Vault adalah inti dari protokol. Vault bertanggung jawab untuk mencetak / menebus token OUSD, menyeimbangkan kembali dana antara berbagai strategi yang didukung, dan melikuidasi token hadiah.

Fungsi terpenting yang dapat dipanggil secara publik di Vault adalah:

* `mint ()`memungkinkan satu stablecoin yang didukung untuk diubah menjadi OUSD
* `mintMultiple ()`memungkinkan beberapa stablecoin yang didukung untuk dikonversi ke OUSD dalam satu panggilan
* `redeem ()`memungkinkan sejumlah OUSD ditukarkan dengan stablecoin lain yang didukung.
* `redeemAll ()`memungkinkan pengguna untuk menebus seluruh saldo OUSD mereka untuk stablecoin lain yang didukung. Ini sangat berguna karena saldo pengguna terus bertambah seiring bertambahnya hasil.
* `rebase ()`memperbarui saldo untuk semua pengguna berdasarkan nilai aset yang saat ini disimpan di kumpulan.
* `allocate ()`memindahkan aset di bawah manajemen ke dalam [Stategies](strategies.md) yang ditentukan untuk memaksimalkan hasil dan mendiversifikasi risiko.

Saat penebusan, adalah protokol dan bukan pengguna yang memutuskan stablecoin \ (s \) mana yang akan dikembalikan ke pengguna. Keputusan tentang coin mana \(s\) yang akan dikembalikan didasarkan pada rasio internal dari aset yang disimpan di pool.



