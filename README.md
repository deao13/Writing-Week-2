**Senin, 26 September 2022**
### JS Dasar - Scope, JS Dasar - Function


#### JS Dasar - Scope
Scope adalah konsep dalam flow data variable, yang dimana menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.
- BLOCKS
    ode yang berada di dalam curly braces atau kurung kurawal ({}). Penerapannya pada seperti conditional, function, dan looping
- GLOBAL SCOPE
    Variabel yang kita buat dapat diakses dimanapun dalam suatu file, suatu variabel tersebut harus di dideklarasikan di luar blocks
    let myName = ‘Dea’;
    function greeting(){
	return myName;
    }
    console.log(myName);
- LOCAL SCOPE
    Mendeklarasikan suatu variabel didalam blocks seperti function, conditional, dan looping, sehingga variabel hanya bisa diakses didalam blocks dan tidak bisa diakses dari luar blocks
    function greeting() {
    let myName = ‘Dea’;
    return myName;
    }
    console.log(greeting())
    console.log(myName);



#### JS Dasar - Function
Sub-program yang bisa digunakan kembali baik di dalam program itu sendiri, maupun di program yang lain. Function di dalam Javascript adalah sebuah objek, karena memiliki properti dan juga method.
- Membuat Function
    function greeting() {
    return “Hello World”;
    };
- Memanggil Function
greeting() //memanggil nama fungsi
console.log(greeting());

- Parameter dan Argumen
1. Parameter Function
    Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas. Saat membuat function kita harus mengetahui terlebih dahulu data yang diperlukan.
        function penambahan(a,b) {
    return a + b;
    }
2. Argumen Function
    Argumen adalah nilai yang digunakan saat memanggil function. Jumlah argumen harus sama seperti jumlah parameter.
    function pengurangan(a,b) {
    return a - b;
    }
    console.log(pengurangan(6, 4));

- Default Parameter
    Memberikan nilai awal/default pada parameter function, yang digunakan untuk menjaga function agar tidak error saat dipanggil tanpa argumen
    function greetOnWebsite(name = “Stranger”){
    return “Hello” + name;
    }
    console.log(greetOnWebsite(“Dafiq”));
    console.log(greetOnWebsite());

- Function Helper
    Menggunakan function yang sudah dibuat pada function lain. 
    function multiplyByNineFifths(number){
    return number * (9/5);
    };
    function getFahrenheit(celcius){
	return multiplyByNineFifths(celcius) + 32;
    };
    getFahrenheit(15);

- Arrow Function
    Cara lain untuk menuliskan sebuah function, dan ini adalah termasuk fitur baru pada ES6(Javascript Version)
    const greeting = () => {
    return “Hello World”;
    };
    const penambahan = (a,b) => {
    return a + b;
    };
- Short Syntax Function
1. Zero Parameters
const functionName = () => {};
2. One Parameters
const functionName = paramOne => {};
3. Two or more parameters
const functionName = (paramOne, paramTwo) => {};
4. Single-Line Block
const sumNumbers = number => number + number;
5. Multi-Line Block
const sumNumbers = number => {
const sum = number + number;
return sum; //return statement
}







** Selasa, 27 September 2022
### Tipe Data

#### Tipe Data
Tipe data merupakan sesuatu yang penting untuk diketahui saat belajar bahasa pemrograman.
Dengan mengetahui tipe data kita akan menulis program sesuai dengan aturan pengelompokan data yang telah ditetapkan pada sebuah bahasa pemrograman. 

JavaScript adalah bahasa dinamis dengan tipe dinamis. Variabel dalam JavaScript tidak secara langsung terkait dengan jenis nilai tertentu, dan variabel apa pun dapat diberi (dan ditetapkan ulang) nilai dari semua jenis :
let foo = 42; // foo is now a number
foo = "bar"; // foo is now a string
foo = true; // foo is now a boolean

JavaScript juga merupakan bahasa yang diketik dengan lemah, yang berarti memungkinkan konversi tipe implisit saat operasi melibatkan tipe yang tidak cocok, alih-alih melempar kesalahan tipe.
const foo = 42; // foo is a number
const result = foo + "1"; // JavaScript coerces foo to a string, so it can be concatenated with the other operand
console.log(result); // 421

