//Car Rental Management System
#include<iostream>
#include<windows.h>
#include<fstream>
using namespace std;



struct car{
	
	
	
	int id;
	string name;
	string model;
	string color;
	int rent;
	
	int add(int i);
	int delet();
	int update();
	int search();
	int view(int i);

};

car c[10];

int car::add(int i){
	
	cout<<"Enter car detail"<<endl;
	cout<<"Enter  car id"<<endl;
	cin>>c[i].id;
	cout<<"Enter  car name"<<endl;
	cin>>c[i].name;
	cout<<"enter car model"<<endl;
	cin>>c[i].model;
	cout<<"enter color"<<endl;
	cin>>c[i].color;
	cout<<"Enter per day rent of car"<<endl;
	cin>>c[i].rent;
}

int car::view(int i){

	
	cout<<c[i].id<<"\t\t"<<c[i].name<<"\t\t"<<c[i].model<<"\t\t"<<c[i].color<<"\t\t"<<c[i].rent;
}

int car::delet(){
		int n;
		cout<<"Enter the id of car which you want to delete"<<endl;
		cin>>n;		
		for(int i=0;i<=10;i++){	
		if(n==c[i].id)
		{
				
			c[i].id=0;
			c[i].name="";
			c[i].model="";
			c[i].rent=0;
	 
		cout<<"***Delete succsessfuly****"<<endl;}}
			
	}
	
	int car::update(){
		int n;
		cout<<"Enter the id of car which you want to update"<<endl;
		cin>>n;		
		for(int i=0;i<=10;i++){	
		if(n==c[i].id)
		{
			cout<<"Enter  car name"<<endl;
			cin>>c[i].name;
			cout<<"enter car model"<<endl;
			cin>>c[i].model;
			cout<<"enter color"<<endl;
			cin>>c[i].color;
			cout<<"Enter per day rent of car"<<endl;
			cin>>c[i].rent;
	 
		cout<<"***Update succsessfuly****"<<endl;}}
			
	}
	
	int car::search(){
		int n;
		cout<<"Enter the id of car which you want to search"<<endl;
		cin>>n;		
		for(int i=0;i<=10;i++){	
		if(n==c[i].id)
		{
				
			cout<<"Car name"<<endl;
			cout<<c[i].name;
			cout<<"Car model"<<endl;
			cout<<c[i].model;
			cout<<"Car color"<<endl;
			cout<<c[i].color;
			cout<<"per day rent of car"<<endl;
			cout<<c[i].rent;
			
	}
	
	
}
}





