```mermaider
Diagram
    ANGGOTA ||--o{ PEMINJAMAN : "melakukan"
    PETUGAS ||--o{ PEMINJAMAN : "melayani"
    PEMINJAMAN ||--o{ DETAIL_PINJAM : "memiliki"
    BUKU ||--o{ DETAIL_PINJAM : "termasuk_dalam"
    
    ANGGOTA {
        ID_Anggota PK
        Nama
        Alamat
    } 

    PETUGAS {
        ID_Petugas PK
        Nama_Petugas
        Jabatan
    } 

    BUKU {
        ISBN PK
        Judul
        Pengarang
        Jumlah_Stok
    } 

    PEMINJAMAN {
        ID_Peminjaman PK
        Tanggal_Pinjam
        ID_Anggota FK
        ID_Petugas FK
        Status_Pinjaman
    } 

    DETAIL_PINJAM {
        ID_Peminjaman PK, FK
        ISBN PK, FK
        Jumlah_Buku_Dipinjam
    }

ERD Peminjaman Buku
