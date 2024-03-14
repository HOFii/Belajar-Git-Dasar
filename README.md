GIT DASAR

1.Poin-Poin Utama:

A. Apa itu Git

    Git adalah sebuah sistem kontrol versi yang sangat populer dan kuat yang digunakan oleh pengembang perangkat lunak untuk mengelola perubahan dalam kode sumber proyek, Dikembangkan oleh Linus Torvalds pada tahun 2005, Git dirancang untuk menjadi cepat, efisien, dan mudah digunakan, serta mendukung kerja tim yang terdistribusi.
    
B. Cara kerja Git

    a) Cara membuat repository didalam Git
         1. Cara membuat repository di Git bisa menggunakan Tools seperti GitBash atau terminal dan Cukup gunakan
            perintah "cd /path/to/your/project/directory", gunakan cd(change directory) untuk berpindah directory 
            atau ke tempat anda menyimpan repository Git anda.
            
         2. Gunakan perintah "git init" untuk menginisialisasi repositori Git baru di direktori saat ini, nanti Git
            akan secara otomatis membuatkan file baru bernama ".git", sangat dianjurkan untuk tidak
            mengubah/memodifikasi isi file tersebut.
            
          3. Git memiliki 3 langkah kerja: Modifed, Staged dan Committed.
           -Modifed artinya menambah, mengedit dan menghapus file. Namun belum disimpan secara permanen ke 
           Repository.
           -Staged artinya menandai modifikasi yang kita lakukan terhadap file dan akan disimpan secara permanen 
           ke Repository.
           -Committed artinya data sudah di simpan kedalam Repository.
           
           4. Git memiliki 3 Section yang berbeda: Working Directory, Staging Area dan Repository.
            -Working Directory, tempat kita melalakukan modifikasi file, bisa menggunakan perintah "git add" untuk
            pindah dari Working Directory ke Staging Area/Staging Index.
            -Staging Area, tempat dimana file sudah disiapkan dan disimpan secara permanen, dan di sini kita bisa
            melihat semua perubahan file. Dan gunakan perintah "git commmit" untuk melakukan commit dari Staging 
            Area ke Repository
            -Repository, tempat dimana semua file dan riwayat disimpan.
            
    b) Code Git Dasar
        1.Anda bisa menggunakan perintah "git add namafile" untuk menambahkan file baru didalam repository atau 
        jika file nya lebih dari satu atau banyak anda bisa menggunakan perintah "git add ." untuk menambahkan file 
        ke Staging Area/Staging Index.
        
        2. Anda bisa menggunakan perintah "git commit -m" untuk melakukan commit atau perubahan pada file.
        
        3. Lalu anda bisa menggunakan perintah "git status" untuk melihat perubahan pada file, seperti 
         penambahan file baru, file yang dihapus, file yang dimodifikasi dll.
         
        4. Anda bisa mengecek apakah ada file baru yang ditambahkan atau tidak dengan menggunakan perintah
        "git diff", nanti git akan menampilkan file mana yang berubah dan apa yang berubah dari file tersebut.
        
        5. Anda juga bisa membatalkan perubahan menggunakan perintah "git restore namafile".
        
        6. Anda bisa membatalkan file yang sudah terlanjur di commit ke Staging Index kembali ke 
        Working Directory dengan menggunakan perintah "git restore --staged namafile".
        
        7. Anda bisa melihat riwayat perubahan, siapa yang merubah, memodifikasi, menghapus file dan tanggal kapan 
        perubahan dilakukan dengan menggunakan perintah "git log".
        
        8. Ada cara lebih simple untuk melihat perubahan yaitu dengan menggunakan perintah "git log --oneline".
        
        9. Dan saat ingin menlihat detail dari perubahan anda bisa menggunakan perintah "git show hash" 
        (hash kode 6 digit pertama saat melakukan perintah 'git log').
        
        10. Anda bisa merubah nama file di Staging Index menggunakan perintah "git add namafile" nanti git akan 
        secara otomatis tau kalau isi filenya sama maka akan menggubah nama file tersebut.
        
    c) Mode Git Reset
        1. Menggunakan "git reset" dengan mode "--soft" memindahkan penunjuk HEAD ke commit yang berbeda 
        tanpa mengubah staging index dan working directory, menjadikannya opsi yang aman untuk membatalkan commit.

        2. "git reset" dengan mode "--mixed" memindahkan penunjuk HEAD dan mengatur ulang staging index ke 
        commit yang ditentukan sambil mempertahankan perubahan di working directory, sehingga memungkinkan 
        penyesuaian lebih lanjut sebelum melakukan commit.

        3. "git reset" dengan mode "--hard" mereset penunjuk HEAD, staging index, dan working directory 
        ke commit yang ditentukan, secara efektif menghapus semua perubahan, namun menjadikannya juga
        opsi yang beresiko untuk membatalkan commit.
        
    d) Git Amend Commit
        1. Perintah "git amend commit" digunakan untuk memperbaiki atau menambahkan perubahan pada commit
        terakhir Anda. Ini berguna ketika Anda ingin menambahkan perubahan ke dalam komit terakhir tanpa 
        membuat commit baru dengan menggabungkan commit.
        
    e) Snapshot 
        1. Perintah "git checkout hash" digunakan untuk melihat perubahan yang sudah dilakukan sebelumnya.
        
    f) Revert Commit
        1. Perintah "git revert" digunakan untuk membatalkan commit sebelumnya dengan membuat commit
        baru dengan perubahan yang berlawanan dengan perubahan yang dikembalikan. Berbeda dengan reset,
        git revert tidak menghapus riwayat tetapi membuat commit baru yang membalikkan perubahan yang
        dibuat oleh commit sebelumnya. Dan ketika menggunakan perintah "git revert" dapat secara 
        otomatis membatalkan perubahan yang dibuat pada commit tertentu, membuat commit baru dengan perubahan
        yang berlawanan.
        
    g) GitIgnore
        1. Dengan menambahkan file ".gitignore" di repository anda bisa mengtrack atau memilih file mana 
        yang tidak dibutihkan di repository. Anda bisa memasukan nama filenya atau nama foldernya.
        
    h) Git Blame
        1. Dengan menggunakan perintah "git blame namafile" anda dapat melihat siapa author, waktu, hash dan isi.
        Dan jika ingin melihat detailnya anda dapat menggunakan perintah "git show hash"
        
    i) Alias 
        1. Digunakan untuk menambahkan nama perintah yang sudah ada di dalam Git, bisanya digunakan untuk
        mempersingkat. Contoh perintahnya "git config --global alias.logone 'log --oneline'" anda bisa menambahkan 
        petik dua jika perintahnya terlalu panjang.
        
3. Pertanyaan dan Catatan Tambahan

a.Saya jarang menggunakan perintah “git reset”, dikarenakan masih kaku dalam penggunaannya dan
apa nanti saat terjun ke project perintah itu sering dipakai? 

5. Kesimpulan

Penggunaan Git Dalam pengembangan dan management perangkkat lunak sangat penting. Ditambah Git merupakan
Control Version yang kuat yang dapat melihat dan mencatat perubahan. Sangat penting bagi saya untuk bisa menguasai
Git sebelum terjun kedalam project sungguhan.
   
         