int main()
{
	fstream myfile;
	myfile.open("carRentManagmentSystem.txt",ios::out);
	
	string username1,username2,password1,password2,key;
	int choice,chose,count,no;
	
	Sleep(500);
	cout<<"\t\t\t\t                 ______________              "<<endl;
	Sleep(500);
	cout<<"\t\t\t\t                 |             |             "<<endl;
	Sleep(500);
	cout<<"\t\t\t\t                 |             |             "<<endl;
	Sleep(500);
	cout<<"\t\t\t\t                 |             |             "<<endl;
	Sleep(500);
	cout<<"\t\t\t\t_________________|             |___________________"<<endl;
	Sleep(500);
	cout<<"\t\t\t\t|                                                  |"<<endl;
	Sleep(500);
	cout<<"\t\t\t\t|                                                  |"<<endl;
	Sleep(500);
	cout<<"\t\t\t\t|                                                  |"<<endl;
	Sleep(500);
	cout<<"\t\t\t\t|              Welcome to car Rental               |"<<endl;
	Sleep(500);
	cout<<"\t\t\t\t|                Managment System                  |"<<endl;
	Sleep(500);
	cout<<"\t\t\t\t|                                                  |"<<endl;
	Sleep(500);
	cout<<"\t\t\t\t|                                                  |"<<endl;
	Sleep(500);
	cout<<"\t\t\t\t|       ________             ________              |"<<endl;
	Sleep(500);
	cout<<"\t\t\t\t|_______|       |____________|       |_____________|"<<endl;
	Sleep(500);
	cout<<"\t\t\t\t        |       |            |       |       "<<endl;
	Sleep(500);
	cout<<"\t\t\t\t        |       |            |       |       "<<endl;
	Sleep(500);
	cout<<"\t\t\t\t        |_______|            |_______|       "<<endl;
	Sleep(500);
	
	system("color 2f");
	Sleep(200);
	system("color 3f");
	Sleep(200);
	system("color 4f");
	Sleep(200);
	system("color 5f");
	Sleep(200);
	system("color 6f");
	Sleep(200);
	system("color 0f");
	Sleep(200);
	system("color 3B");
	Sleep(200);
	system("color 4A");
	Sleep(200);
	system("color 56");
	Sleep(200);
	system("color 64");
	Sleep(200);
	system("color 0f");
	
	
	
	cout<<"\t\t\t\t\t***CAR RENTAL SYSTEM**"<<endl;
	cout<<"Signin"<<endl;
	cout<<"Enter your Username"<<endl;
	cin>>username1;
	myfile<<"Username: "<<username1;
	cout<<"Enter your password"<<endl;
	cin>>password1;
	myfile<<"Password: "<<password1;
	myfile.close();
	cout<<"Login"<<endl;
	cout<<"Enter your Username"<<endl;
	cin>>username2;
	cout<<"Enter your password"<<endl;
	cin>>password2;
	if(username1==username2 && password1==password2)
	{
		while(1)
		{
		system("cls");
		cout<<"Enter 1 for admin"<<endl;
		cout<<"Enter 2 for costumer"<<endl;
		cout<<"Exit"<<endl;
		cin>>choice;
		
		if(choice==1)
		{
			system("cls");
			cout<<"Menu"<<endl;
			cout<<"1-Add a Car"<<endl;
			cout<<"2-Delete a Car"<<endl;
	       	cout<<"3-Update a Car"<<endl;
	       	cout<<"4-Search a Car"<<endl;
	        cout<<"Enter the number to choose"<<endl;
	        cin>>chose;
	        if(chose==1)
	        {
	        	system("cls");
	        	cout<<"Enter how many cars you want to add";
	        	cin>>no;
	        	for(int i=1;i<=no;i++)
				{
				cout<<"\n\n\t\t\t\t\t*******Add cars*******\n\n";	
	        	c[i].add(i);

	        	cout<<"**************************************";
	        }
			}
			else if(chose==2)
			{
				system("cls");
				cout<<"Enter how many cars you want to delete";
	        	cin>>no;
	        	for(int i=1;i<=no;i++)
				{
				cout<<"\n\n\t\t\t\t\t*******Delete cars*******\n\n";	
	        	c[i].delet();
	        	cout<<"**************************************";
	        }
	        }
	        	
			else if(chose==3)
			{
				system("cls");
				cout<<"Enter how many data you want to update";
	        	cin>>no;
	        	for(int i=1;i<=no;i++)
				{
				cout<<"\n\n\t\t\t\t\t*******Update cars*******\n\n";	
	        	c[i].update();
	        	cout<<"**************************************";
	        }
	        	
			}
			else if(chose==4)
			{
				system("cls");
				cout<<"Enter how many car you want to search";
	        	cin>>no;
	        	for(int i=1;i<=no;i++)
				{
				cout<<"\n\n\t\t\t\t\t*******Update cars*******\n\n";	
	        	c[i].search();
	        	cout<<"**************************************";	
	        }		
		}
	}
		else if(choice==2)
		{
			system("cls");	 
			cout<<"Costumer Menu"<<endl;
			cout<<"1-View Cars"<<endl;
	        cin>>chose;
	        if(chose==1)
	        {
	        	
						cout<<"\n\n\t\t\t\t\t*******view cars*******\n\n";
						cout<<"\nCar id\t\tCar name\t\tCar Model\t\tCar Color\t\tRent per day";
	        	for(int i=0;i<10;i++)
				{
					if(c[i].id!=0)
					{
						c[i].view(i);
					
					}
					
	        	
	        	}
	        	cout<<"\n**************************************\n";
	cout<<"Enter any key for main menu";
	cin>>key;
			}
		
	}
}
	
}

 return 0;
}
