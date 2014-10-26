tugas-mencari-nilai
===================

tugas mencari nilai


#Tugas Algoritma dan Struktur Data ke 3 
#Program Python TampilkanAngkaDalamRange
awal = raw_input("Masukan Angka Awal : ")
awal = int(awal)
akhir = raw_input("Masukan Angka Akhir : ")
akhir = int(akhir)
angka = raw_input("Masukkan Angka yang di cari : ")
angka = int(angka)
jumlah = 0
kurang = 10
kurang_2 = 0
batas = 0
new_angka = angka*10
new_angka_3 = angka*100
while awal<=akhir:
	new_awal = awal - kurang
	new_angka_2 = awal - kurang_2
	
	if awal<=10:
		if awal==angka:
			print awal
			jumlah = jumlah + 1
			awal=awal+1
		else:
			awal=awal+1	
	else:
		if new_angka==new_angka_2:
			if batas < 10:
				print awal
				awal=awal+1
				jumlah = jumlah + 1
				kurang_2 = kurang_2 + 1
				batas = batas + 1
				
			else:
				batas = 0
				kurang_2 = 0
				new_angka = new_angka+100
				kurang = kurang + 10
				awal = awal+1
		elif angka==new_awal:
			print awal
			kurang = kurang + 10
			awal = awal + 1
			jumlah = jumlah + 1
			new_awal = awal - kurang
		elif new_angka_3 == awal:
			print awal
			awal = awal + 1
			jumlah = jumlah + 1
			new_angka_3=new_angka_3*10
			
		else:
			awal=awal+1
			
else:
	print "Total ada ",jumlah," angka yang mengandung unsur angka ",angka
