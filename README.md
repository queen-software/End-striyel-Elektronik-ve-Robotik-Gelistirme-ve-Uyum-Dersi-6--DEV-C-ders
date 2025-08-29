# End-striyel-Elektronik-ve-Robotik-Gelistirme-ve-Uyum-Dersi-6--DEV-C++-ders
#include <iostream>
#include <vector>
/* run this program using the console pauser or add your own getch, system("pause") or input loop */
using namespace std;
//DEĞER ÜRETMEYEN PARAMETRE ALMAYAN FONKSİYONLAR
void sayHello(){
	cout<<"Merhabalar bu ilk fonksiyon"<<endl;
	
}

void info(string name){
	cout<<"Merhabalar : "<<name<<endl;
	
	
}

void info_detail(string name ,string surname ,int age){
	
		cout<<"Ad : "<<name<<"Soyad : "<<surname<<"Yas : "<<age<<endl;
}

//kullanıcı ders adı ve üç tane sınav notu girince ortalaması alan fonksiyonu yazınız.
void ders_notu_hesapla(string ders, vector<double> sinavlar){
	double toplam = 0;
	for(double sinav_notu : sinavlar){
		toplam+= sinav_notu;
		
	}
	//sizeof(dizi) :dizinin oyutu byte cinsinden verir.
	//byte cinsindn verildiğinden dolayı ilgili ilk elemanın da byte olarak 
	int sinav_adet = sinavlar.size();
	double average =toplam /sinav_adet;
	
	
	
	cout<<"Dersin Adi: "<<ders<<endl;
	cout<<"Ortalama : "<<average<<endl;
	
	string harf;
	
	if(average >= 50 && average <60){
		harf ="D";
	}else if(average >=60 && average <70){
		harf ="C";
	
		
	}else if(average >=70 && average <80){
		harf ="B";
	}
	else if(average >=80 && average <90){
		harf ="A";
	}
	else if(average >=90 && average <100){
		harf ="S";
	}else if(average>=0 && average < 50){
		harf ="F";
	}else{
		harf= "LÜTFEN SINAV NOTLARİNİ KONTROL EDİNİZ";
	}
	
}

//Paramtere olarka kullanıcı adı,parola ve email alan bir fonk yaz.
//Kullanici Adi : queensoftware Email : quenn@gmail.com Parola : queen_software

void info_bilgi(string username,string email, string password){
	
	cout<<"Username : "<<username<<" E-mail : "<<email<<" Password : "<<password<<endl;
}



int main(int argc, char** argv) {
	// ad soyad yaş
	/*
	cout<<"Ad : "<<"Omer "<<"Soyad : "<<"Dogan "<<"Yas : "<<24<<endl;
	cout<<"Ad : "<<"BUSE "<<"Soyad : "<<"Dogan "<<"Yas : "<<27<<endl;*/
/*	
	sayHello();
	info("Buse");
	info("Uzay");
	info("Sanal");
	info("Evren");
	info_detail("Omer","Dogan",24);
	info_bilgi("queensoftware","quenn@gmail.com","queen_software");
	
	
	 */
	 string lesson;
	 int sinav_sayisi =0;
	 cout<<"Lutfen ders adını giriniz :"<<endl;
	cin>>lesson;
	
	cout<<lesson<<" Dersinin kac tane sinavi var:"<<endl;
	cin>>sinav_sayisi;
	
	vector<double> exams = {};
	for(int i =1; i<= sinav_sayisi;i++){
		
		double note;
		cout<<lesson<<"Dersinin"<<i<<" . sinav notu : "<<endl;
		cin>>note;
		exams.push_back(note);
		
		
	} 
	ders_notu_hesapla(lesson,exams);
	
}


------------------------------------------------------------------

#include <iostream>
#include <cmath>
#include <ctime>
/* run this program using the console pauser or add your own getch, system("pause") or input loop */
using namespace std;

void merhaba(){
	cout<<"Merhabalar"<<endl;
}

//
int toplam(int a ,int b){
	
	return a+b;
	
}
string full_name(string name, string surname){
	
	return name +surname;
}
int main(int argc, char** argv) {
	
/*	int result = toplam(3,45);
	cout<<result<<endl;
	string ful =full_name("queen","software");
	cout<<ful<<endl; 
	
	*/
	
	//Karakök alan fonksiyon
	cout<<"25'in karakoku :'"<<sqrt(25)<<endl;
	int a = 6;
	int b =3;
	int kuvvet =pow(a,b);
	cout<<"6'nin 3. kuvveti : "<<kuvvet<<endl;
	cout<<"-156 nin mutlak degeri : "<<abs(-156)<<endl;
	
	
	string s ="Merhabalar";
	cout<<"s metninin kac harflidir ? :" <<s.length()<<endl;	
	
	time_t now = time(0);
	char* dt = ctime(&now);
	cout<<dt<<endl;
	
}


python için colab