- Tipe Data Primitive
1. Boolean type
Memiliki 2 bentuk nilai yaitu true dan false
2. Null type
Di JavaScript null merupakan sesuatu yang telah dipilih sebagai variabel null dari script program yang dibuat.
3. Undefined type
Sebuah variabel jika tidak ditetapkan nilainya maka data variabel tersebut akan disebut sebagai undefined.
4. Number type
salah satu tipe data yang dapat digunakan untuk menunjukan nilai numerik di JavaScript. Number di JavaScript dapat berupa nilai positif dan negatif.
5. BigInt type
BigInt memiliki kapasitas penyimpanan bilangan numerik lebih besar dari number.
6. String type
String digunakan menyimpan karakter berupa text.
7. Symbol type
Simbol di JavaScript digunakan untuk sesuatu yang bernilai unik dan tidak dapat diubah (immutable). Dalam pembuatannya Symbol terdiri atas nama simbol dan description.

- Tipe Data Object
Tipe data object terdiri atas kumpulan properti. properti adalah diidentifikasikan sebagai sebuah key yang memiliki nilai. nilai dari key tersebut dapat dalam bentuk number, text atau symbol.




#### String
String Javascript adalah tipe data primitif yang ada dalam high-level programming language. Objek String digunakan untuk mewakili dan memanipulasi urutan karakter. String berguna untuk menyimpan data yang dapat direpresentasikan dalam bentuk teks. Beberapa operasi yang paling sering digunakan pada string adalah memeriksa panjangnya, membangun dan menggabungkannya menggunakan operator string + dan +=, memeriksa keberadaan atau lokasi substring dengan metode indexOf(), atau mengekstrak substring dengan substring () metode.

`const string1 = "A string primitive";`
`const string2 = 'Also a string primitive';`
`const string3 = ``Yet another string primitive`


- Akses Karakter
Ada dua cara untuk mengakses karakter individu dalam sebuah string. Yang pertama adalah metode charAt() :
1. `'cat'.charAt(1) // memberikan nilai "a"`
2. `'cat'[1] // memberikan nilai "a"`
   
- Membandingkan String
Dalam C, fungsi strcmp() digunakan untuk membandingkan string. Dalam JavaScript, Anda cukup menggunakan operator kurang dari dan lebih besar dari:

`const a = 'a';`
`const b = 'b';`
`jika (a < b) { // benar`
   console.log(`${a} kurang dari ${b}`)
} `else jika (a > b) {`
    console.log(`${a} lebih besar dari ${b}`)
} `if else{`
   console.log(`${a} dan ${b} sama.`)
}`

- String Primitive dan String Object
String literal (dilambangkan dengan tanda kutip ganda atau tunggal) dan string yang dikembalikan dari panggilan String dalam konteks non-konstruktor (yaitu, dipanggil tanpa menggunakan kata kunci baru) adalah string primitif. Dalam konteks di mana metode akan dipanggil pada string primitif atau pencarian properti terjadi, JavaScript akan secara otomatis membungkus string primitif dan memanggil metode atau melakukan pencarian properti pada objek pembungkus sebagai gantinya.

`const strPrim = "foo"; // Sebuah literal adalah sebuah string primitif`
`const strPrim2 = String(1); // Dipaksa ke dalam string primitif "1"`
`const strPrim3 = String(benar); // Dipaksa ke dalam string primitif "benar"`
`const strObj = String baru(strPrim); // String dengan yang baru mengembalikan objek pembungkus string.`

`console.log(tipe strPrim); // Log "string"`
`console.log(tipe strPrim2); // Log "string"`
`console.log(tipe strPrim3); // Log "string"`
`console.log(tipe strObj); // Mencatat "objek"`


- Construktor
String()
Membuat objek String baru. Ia melakukan konversi tipe ketika dipanggil sebagai fungsi, bukan sebagai konstruktor, yang biasanya lebih berguna.


#### Number
Number adalah objek pembungkus primitif yang digunakan untuk mewakili dan memanipulasi angka seperti 37 atau -9,25. Konstruktor Number berisi konstanta dan metode untuk bekerja dengan angka. Nilai dari tipe lain dapat dikonversi ke angka menggunakan fungsi Number(). Angka paling sering dinyatakan dalam bentuk literal seperti 0b101, 0o13, 0x0A. Tata bahasa leksikal berisi referensi yang lebih rinci.
contoh : 
`123; // seratus dua puluh tiga`
`123.0; // sama`
`123 === 123.0; // TRUE`

