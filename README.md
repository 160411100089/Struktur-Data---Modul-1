# Struktur-Data---Modul-1
Review Algoritma Pemrograman
---------------------------------------------------------------------------------------------------------------------------------
Berikut pengulangan kembali materi-materi dasar yang terdapat pada mata kuliah Algoritma Pemrograman :
1.	Variabel dan Tipe Data
2.	Jenis Algoritma
3.	String-List-Tuple
4.	Dictionaries
5.	Function
6.	Module



A. Variabel dan Tipe Data

Variabel merupakan simbol yang digunakan untuk menyimpan sebuah nilai. 
Sedangkan tipe data adalah jenis nilai yang akan disimpan. Macam tipe data dasar yang dikenal dalam bahasa pemrograman Python, antara lain:

•	Integer,
Jenis tipe data integer digunakan jika ingin menyimpan informasi angka (bilangan bulat) dalam variabel, tetapi bukan bilangan pecahan.

•	Float,
Jika Anda bermaksud menyimpan informasi angka dengan format pecahan atau angka decimal.

•	String, 
Tipe data string ini memungkinkan variabel menyimpan informasi untaian karakter, seperti kata atau kalimat.

•	Boolean,
Jenis tipe data ini biasanya digunakan hanya untuk merepresentasikan dua kondisi, yakni nilai TRUE dan FALSE.


*Contoh code inisialisasi dan informasi type data dengan menggunakan syntax type untuk masing-masing tipe data


•	Tipe Data Integer

	num = 100
	type(num)

•	Tipe Data Float

	realNum = 0.9999
	type(realNum)

•	Tipe Data String

	data="Hello World"
	type(data)

•	Tipe Data Boolean

	boolDat=True
	type(boolDat)
	
	
#Operasi Data

Setiap variabel dapat dioperasikan dengan menggunakan operasi tertentu  tetapi operasi dapat dilakukan hanya pada variabelvariabel yang memiliki tipe data yang sama.

*contoh code untuk operasi antara variabel dengan tipe data yang sama

	#Operasi antara variabel bertipe integer
	a=10
	b=5
	hasil=a+b
	print('hasil=',hasil)

	#Operasi antara variabel bertipe float
	a=5.5
	b=1.2
	hasil=a+b
	print('hasil=',hasil)

	#Operasi antara variabel bertipe string
	a='struktur'
	b='data'
	hasil=a+' '+b
	print('hasil=',hasil)

*contoh code untuk operasi antara variabel dengan tipe data yang tidak sama

	#Operasi antara variabel bertipe integer dengn variabel bertipe float
	a=10
	b=5.5
	hasil=a+b
	print('hasil=',hasil)

	#Operasi antara variabel bertipe integer dengn variabel bertipe string
	a='struktur data'
	b=2
	hasil=a+b
	print('hasil=',hasil)
	
	
B. Algoritma

Terdapat beberapa jenis algoritma dasar, yaitu:

1.	Sequential
2.	Branching
3.	Iteration

•	Sequential,
Algoritma sequential merupakan algoritma yang harus dikerjakan berurutan, mulai dari langkah pertama sampai dengan langkah terakhir. 

•	Branching, 
Algoritma branching atau selection ini merupakan algoritma yang didalamnya terdapat pilihan. Pada algoritma branching terdapat kondisi True atau False. Jika memenuhi kondisi True maka syntax pada percabangan True yang akan diekseskusi, begitu juga sebaliknya. 

•	Iteration, 
Pada Algoritma ini syntax akan dieksekusi secara berulang-ulang selama kondisi bernilai True. Jika kondisi bernilai False maka proses iterasi akan berhenti.

*contoh code untuk masing-masing jenis algoritma
	
	# Algoritma Sequence ‐ Konversi Kurs Mata Dollar ke Rupiah
	dollar=int(input('Jumlah Dollar = '))
	rupiah=dollar*15000
	print(dollar,'$ = Rp.',rupiah)

	# Algoritma Branching ‐ Penentuan jenis bilangan
	num=int(input('Masukkan bilangan = '))
	if num%2==0 :
   		print(num, ' adalah bilangan genap')
	else:
   		print(num, ' adalah bilangan ganjil')

	# Algoritma Iteration ‐ Menampilkan sejumlah n bilangan genap
	num=int(input('Jumlah bilangan genap = '))
	count=1
	i=0
	while count<=num:
   		if i%2==0:
      			print(count,'. ',i)
       			count=count+1
   		i=i+1


