#include<iostream>
#include<ctime>
#include<cstdlib>
using namespace std;
struct cl_patient
{
	char first_name[20];
	char last_name[20];
	char patient_add[200];
    char patient_phonenumber[10];
    int patient_age;
    char patient_gender[8];
    char patient_bloodtype[5];
    int patient_id;
    char patient_symptom[500];
    char patient_diagnosis[500];
    char patient_medicine[500];
	struct cl_patient *next;
	bool diagnose_patient;
};
struct cl_patient *first_patient,*last_patient;
bool checking=true;
int array[20]={0},v=0;
bool check_id(int ch)
{
  	    for(int y=0;y<v;y++)
  	    {
  	    	if(ch==array[y])
  	    	{
  	    		return true;
			}
		}
		return false;
};
class Doctor
{
	public:
	  void add()
	  {

	  	cl_patient *pat;
	  	pat=new cl_patient;
	  	pat->diagnose_patient=false;
	  	cout<<"Enter Patient ID"<<endl;
	  	cin>>pat->patient_id;
		bool id_present = false;
		for(int i = 0 ; i < v ; i++) {
			if(array[i] == pat->patient_id) {
				id_present = true;
				break;
			}
		}
		if(id_present) {
			cout << "ID already exists" << endl;
			free(pat);
			return;
		}
	  	cout<<"Enter Patient First Name"<<endl;
	  	cin>>pat->first_name;
	  	cout<<"Enter Patient Last name"<<endl;
	  	cin>>pat->last_name;
	  	cout<<"Enter Patient Age"<<endl;
	  	cin>>pat->patient_age;
	  	cout<<"Enter Patient Gender"<<endl;
	  	cin>>pat->patient_gender;
	  	cout<<"Enter Patient Blood Group"<<endl;
	  	cin>>pat->patient_bloodtype;
	  	cout<<"Enter Patient Contact "<<endl;
	  	cin>>pat->patient_phonenumber;
	  	cout<<"Enter Patient Address"<<endl;
		char ch;
		cin >> ch;
	  	cin.getline(pat->patient_add,1000);
	  	pat->next=NULL;
	  	array[v]=pat->patient_id;
	  	v++;
	  	if(checking)
	{
	    first_patient=pat;
	    last_patient=pat;
	    checking=false;
	}
	else
	{
		last_patient->next=pat;
		last_patient=pat;
	}
	cout << "Patient Added " << endl;

  }
  void show()
  {
  	    int z;
  	    cl_patient *cur=NULL;
  	    cur=first_patient;
  	    int patient_id;
 	    cout<<"Enter Patient ID"<<endl;
  	    cin>>patient_id;
		if(check_id(patient_id))
		{
  	    while(cur->patient_id!=patient_id)
  	    {
  	    	cur=cur->next;
  	   	  }

  	 	cout<<"Patient First Name"<<endl;
	  	cout<<cur->first_name<<endl;
	  	cout<<"Patient Last Name"<<endl;
	  	cout<<cur->last_name<<endl;
	  	cout<<"Patient ID"<<endl;
	  	cout<<cur->patient_id<<endl;
	  	cout<<"Patient Age"<<endl;
	  	cout<<cur->patient_age<<endl;
	  	cout<<"Patient Gender"<<endl;
	  	cout<<cur->patient_gender<<endl;
	  	cout<<"Patient Blood Type"<<endl;
	  	cout<<cur->patient_bloodtype<<endl;
	  	cout<<"Patient Contact "<<endl;
	  	cout<<cur->patient_phonenumber<<endl;
	  	cout<<"Patient Address"<<endl;
	    cout<<cur->patient_add<<endl;
	    cout<<"*********************************"<<endl;
	    if(cur->diagnose_patient){
	    cout<<"Symptoms"<<endl;
	    cout<<cur->patient_symptom<<endl;
	    cout<<"Diagnosis"<<endl;
	    cout<<cur->patient_diagnosis<<endl;
	    cout<<"Medicines"<<endl;
	    cout<<cur->patient_medicine<<endl;
	   }}
	   else
	   {
	   	cout<<"ID not present"<<endl;
	   }
}
  void diagnosis()
  {
  	int z;
    cl_patient *pat=NULL;
    pat=first_patient;
  	int patient_id;
  	cout<<"Enter Patient ID"<<endl;
  	cin>>patient_id;
	if(check_id(patient_id)){
		while(pat->patient_id!= patient_id)
	  	{
	  		pat=pat->next;
		}
		pat->diagnose_patient=true;
		cout<<"Enter Symptoms"<<endl;
		cin>>pat->patient_symptom;
		cout<<"Enter Diagnosis"<<endl;
		cin>>pat->patient_diagnosis;
		cout<<"Enter Medicines"<<endl;
		cin>>pat->patient_medicine;
		cout << "Patient Diagnosed " << endl;
	}

	else
		cout<<"ID is not Registered\n";

	}
void update_menu()
{
	    cout<<"Enter 1 Patient First Name"<<endl;
	  	cout<<"Enter 2 Patient Last Name"<<endl;
	  	cout<<"Enter 3 Patient ID"<<endl;
	  	cout<<"Enter 4 Patient Age"<<endl;
	  	cout<<"Enter 5 Patient Gender"<<endl;
	  	cout<<"Enter 6 Patient Blood Type"<<endl;
	  	cout<<"Enter 7 Patient Phone Number "<<endl;
      	cout<<"Enter 8 Patient Address"<<endl;
	    cout<<"*********************************"<<endl;
	    cout<<"Enter 9 Symptoms"<<endl;
	    cout<<"Enter 10 Diagnosis"<<endl;
	    cout<<"Enter 11 Medicines"<<endl;
}
void update_data(){
    cl_patient *cur=NULL;
	cur=first_patient;
	int patient_id,change;
	cout<<"Enter ID"<<endl;
	cin>>patient_id;
	if(check_id(patient_id)){
		while(cur->patient_id!=patient_id)
  	    {
  	    	cur=cur->next;
  		}
  		update_menu();
  		cout<<"Choose Number"<<endl;
  		cin>>change;
  		if(change==1){
  			cout<<"Enter First Name"<<endl;
  			cin>>cur->first_name;
		  }
		else if(change==2){
			cout<<"Enter Second Name"<<endl;
			cin>>cur->last_name;
		}
		else if(change==3){
			cout<<"Enter ID"<<endl;
			cin>>cur->patient_id;
		}
  		else if(change==4){
  			cout<<"Enter Age"<<endl;
  			cin>>cur->patient_age;
		  }
		else if(change==5){
			cout<<"Enter Gender"<<endl;
			cin>>cur->patient_gender;
		}
		else if(change==6){
			cout<<"Enter Blood Type"<<endl;
			cin>>cur->patient_bloodtype;
		}
		else if(change==7){
			cout<<"Enter Phone Number"<<endl;
			cin>>cur->patient_phonenumber;
		}
		else if(change==8){
			cout<<"Enter Address"<<endl;
			cin>>cur->patient_add;
		}
		else if(change==9){
			cout<<"Enter Symptoms"<<endl;
			cin>>cur->patient_symptom;
		}
		else if(change==10){
	    cout<<"Enter Diagnosis"<<endl;
	    cin>>cur->patient_diagnosis;
	    }
	    else if(change==11){
	    cout<<"Enter Medicines"<<endl;
	    cin>>cur->patient_medicine;
		}
		cout << "Patient Attribute Updated " << endl;
   }
   else
     cout<<"ID not present"<<endl;
}
};

void display_menu()
{
	cout<<"|=================================|"<<endl;
	cout<<"|[1] Add New Patient Record       |"<<endl;
	cout<<"|[2] Add Patient Prescription     |"<<endl;
	cout<<"|[3] Full History of the Patient  |"<<endl;
	cout<<"|[4] Update Patient Record        |"<<endl;
	cout<<"||5] Exit                         |"<<endl;
    cout<<"|=================================|"<<endl;
	cout<<"Enter the number you want to Choose:"<<endl;
}
void menu()
{
	cout<<"press 1 To Doctor Menu"<<endl;
	cout<<"press 2 To Patients Menu"<<endl;
	cout<<"press 3 To Pharmacist Menu"<<endl;
}
int main()
{
	Doctor m;
	int v=0;
	do{
	display_menu();
	cin>>v;
	if(v==1)
	m.add();
	else if(v==2)
	m.diagnosis();
	else if(v==3)
	m.show();
	else if(v==4)
	m.update_data();
	else if(v == 5)
		break;
	else
	cout<< "Enter Valid Choice" << endl;
	}while(1);
	return 0;
}