- Pengkodean Angka
Jenis Nomor JavaScript adalah nilai IEEE 754 format biner 64-bit presisi ganda, seperti ganda di Java atau C#. Ini berarti dapat mewakili nilai pecahan, tetapi ada beberapa batasan untuk besaran dan presisi angka yang disimpan. Secara singkat, nomor presisi ganda IEEE 754 menggunakan 64 bit untuk mewakili 3 bagian:

1 bit untuk tanda (positif atau negatif)
11 bit untuk eksponen (-1022 hingga 1023)
52 bit untuk mantissa (mewakili angka antara 0 dan 1)

- Number coercion
Banyak operasi built-in yang mengharapkan angka pertama-tama memaksakan argumen mereka ke angka (yang sebagian besar mengapa objek Number berperilaku mirip dengan angka primitif). Operasi tersebut dapat diringkas sebagai berikut:

Number dikembalikan apa adanya.
Undefined berubah menjadi NaN.
Null berubah menjadi 0.
True berubah menjadi 1; False berubah menjadi 0.

- Constructor
Number()
Membuat nilai Angka baru.

Ketika Number dipanggil sebagai konstruktor (dengan yang baru), itu menciptakan objek Number, yang bukan primitif. Misalnya, ketik Nomor baru(42) === "objek", dan Nomor baru(42) !== 42 (meskipun Nomor baru(42) == 42).






#### Math
Math adalah objek bawaan yang memiliki properti dan metode untuk konstanta dan fungsi matematika. Ini bukan objek fungsi. Matematika bekerja dengan tipe Number. Ini tidak bekerja dengan BigInt. Tidak seperti banyak objek global lainnya, Math bukanlah sebuah konstruktor. Semua properti dan metode Math bersifat statis. Anda merujuk ke pi konstan sebagai Math.PI dan Anda memanggil fungsi sinus sebagai Math.sin(x), di mana x adalah argumen metode. Konstanta didefinisikan dengan presisi penuh bilangan real dalam JavaScript.

- Static Properties
1. Math.E
Konstanta Euler dan basis logaritma natural; sekitar 2,718.
2. Math.LN2
Logaritma natural dari 2; sekitar 0,693.
3. Math.LN10
Logaritma natural 10; sekitar 2,303.

- Static Methods
1. Math.abs()
Mengembalikan nilai absolut dari x.
2. Math.acos()
Mengembalikan arccosinus dari x.
3. Math.acosh()
Mengembalikan arccosinus hiperbolik dari x.
4. Math.max()
Mengembalikan bilangan terbesar dari nol atau lebih.
5. Math.min()
Mengembalikan angka terkecil dari nol atau lebih.
6. Math.pow()
Mengembalikan basis x ke pangkat eksponen y (yaitu, xy).





#### Primitive & NonPrimitive
- Primitive
    1. Numbers
    2. String
    3. Booleans
    4. Undefined
    5. Null
	contoh : 
    let a = 5
    let b = a
    console.log(a) // 5
    console.log(b) // 5
    console.log(a === b) // true
    a = 10
    console.log(a) // 10
    console.log(b) // 5
    console.log(a === b) // false

Ini karena Primitif disimpan berdasarkan nilai. Artinya, setiap kali kita memutuskan untuk mendeklarasikan variabel baru menggunakan tipe data primitif, kita membuat alamat baru di memori untuk nilai tersebut.


- Non Primitive
    1. Objects
    2. Array
    3. Function
	contoh : 
    let a = [10]
    let b = a
    console.log(a === b) // true
    a.push(10)
    console.log(a) // [10, 10]
    console.log(a === b) // true
	
Alasan untuk ini adalah karena Non-Primitif (Objek) disimpan dengan referensi. Pada dasarnya, kami selalu menyimpan pointer ke alamat saat bekerja dengan tipe data Non-Primitif.

KESIMPULAN : 
Tipe data primitif disimpan berdasarkan nilai. Tipe data non-primitif disimpan dengan referensi. Saat mendeklarasikan variabel, Anda biasanya membuat alamat baru yang potensial.