C. String, List, dan Tuple

•	String

String merupakan salah satu tipe data dalam suatu bahasa pemrograman yang terdiri dari beberapa character.
Suatu karakter pada string dapat diakses dengan menggunakan syntax namaVariabel[offset], atau jika terdapat beberapa karakter yang harus diakses, dapat menggunakan syntax namaVariabel[offsetAwal:offsetAkhir1]

*contoh inisialisasi variabel dengan tipe data string, dan cara pengaksesan satu dan lebih dari satu karakter

	data="Where is Waldo ?"
	print(data[12]) # Satu karakter
	temp=data[9:14] # lima karakter
	print(temp)

*contoh code untuk proses perubahan nilai melalui operasi assignment, dan melalui method pada string

	#immutable, tidak dapat dirubah melalui assignment operator
	data="Where is Waldo ?"
	data[13]='i'
	print(data)

	#nilai dirubah melalui method 'replace'
	data="Where is Waldo ?"
	data.replace('o','i')
	
•	List

List adalah struktur data yang terdiri dari beberapa elemen atau anggota list dengan berbagai tipe data. Masing-masing elemen dipisahkan oleh koma. Didalam list terdapat index yang menunjukkan urutan elemen dari suatu list. Index dari list ini dimulai dari '0'. Untuk mengakses elemen pada suatu list, dilakukan dengan cara yang sama dengan tipe data string.

*contoh inisialisasi variabel dengan tipe data list, dan cara mengakses satu dan lebih dari satu elemen pada list

	arrData=[1,2,'python',0.8,'numpy']
	print (arrData)
	print(arrData[1])
	print(arrData[1:4])

*contoh code untuk merubah nilai elemen dari suatu list

	arrData=[1,2,'python',0.8,'numpy']
	print(arrData)
	arrData[2]='Java'
	print(arrData)
	
•	Tuple

Tuple, tuple ini terdiri dari beberapa elemen, dan elemen tersebut dapat terdiri dari berbagai tipe. Jika pada list, representasi anggota menggunakan kurung siku atau [a,b,c,...,d], maka pada tuple menggunakan kurung atau (a, b, c, ..., d)

*contoh code untuk inisialisasi tuple dan akses elemen pada tuple

	tupData=(1,2,'python',0.8,'numpy')
	print(tupData)
	print(tupData[2])
	tupData[2]='Java'
	print(tupData)


D. Dictionaries

Dictionary adalah stuktur data yang bentuknya seperti kamus. Ada kata kunci kemudian ada nilaninya. Kata kunci harus unik, sedangkan nilai boleh diisi denga apa saja.

*contoh inisialisasi dictionaries dengan dua cara tersebut
	
	#Cara‐1
	studData={'001':'Ranti','002':'Diana','003':'Budi','004':'Eri'}
	print(studData)

	#Cara‐2
	studentData={}
	studentData['001']='Fatimah'
	studentData['002']='Sofiah'
	studentData['003']='Ahmad'
	studentData['005']='Ali'
	print(studentData)

#Sparse Matrix

Matriks dapat dikatakan sebagai list dua dimensi dimana suatu list berisi list lagi. Untuk merepresentasikan matriks, kita harus menyimpan list dengan panjang yang sama dalam suatu list. Bila list berbeda - beda panjangnya, maka list tersebut disebut sebagai sparse matrix.

*contoh code pembuatan sparse matrix dengan menggunakan dictionary

	Mat = {(0,3): 1, (2, 1): 2, (3, 3): 3}
	print(Mat)
	Mat[0,2]=4 #penambahan data baru
	print(Mat)
	#pengecekan data pada index (ind1,ind2), jika tidak terdapat data, maka return
	value=None,
	#jika terdapat data maka return value=adalah data
	cek=Mat.get((0,1))
	print(cek)
	cek=Mat.get((2,1))
	print('(2,1)=',cek)
	cek=Mat.get((1,3))
	print('(1,3)=',cek)


