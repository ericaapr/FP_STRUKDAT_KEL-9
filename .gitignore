#include <iostream>
#include <stdio.h>
#include <stdlib.h>
#include <iomanip>
#include <string>
#include <conio.h>
#include <cmath>

using namespace std;

struct node
{
    	long long int npm;
	string nama, jenis, status;
	float berat, tinggi, bmi, ideal;
	struct node *next;
}*top = NULL;

void push(long long int input_npm, string input_nama, string input_jenis, float input_berat, float input_tinggi)
{
	string input_status;
    	float meter, rumusbmi, rumusbroca, hasil;
	struct node *temp = new(struct node);
	if(temp==NULL)
	{
		cout << "\nStack Penuh\n";
	}
	temp->npm = input_npm;
	temp->nama = input_nama;
	temp->jenis = input_jenis;
	temp->berat = input_berat;
	temp->tinggi = input_tinggi;

	meter = input_tinggi/100;
	rumusbmi = (input_berat/(meter*meter));
	temp->bmi = rumusbmi;

	if (rumusbmi<18.5)
    	{
        input_status = "Kurus";
    	}
    	else if (rumusbmi<=24.9)
    	{
        input_status = "Normal";
    	}
    	else if (rumusbmi<29.9)
    	{
        input_status = "Overweight";
    	}
    	else
    	{
        input_status = "Obesitas";
   	}
    	temp->status = input_status;

    	if (input_jenis == "L")
    	{
        	rumusbroca= ((input_tinggi-100)-(0.10*(input_tinggi-100)));
        	hasil = rumusbroca;
    	}
    	else
    	{
       		rumusbroca = ((input_tinggi-100)-(0.15*(input_tinggi-100)));
        	hasil = rumusbroca;
    	}
    	temp->ideal = hasil;
    	temp->next = top;
	top = temp;
}

void pop()
{
	if(top==NULL)
	{
		cout << "\nStack Masih Kosong\n";
		system("pause");
		return;
	}
	cout << "\nData Yang Dihapus : \n";
	cout << "====================================================================================================\n";
    	cout << "|     NPM     |     NAMA      | JENIS KELAMIN | BERAT | TINGGI |  BMI  |   STATUS   | BERAT IDEAL  |\n";
    	cout << "====================================================================================================\n";
    	cout << "| " << setiosflags(ios::left) << setw(12) << top->npm << "|";
    	cout << " " << setiosflags(ios::left) << setw(14) << top->nama << "|";
    	cout << " " << setiosflags(ios::left) << setw(14) << top->jenis << "|";
    	cout << " " << setiosflags(ios::left) << setw(6) << top->berat << "|";
    	cout << " " << setiosflags(ios::left) << setw(7) << top->tinggi << "|";
    	cout << " " << setiosflags(ios::left) << setw(6) << setprecision(3) << top->bmi << "|";
    	cout << " " << setiosflags(ios::left) << setw(11) << top->status << "|";
    	cout << " " << setiosflags(ios::left) << setw(13) << top->ideal << "|";
    	cout << "\n====================================================================================================\n";
	top = top->next;
    	cout << "\nTekan Enter Untuk Melanjutkan";
	getch();
}

void top_stack()
{
	if(top==NULL)
	{
		cout << "\nStack Masih Kosong\n";
		system("pause");
		return;
	}
	cout << "\nData Yang Berada Di Top : \n";
	cout << "====================================================================================================\n";
    	cout << "|     NPM     |     NAMA      | JENIS KELAMIN | BERAT | TINGGI |  BMI  |   STATUS   | BERAT IDEAL  |\n";
    	cout << "====================================================================================================\n";
    	cout << "| " << setiosflags(ios::left) << setw(12) << top->npm << "|";
    	cout << " " << setiosflags(ios::left) << setw(14) << top->nama << "|";
    	cout << " " << setiosflags(ios::left) << setw(14) << top->jenis << "|";
    	cout << " " << setiosflags(ios::left) << setw(6) << top->berat << "|";
    	cout << " " << setiosflags(ios::left) << setw(7) << top->tinggi << "|";
    	cout << " " << setiosflags(ios::left) << setw(6) << setprecision(3) << top->bmi << "|";
    	cout << " " << setiosflags(ios::left) << setw(11) << top->status << "|";
    	cout << " " << setiosflags(ios::left) << setw(13) << top->ideal << "|";
    	cout << "\n====================================================================================================\n";
    	cout << "\nTekan Enter Untuk Melanjutkan\n";
	getch();
}

void display_stack()
{
	if(top==NULL)
	{
		cout << "\nStack Masih Kosong\n";
		system("pause");
		return;
	}
	cout << endl;
    cout << "\nData Berat Badan Mahasiswa Informatika : \n";
	cout << "====================================================================================================\n";
    cout << "|     NPM     |     NAMA      | JENIS KELAMIN | BERAT | TINGGI |  BMI  |   STATUS   | BERAT IDEAL  |\n";
    cout << "====================================================================================================\n";

	struct node *temp=top;
	while(temp!=NULL)
	{

		cout << "| " << setiosflags(ios::left) << setw(12) << temp->npm << "|";
		cout << " " << setiosflags(ios::left) << setw(14) << temp->nama << "|";
		cout << " " << setiosflags(ios::left) << setw(14) << temp->jenis << "|";
		cout << " " << setiosflags(ios::left) << setw(6) << temp->berat << "|";
		cout << " " << setiosflags(ios::left) << setw(7) << temp->tinggi << "|";
		cout << " " << setiosflags(ios::left) << setw(6) << setprecision(3) << temp->bmi << "|";
		cout << " " << setiosflags(ios::left) << setw(11) << temp->status << "|";
		cout << " " << setiosflags(ios::left) << setw(13) << temp->ideal << "|";
		temp=temp->next;
		cout << "\n====================================================================================================\n";
	}
    cout << "\nTekan Enter Untuk Melanjutkan\n";
	getch();
}

int main()
{
	int pilih;
	float input_berat, input_tinggi;
	long long int input_npm;
	string input_nama, input_jenis;

	while(1)
	{
	    system("cls");
	    cout << "|===================================|\n";
		cout << "|======= PROGRAM BERAT BADAN =======|\n";
        cout << "|====== MAHASISWA INFORMATIKA ======|\n";
		cout << "|===================================|\n";
		cout << "| [1] Input Data                    |\n";
		cout << "| [2] Hapus Data Top                |\n";
		cout << "| [3] Tampilan Data Top             |\n";
		cout << "| [4] Tampilan Semua Data           |\n";
		cout << "| [5] Exit                          |\n";
		cout << "|===================================|\n";
		cout << "Masukkan Pilihan Anda : ";
		cin >> pilih;

		switch(pilih)
		{
			case(1):
				cout << "Masukkan NPM          : ";
				cin >> input_npm;
				cout << "Masukkan Nama Depan   : ";
				cin >> input_nama;
				cout << "Masukkan Jenis Kelamin (L/P) : ";
				cin >> input_jenis;
				cout << "Masukkan Berat Badan   (KG)  : ";
				cin >> input_berat;
				cout << "Masukkan Tinggi Badan  (CM)  : ";
				cin >> input_tinggi;
				push(input_npm,input_nama,input_jenis,input_berat,input_tinggi);
                system("pause");
				break;
			case(2):
				pop();
				break;
			case(3):
				top_stack();
				break;
			case(4):
				display_stack();
				break;
			case(5):
				exit(0);
				break;
			default:
				cout << "\nPilihan Anda Salah";
				continue;
		}
	}
	return 0;
}
