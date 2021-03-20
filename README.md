# Windows-Fundamentals-Walkthrough-1
Windows Fundamentals Introduction to Windows module walkthrough 

<!DOCTYPE html  PUBLIC '-//W3C//DTD XHTML 1.0 Transitional//EN'  'http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd'>
<html xmlns="http://www.w3.org/1999/xhtml">
	<head>
	<meta content="text/html; charset=utf-8" http-equiv="Content-Type"/>
	<title>Introductory to Windows</title>
	</head>

	<body>
			<h1>Introduction to Windows</h1>
				<h3>The Windows Operating System</h3>
						<br/>
					<p>Windows 1985'ten beri işletim sistemleri üretmektedir. Windows'un ilk versiyonu 1985'te üretilmiş MS-DOS için oluşturulmuş bir grafik işletim sistemi kabuğudur.</p>
						<br/>
					<p>Daha sonra 1995 yılında Windows 95 çıkmıştır. Bu versiyonla birlikte ilk defa yerleşik internet desteği ve o zamanlar yaygın olarak kullanılan Internet Explorer tarayıcısı gelmiştir. Bu şekilde Microsoft Şirketi günümüze kadar Windows XP'den tut Windows 10'a kadar hem normal hem de kurumsal müşteriler için bir çok işletim sistemi geliştirdi ve satışa sundu.</p>
						<br/>
						<br/>
				<h3>Windows Servers</h3>
						</br>
					<p>Windows sadece işletim sistemleriyle kalmadı aynı zamanda serverlar da geliştirdi. İlk Windows Server 1993 yilinda Windows NT 3.1 olarak satışa sunuldu. Windows Serverlar da günümüze kadar Internet Information Services (IIS), bir çok ağ protokolü, admin görevlerini kolaylastirmak için Administrative Wizards gibi bir çok guncelleme ve yeni teknoloji aldi.</p>
					<br/>
					<p>Windows 2000'in yayinlanmasiyla Microsoft, sistem yöneticilerinin dosya paylaşımı, veri encryption ve VPN kullanımına yarayan <b>"Active Directory"</b> hizmetini Windows Serverlara ekledi. Microsoft kendini güncellemeye devam etti ve Windows Server 2003, Windows Windows Server 2008, Windows Server 2012, Windows Server 2016 ve sürümün son versiyonu olan Windows Server 2019'u yayınladı.</p>
						<br/>
					<p> Microsoft şirketi, çeşitli nedenlerle Windows'un eski versiyonlarina cok buyuk guvenlik acikliklari haricinda (SMBv1 Eternalblue) gibi guvenlik acikliklari disinda guncelleme yapmiyor. Hatta çok yakın zamanda Windows 7'den desteğini çektiğini hatırlayacaksınız.</p>
						<br/>
						<p>Geçmişten günümüze Windows:</p>
						<br/>
					<img src="image.png"/><br/>
						<br/>
						<br/>
				<h3>Get-WmiObject</h3>
					<p>Windows'ta işletim sistemi hakkında bilgi almak için <b>Get-WmiObject</b> cmdlet'ini kullanabiliriz. Bu cmdlet'i WMI classları hakkında bilgi toplamak için kullanırız. Sistem versiyon ve build number (yapı numarası) bilgilerini toplamak için <b>win32_OperatingSystem</b> classını kullanabiliriz.</p>
						<br/>
						<br/>
					<img src="image 2.png"/><br/>
						<br/>
						<br/>
					<p>Kullanabileceğimiz bir diğer class olan <b>Win32_Process</b> classını processes listesini almak için kullanabiliriz</p>
						<br/>
					<p>Sonuç buna benzer upuzun bir liste:</p>
						<br/>
					<img src="image 3.png"/><br/>
						<br/>
						<br/>
						<br/>
					<p>Yine kullanabileceğimiz bir diğer class ise Win32_Bios servislerinin listesini ve onlar hakkında bilgi almak için <b>Win32_Service </b>class'dır</p>
						<br/>
					<p>Sonuç yine bunun gibi uzun bir liste:</p>
						<br/>
					<img src="image 4.png"/><br/>
						<br/>
					<p>GetWmiObejcet cmdlet'i hakkında daha fazla bilgi için<a href="https://ss64.com/ps/get-wmiobject.html"> buraya </a>ve <a href="https://adamtheautomator.com/get-wmiobject/">buraya</a> tıklayabilirsiniz.</p>
						<br/>
						<br/>
				<h2>SORULAR:</h2>
						<br/>
						<br/>
					<p>Hedef makineye bağlanabilmemiz için akademinin VPN ağının içinde bulunmalıyız. İlk olarak bize verilen <b>ovpn</b> dosyasını şekildeki butondan indiriyoruz:</p>
						<br/>
						<br/>
					<img src="image 10.png"/><br/>
						<br/>
					<p>Daha sonra aşağıda gösterilği gibi openvpn ile akademinin VPN'ine bağlanıyoruz:</p>
						<br/>
						<br/>
					<img src="image 7.png"/><br/>
						<br/>
					<p>Makinemizi çalıştırıyoruz:</p>
						<br/>
					<img src="image 9.png"/><br/>
						<br/>
					<p>Daha sonra bize verilen username ve password ile RDP bağlantımızı kuruyoruz:</p>
						<br/>
						<br/>
					<img src="image 8.png"/><br/>
						<br/>
					<img src="image 11.png"/><br/>
						<br/>
					<img src="image 12.png"/><br/>
						<br/>
						<br/>
					<p>Ve bağlantımız geliyor:</p>
						<br/>
					<img src="image 13.png"/><br/>
						<br/>
						<br/>
					<p>Win + S kombinasyonuyla arama çubuğunu açıyoruz ve Powershell'i çalıştırıyoruz</p>
						<br/>
					<img src="image 14.png"/><br/>
						<br/>
						<br/>
				<h3>SORU 1</h3>
						<br/>
						<br/>
					<img src="image 16.png"/><br/>
						<br/>
					<p>İlk soruda hedefimizin Build Number'ını istiyor bu sebeple <b>Get-WmiObject</b> cmdlet'ini <b>win32_OperatingSystem</b> class'ıyla kullanıyoruz.</p>
						<br/>
						<br/>
					<img src="image 15.png"/><br/>
						<br/>
					<p>Ve karşımızda Build Number </p>
						<br/>
						<br/>
				<h3>SORU 2</h3>
						<br/>
						<br/>
					<img src="image 17.png"/>
						<br/>
						<br/>
					<p>Soru bize hedefte hangi Windows NT versiyonun bulunduğunu soruluyor.</p>
						<br/>
					<p>Bu bilgiyi edinmek için systeminfo cmdlet'ini kullanabiliriz</p>
						<br/>
						<br/>
					<img src="image 18.png"/>
						<br/>
						<br/>
					<p>Hedefin Windows 10 kullandığını görebiliyoruz.</p>
						<br/>
						<br/>
				<h3>CEVAPLAR<h3>
						<br/>
						<br/>
					<img src="image 5.png"/>
						<br/>
						<br/>
				<h4>Bu modül için kullanılan cheat sheet:</h4>
						<br/>
						<br/>
					<img src="image 19.png"/>
						<br/>

	</body>
</html>