E. Function

Fungsi adalah bagian dari program yang dapat digunakan ulang. Hal ini bisa dicapai dengan memberi nama pada blok statemen, kemudian nama ini dapat dipanggil di manapun dalam program. Kita telah menggunakan beberapa fungsi builtin seperti range.
Fungsi dalam Python didefinisikan menggunakan kata kunci def. Setelah def ada nama pengenal fungsi diikut dengan parameter yang diapit oleh tanda kurung dan diakhir dingan tanda titik dua :. Baris berikutnya berupa blok fungsi yang akan dijalankan jika fungsi dipanggil.

*contoh sederhana function tanpa parameter, function dengan parameter, dan function dengan return value

	# Function tanpa parameter

	def addNumbers():
    		a=int(input('Bilangan pertama = '))
    		b=int(input('Bilangan kedua = '))
    		print('Hasil = ',a+b)

	#Main program
	addNumbers()#memanggil fungsi addNumbers agar dieksekusi


	# Function dengan parameter

	def addNumbers(a,b):
    		print('Hasil = ',a+b)

	#Main program
	num1=int(input('Bilangan pertama = '))
	num2=int(input('Bilangan kedua = '))
	addNumbers(num1,num2)#memanggil fungsi addNumbers agar dieksekusi


	# Function dengan parameter dan return value
	def addNumbers(a,b):
    		hasil=a+b
    		return hasil

	def cekGenap(num):
    		if num%2==0:
        		return True
    		else:
        		return False

	#Main program
	num1=int(input('Bilangan pertama = '))
	num2=int(input('Bilangan kedua = '))
	result=addNumbers(num1,num2)#memanggil fungsi addNumbers agar dieksekusi
	print('Hasil Penjumlahan= ', result)
	if cekGenap(result):
    		print(result,' adalah Bilangan Genap')
	else:
    		print(result,' adalah Bilangan Ganjil')
		
F. Module

Python juga menyediakan fasilitas untuk membuat Module. Module ini merupakan suatu file yang terdiri dari sebuah atau lebih dari satu function. Dengan mengelompokkan function-function dalam suatu file, akan memudahkan programmer untuk membaca program dan merubah atau memperbaharui program. Modul ini dapat dipanggil di file lain dengan menggunakan keyword import.

*contoh pemanggilan module yang sudah dibuat yaitu checkPrime. Module ini dapat dilihat pada folder code

	import checkPrime

	checkPrime.isPrime(2)


Praktikum Struktur Data - 2019
#Modul 1 – Reviews
--------------------------------------------------------------------------------------------------------------------------------------

1.    Buatlah suatu fungsi untuk menampilkan segitiga, yang memiliki dua buah parameter, yaitu karakter yang akan dicetak, dan tinggi segitiga (jika diperlukan, gunakan formatting string).

Berikut adalah contoh program untuk memanggil fungsi segitiga tersebut, dan hasil output segitiga yang ditampilkan:

Jika tinggi segitiga adalah 7
	
	printTriangle('$', 7)
			$
		       $$$
		      $$$$$$
		     $$$$$$$$
		    $$$$$$$$$$
		   $$$$$$$$$$$$
		  $$$$$$$$$$$$$$
	
Jika tinggi segitiga adalah 12

	printTriangle('*', 12)
				*
		               ***
			      *****
			     *******
			    *********
			   ***********
			  *************
			 ***************
			*****************
		       *******************
		      *********************
		     ***********************
		  
2.    Buatlah suatu modul dengan nama sparseMatrix (matriks yang memiliki banyak elemen ‘nol’) yang berisi beberapa fungsi sebagai berikut :

a)   Fungsi untuk input data dari user.  Input data ini berupa ukuran matriks, dan elemen-elemen pada sparse matrix tersebut , seperti contoh berikut 

	matrix-1					matrix-2
	jumlah baris = 3				jumlah baris = 4
	jumlah kolom = 4				jumlah kolom = 1
	jumlah data = 2					jumlah data = 2
	baris ke?0					baris ke?0
	kolom ke?0					kolom ke?0
	matrix [0,0] = 2				matrix[0,0]
	baris ke?2					baris ke?3
	kolom ke?3					kolom ke?0
	matrix[2,3] = 4					matrix[3,0] = 2

