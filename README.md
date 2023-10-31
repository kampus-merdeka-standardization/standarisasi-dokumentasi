# Penulisan Dokumentasi Project

## Judul

Ini adalah nama dari projectnya. Ini menggambarkan keseluruhan proyek dalam satu kalimat, dan membantu orang memahami apa tujuan dan sasaran utama proyek tersebut.

## Deskripsi (naufal)

## Version History

Version history menggunakan Semantic Versioning (SemVer). SemVer berbentuk Major.Minor.Patch

![SemVer](https://camo.githubusercontent.com/e76dc140c69aa525577ee3e475f42a1f5e8af501e67260f9f7788d94cc5ee51f/68747470733a2f2f6d656469612e6765656b73666f726765656b732e6f72672f77702d636f6e74656e742f75706c6f6164732f73656d7665722e706e67)

Semantic Versioning merupakan bilangan 3 komponen dalam format X.Y.Z, dimana :
- X adalah singkatan dari versi Major. Angka paling kiri menunjukkan versi mayor. Saat Anda menambah nomor versi mayor, Anda menambahnya satu tetapi Anda menyetel ulang versi patch dan versi minor ke nol. Jika versi saat ini adalah 2.6.9 maka upgrade berikutnya untuk versi mayor adalah 3.0.0. Tingkatkan nilai X ketika
- Y adalah singkatan dari versi Minor. Ini digunakan untuk merilis fungsionalitas baru dalam sistem. Ketika Anda meningkatkan versi minor, Anda menambahnya satu tetapi Anda harus mengatur ulang versi patch ke nol. Jika versi saat ini adalah 2.6.9 maka upgrade berikutnya untuk versi minor adalah 2.7.0. Tingkatkan nilai Y ketika mengimplementasikan fitur baru yang kompatibel dengan versi sebelumnya.
- Z adalah singkatan dari Versi Patch: Versi patch digunakan untuk perbaikan bug. Tidak ada perubahan fungsionalitas pada peningkatan versi patch. Jika versi saat ini adalah 2.6.9 maka versi berikutnya untuk peningkatan patch adalah 2.6.10. Tidak ada batasan untuk angka-angka ini. Tingkatkan nilai Z saat memperbaiki bug

![contoh SemVer](https://camo.githubusercontent.com/b4a391552ece4a357eba4765a093199dfed76c0a924918bb71939e1510de39d2/68747470733a2f2f6d656469612e6765656b73666f726765656b732e6f72672f77702d636f6e74656e742f75706c6f6164732f32303230313032313031303135372f53656d616e74696356657273696f6e696e672e706e67)

### Catatan

- Versi pertama dimulai pada 0.1.0 dan bukan pada 0.0.1, karena tidak ada perbaikan bug yang dilakukan, kami memulai dengan serangkaian fitur sebagai draf pertama proyek.
- Sebelum 1.0.0 hanyalah Fase Pengembangan, di mana Anda fokus menyelesaikan sesuatu. Tahap ini diperuntukkan bagi pengembang dimana sistem sedang dikembangkan.
- SemVer tidak mencakup perpustakaan yang diberi tag 0. * . *. Versi stabil pertama adalah 1.0.0.2

## High Level Arsitektur (ilham)

## Use Case Diagram (naufal)

## Diagram (ER Diagram, User Journey, Sequence Diagram, dll) (disarankan menggunakan mermaid) (ilham)

## Makefile (install, audit, run, test, test with coverage)

Makefile adalah cara mengotomatiskan prosedur *software building* dan tugas kompleks lainnya yang memiliki ketergantungan. Makefile berisi *dependency rules*, *macros* dan *suffix* (atau *implicit*) *rules*.

### Golang

- install
  ```Makefile
  install:
    go mod download
  ```
- audit
  ```Makefile
  audit:
    go list -m -u all
  ```
- run (disesuaikan letak fungsi main)
  ```Makefile
  run:
	go run cmd/http/api.go
  ```
- test 
  ```Makefile
  test:
    go test -v ./...
  ```
- test (with coverage)
  ```Makefile
  test-coverage:
	go test -v -covermode=count ./... -coverprofile=coverage.cov
	go tool cover -func=coverage.cov
  ```

### Java

### Node.js

## Badge

Badge ini bersifat tidak wajib. Memiliki bagian ini dapat membantu link ke tools penting dan juga menunjukkan beberapa statistik sederhana tentang project seperti jumlah form, kontributor, open issues, dll.

![badge](https://www.freecodecamp.org/news/content/images/2021/11/check.png)