b)   Fungsi untuk menampilkan sparse matrix.  Contoh tampilan sparse matrix dapat dilihat sebagai berikut

	matrix 1=					matrix2=
	| 2 0 0 0 |					| 3 |
	| 0 0 0 0 |					| 0 |
	| 0 0 0 4 |					| 0 |
							| 2 |
							
c)   Fungsi untuk mengalikan dua buah sparse matrix.  Contoh hasil perkalian dua buah sparse matrix, dapat dilihat sebagai berikut :

	matrix 1=
	| 2 0 0 0 |
	| 0 0 0 0 |
	| 0 0 0 4 |
	matrix2=
	| 3 |
	| 0 |
	| 0 |
	| 2 |
	Hasil = 
	| 6 |
	| 0 |
	| 8 |
	
Import modul yang sudah dibuat dalam program utama (main program), dan eksekusi fungsi-fungsi yang sudah dibuat agar dapat meminta input dari user, mengalikan dua buah sparse matrix, dan menampilkan sparse matrix-sparse matrix tersebut  (matriks yang dikalikan dan hasil perkalian)


Jawaban Praktikum
----------------------------------------------------------------------------------------------------

#Program Nomer 1

	string = ""

	x = int(input("Masukkan angka :"))
	bar = x

	while bar >= 0:
	
		kol = bar
		while kol > 0:
			string = string + "   "
			kol = kol - 1
	
		kiri = 1
			while kiri < (x - (bar-1)):
			string = string + " * "
			kiri = kiri + 1		
	
		kanan = 1
		while kanan < kiri -1:
			string = string + " * "
			kanan = kanan + 1	

		string = string + "\n\n"
		bar = bar - 1
	
	print (string)


#Program Nomer 2

	def MatriksInput():
    	baris=input("Banyak Baris Matriks : ")
    	kolom=input("Banyak Kolom Matriks : ")
    	JumlahData=int(input("Jumlah Nilai yang ingin dimasukkan : "))
    	matrixData={}
    
    	for i in range (0,JumlahData):
        	tempbaris=int(input("Baris Koordinat : "))
        	tempkolom=int(input("Kolom Koordinat : "))
        	temp="Masukkan Nilai Matriks Baris ke " + str(tempbaris) + " Kolom ke " + str(tempkolom) + " : "
        	data=input(temp)
        	matrixData[tempbaris,tempkolom]=data
    	return (matrixData,baris,kolom)

	def displayData(matrixData,baris,kolom):
    		matrix={}
    		for i in range(0,int(baris)):
        		temp=''
        	for j in range(0,int(kolom)):
            		if matrixData.get((i+1,j+1),0)==0:
                		temp=temp+' '+str(0)
           	 	else:
               		 	temp=temp+' '+str(matrixData[i+1,j+1])
        	print(temp)

	def multMatrix(a,b,baris,kolom):
    		c={}
   		for i in range(0,int(baris)):
        		for j in range(0, int(kolom)):
            			temp=0
            			for k in range(0,int(baris)):
                			if ((a.get((i+1,k+1),0)!=0) and (b.get((k+1,j+1),0)!=0)):

                    				temp=temp+int(a[i+1,k+1])*int(b[k+1,j+1])

              			  else:
                    			temp=temp+0

            	c[i+1,j+1]=temp
    	return(c)

	print("Matriks A")
	(a,baris_a,kolom_a)=MatriksInput()
	print("_________________________________________________\n")
	print("Matriks B")
	(b,baris_b,kolom_b)=MatriksInput()
	if (kolom_a==baris_b):
   		c=multMatrix(a,b,baris_a,kolom_a)
    		print("_________________________________________________\n \n~ PERKALIAN MATRIKS A & MATRIKS B ~\n")
    		print("Matriks A = ")
    		displayData(a,baris_a,kolom_a)
    		print("Matriks B = ")
    		displayData(b,baris_b,kolom_b)
    		print("Hasil = ")
    		displayData(c,baris_a,kolom_b)
	else:
    		print("_________________________________________________\n \nUkuran Matriks yang Anda Masukkan Tidak Sesuai")
