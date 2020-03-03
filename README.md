# Github-Portfolio-1
This was a project I created for my final in my prior programming class. Its in C++. It is a bit messy, but I was still rather inexperienced. The goal of the project is to create a class schedule for a student. It outputs up to three files, the title page, and two which give you your schedule. In this project I use commands that require me to include multiple items in the header. Using include Fstream allows me to create output files. String allows strings to be used. 


Here are all of the global variables that I use in my project. The firstname, lastname, major, page, and SSN variables are all later input by the user. The crn's and course variables are used to find your classes later. 
```
string firstname;
string lastname;
string major;
string date;
int stunumber;
int page;
int SSN;
bool yesno="yes";
int crn1=1; //not used in input
int crn2;
int crn3;
int crn4;
int crn5;
int crn6;
int crn7;

string course1;
string course2;
string course3;
string course4;
string course5;
string course6;
```




This part of the code outputs page 1. I use a class to state my name, my school, the semester that I created this project, the class I created it for, and what it is. 

```
 class Cpage1
 {

     public:
      
     string myname="Logan Driver";
     string myschool="Jacksonville State university ";
     string mysemester= "Fall Semster 2019";
     string mycourse= "CS230";

```




This function helps build page 1. I also use fstream to create a new file called "page1.h" that contains all of the information from page 1. 
  
```
   void coutPage1()
   {
       ofstream page1;
   page1.open("page1.h");

     page1 <<line<<endl;
     page1 <<space<<endl;
     page1 <<myschool<<endl;
     page1 <<mysemester<<endl;
     page1 <<mycourse<<endl;
     page1 <<myname<<endl;
     page1<<space<<endl;
     page1 <<line<<endl;
     page1 <<CRE<< endl;
     page1 <<line<<endl;
     page1 <<line<<endl;
 

   page1.close();
       ifstream infile; 
       infile.open("page1.h"); 


   }

};
```



Code for page two. This function creates page two via fstream. I later prompt you for input. Page two contains information relavent to the person who is using this program, rather than me (unlike page one)

```
 void pg2()
 {   
        ofstream page2;
        page2.open("page2.h");


    page2 << "_________Course Enrollment Simulation_________"<< endl;
    page2<< " "<< endl;
    page2 <<"Enter the following information: "<<endl;
    page2 << " "<< endl;
    page2 <<"student number: ";
    page2 << stunumber ;
    page2 <<"    ";


    page2 <<"Last name: ";
    page2 << lastname ;
    page2 <<"    ";

    page2 <<"First name: ";
    page2 << firstname ;
    page2 <<"    ";


    page2 <<"         "<<endl;
    page2 <<" ____________________________________________"<<endl;
    page2 <<" ____________________________________________"<<endl;

  page2.close();

   ifstream infile; 
   infile.open("page2.dat"); 
   infile >> stunumber; 
   infile >> lastname; 


 };
```




  Page 3. What page 3 does is takes the input of each CRN number you enter, and turns it into a class name that is correlated with that CRN and outputs the class name. It also outputs your name, major, and SSN. This code is rather long, as I use if statements for each potential CRN input. Some information is hardcoded, but most of it will be entered via keyboard input from the user. 


```
void pg3()
{   
        ofstream page3;
        page3.open("page3.h");

    page3 <<"_____________________________________________________"<<endl;
    page3 <<"          "<<endl;
    page3 <<"            "<<"Jacksonville State university"<< endl;
    page3 <<"             "<<"Fall Semster 2019"<<endl;
    page3 <<"              "<<"Class Schedule"<<endl;
    page3 << " "<< endl;
    page3 <<"December 6th, 2019";
    page3 << "          ";
    page3 <<"Advisor: Dr Robert A Elliott Sr PhD"<<endl;
    page3 << "          "<<endl;
    page3 <<"SSN: "<<SSN;
    page3 << "     ";
    page3 <<"Name: "<<firstname<<" "<<lastname<< "     ";
    page3 <<"Major: ";
    page3 <<major<<endl;
    page3 << "      ";
    page3 <<"         "<<endl;


    if (crn2==123)
       {
       page3<<"CRS1: LIT 112 001 Literature"<<endl;
       }
        if (crn2==124)
       {
       page3<<"CRS1: CIS 325 124 Computer Programming"<<endl;
       }
        if (crn2==125)
       {
       page3<<"CRS1: CIS 334 125 Web Design"<<endl;
       }
        if (crn2==126)
       {
       page3<<"CRS1: CIS 358 126 Management of security and forensics"<<endl;
       }
        if (crn2==127)
       {
       page3<<"CRS1: EC 235 127 Introduction to E-commerce"<<endl;
       }
        if (crn2==128)
       {
       page3<<"CRS1: SC 550 128 Science"<<endl;
       }
        if (crn2==129)
       {
       page3<<"CRS1: SC 551 129 Science (lab)"<<endl;
       }
        if (crn2==130)
       {
       page3<<"CRS1: PSYCH 150 130 Psychology"<<endl;
       }
        if (crn2==131)
       {
       page3<<"CRS1: FL 901 131 Foreign language"<<endl;
       }
        if (crn2==132)
       {
       page3<<"CRS1: MTH 190 132 Calculus"<<endl;
       } 

        if (crn3==123)
       {
       page3<<"CRS2: LIT 112 123 Literature"<<endl;
       }
        if (crn3==124)
       {
       page3<<"CRS2: CIS 325 124 Computer Programming"<<endl;
       }
        if (crn3==125)
       {
       page3<<"CRS2: CIS 334 125 Web Design"<<endl;
       }
        if (crn3==126)
       {
       page3<<"CRS2: CIS 358 126 Management of security and forensics"<<endl;
       }
        if (crn3==127)
       {
       page3<<"CRS2: EC 235 127 Introduction to E-commerce"<<endl;
       }
        if (crn3==128)
       {
       page3<<"CRS2: SC 550 128 Science"<<endl;
       }
        if (crn3==129)
       {
       page3<<"CRS2: SC 551 129 Science (lab)"<<endl;
       }
        if (crn3==130)
       {
       page3<<"CRS2: PSYCH 150 130 Psychology"<<endl;
       }
        if (crn3==131)
       {
       page3<<"CRS2: FL 901 131 Foreign language"<<endl;
       }
        if (crn3==132)
       {
       page3<<"CRS2: MTH 190 132 Calculus"<<endl;
       } 

     if (crn4==123)
       {
       page3<<"CRS3: LIT 112 123 Literature"<<endl;
       }
        if (crn4==124)
       {
       page3<<"CRS3: CIS 325 124 Computer Programming"<<endl;
       }
        if (crn4==125)
       {
       page3<<"CRS3: CIS 334 125 Web Design"<<endl;
       }
        if (crn4==126)
       {
       page3<<"CRS3: CIS 358 126 Management of security and forensics"<<endl;
       }
        if (crn4==127)
       {
       page3<<"CRS3: EC 235 127 Introduction to E-commerce"<<endl;
       }
        if (crn4==128)
       {
       page3<<"CRS3: SC 550 128 Science"<<endl;
       }
        if (crn4==129)
       {
       page3<<"CRS3: SC 551 129 Science (lab)"<<endl;
       }
        if (crn4==130)
       {
       page3<<"CRS3: PSYCH 150 130 Psychology"<<endl;
       }
        if (crn4==131)
       {
       page3<<"CRS3: FL 901 131 Foreign language"<<endl;
       }
        if (crn4==132)
       {
       page3<<"CRS3: MTH 190 132 Calculus"<<endl;
       } 

     if (crn5==123)
       {
       page3<<"CRS4: LIT 112 123 Literature"<<endl;
       }
        if (crn5==124)
       {
       page3<<"CRS4: CIS 325 124 Computer Programming"<<endl;
       }
        if (crn5==125)
       {
       page3<<"CRS4: CIS 334 125 Web Design"<<endl;
       }
        if (crn5==126)
       {
       page3<<"CRS4: CIS 358 126 Management of security and forensics"<<endl;
       }
        if (crn5==127)
       {
       page3<<"CRS4: EC 235 127 Introduction to E-commerce"<<endl;
       }
        if (crn5==128)
       {
       page3<<"CRS4: SC 550 128 Science"<<endl;
       }
        if (crn5==129)
       {
       page3<<"CRS4: SC 551 129 Science (lab)"<<endl;
       }
        if (crn5==130)
       {
       page3<<"CRS6: PSYCH 150 130 Psychology"<<endl;
       }
        if (crn5==131)
       {
       page3<<"CRS4: FL 901 131 Foreign language"<<endl;
       }
        if (crn5==132)
       {
       page3<<"CRS4: MTH 190 132 Calculus"<<endl;
       } 



    if (crn6==123)
       {
       page3<<"CRS5: LIT 112 123 Literature"<<endl;
       }
        if (crn6==124)
       {
       page3<<"CRS5: CIS 325 124 Computer Programming"<<endl;
       }
        if (crn6==125)
       {
       page3<<"CRS5: CIS 334 125 Web Design"<<endl;
       }
        if (crn6==126)
       {
       page3<<"CRS5: CIS 358 126 Management of security and forensics"<<endl;
       }
        if (crn6==127)
       {
       page3<<"CRS5: EC 235 127 Introduction to E-commerce"<<endl;
       }
        if (crn6==128)
       {
       page3<<"CRS5: SC 550 128 Science"<<endl;
       }
        if (crn6==129)
       {
       page3<<"CRS5: SC 551 129 Science (lab)"<<endl;
       }
        if (crn6==130)
       {
       page3<<"CRS5: PSYCH 150 130 Psychology"<<endl;
       }
        if (crn6==131)
       {
       page3<<"CRS5: FL 901 131 Foreign language"<<endl;
       }
        if (crn6==132)
       {
       page3<<"CRS5: MTH 190 132 Calculus"<<endl;
       } 

    if (crn7==123)
       {
       page3<<"CRS6: LIT 112 123 Literature"<<endl;
       }
        if (crn7==124)
       {
       page3<<"CRS6: CIS 325 124 Computer Programming"<<endl;
       }
        if (crn7==125)
       {
       page3<<"CRS6: CIS 334 125 Web Design"<<endl;
       }
        if (crn7==126)
       {
       page3<<"CRS6: CIS 358 126 Management of security and forensics"<<endl;
       }
        if (crn7==127)
       {
       page3<<"CRS6: EC 235 127 Introduction to E-commerce"<<endl;
       }
        if (crn7==128)
       {
       page3<<"CRS6: SC 550 128 Science"<<endl;
       }
        if (crn7==129)
       {
       page3<<"CRS6: SC 551 129 Science (lab)"<<endl;
       }
        if (crn7==130)
       {
       page3<<"CRS6: PSYCH 150 130 Psychology"<<endl;
       }
        if (crn7==131)
       {
       page3<<"CRS6: FL 901 131 Foreign language"<<endl;
       }
        if (crn7==132)
       {
       page3<<"CRS6: MTH 190 132 Calculus"<<endl;
       } 
    page3 <<"          "<<endl;
    page3 <<"            "<<"Total hours: 18.00"<<endl;






    page3 <<"         "<<endl;
    page3 <<"_____________________________________________________"<<endl;
    page3 <<"_____________________________________________________"<<endl;
    
  page3.close();

   ifstream infile; 
   infile.open("page3.dat"); 
   infile >> stunumber; 
   infile >> lastname; 

 };
```




The following are all of the functions I will use in the main method: 

Function 1: This aborts the program if the user enters a number greater than 3 or less than one when promted for the page number. 
```
    void abortit()

    {

        for (page<1;page>=4;)

        {   

     cout << "(ABORT: Please enter a number 1-3)" << endl; 
     exit(0);
     break;

        }

    }

```




Function 2: The user inputs the CRN numbers for the classes they would like to take.

```
    void mycrns()
    {
        cout<<"Use to above list to find the CRNs for your desired courses:"<<endl;
        cout<<""<<endl;
        cout<<"Please choose (any) 6 courses, one at a time."<<endl;
        cout<<"Enter the CRN for course 1: "<<endl;
        cin>>crn2;

        cout<<"Enter the CRN for course 2: "<<endl;
        cin>>crn3;


        cout<<"Enter the CRN for course 3: "<<endl;
        cin>>crn4;

        cout<<"Enter the CRN for course 4: "<<endl;
        cin>>crn5;

        cout<<"Enter the CRN for course 5: "<<endl;
        cin>>crn6;

        cout<<"Enter the CRN for course 6: "<<endl;
        cin>>crn7;
    }

```




Function 3: This asks if you would like to view the CRN numbers. If you type "yes" it will display them.

```
void switchcrn()

    {
       if (yesno="yes")
       {
            cout<<" "<<endl;
            cout<<"The list of classes available to you are as follows:"<<endl;

        if (yesno="yes")
        switch (crn1) 

                  { 

                default: cout<<"Literature: CRN 123"<<endl;

                 case 1: cout<<"Computer Programming: CRN 124"<<endl;


                case 2: cout<<"Web Design: CRN 125"<<endl;

                 case 3: cout<<"Management of security and forensics: CRN 126"<<endl;

                case 4: cout<<"Introduction to E-commerce: CRN 127"<<endl;

                 case 5: cout<<"Science: CRN 128"<<endl;

                 case 6: cout<<"Science (lab): CRN 129"<<endl;

                case 7: cout<<"Psychology: CRN 130"<<endl;

                case 8: cout<<"Foreign language: CRN 131"<<endl;

                case 9: cout<<"Calculus: CRN 132"<<endl;



                break;  
                  };
                  cout<<""<<endl;


    }
      }

```




Function 4: This function simply outputs the following message in the console: ""Generating schedule....Successfully generated schedule."

```
     void viewcrn()

    {
        mycrns();

        cout<<" "<<endl;
        cout<<"Generating schedule...."<<endl;
        cout<<"Successfully generated schedule."<<endl;
       }
```




Function 5: If the user enters a number less than one they get an error message.
```

    void abortlessthan()

    {

        while (page<1)

     {   

    cout << "(ABORT: Please enter a number 1-3)" << endl; 
    exit(0);
    break;

        }

    }

```




Function 6: Prompts the user to enter their student number.
```
    void mystunumber()

  {
      cout<<" "<<endl;
        cout<<"Enter your student number: "<<endl;
      cin>>stunumber;

  };

```



Function 7: Prompts the user for their first name.

```
   void myfirstname()

   {
       cout<<"Enter your first name: "<<endl;
    cin>>firstname;

   };

```

Function 8: Prompts the user for their last name. 

```
   void mylastname()

   {
       cout<<" "<<endl;
       cout<<"Enter your last name: "<<endl;
    cin>>lastname;

   };

```



Function 9: Prompts the user for their SSN

```
   void myssn()

   {
       cout<<" "<<endl;
       cout<<"Enter your SSN"<<endl;
    cin>>SSN;

   };

```



Function 9: Prompts the user to enter a page to view.

```
  void mypage()

   {
       cout<<" "<<endl;
       cout<<"View page one, two, or three? (Type 1, 2 or 3.)"<<endl;
   };

```



Function 10: If statements that output the messages below when you open pages 1, or 2.

```
 void mypagenumber()
 {
     cin>>page;
     Cpage1 obj1;

    if(page==1)
        { 

           cout << "Going to the initialization screen..." << endl; 
           obj1.coutPage1(); 
           exit (0);


}

     if (page>=1)
     {
    obj1.coutPage1(); 
     }

     if (page==2)
     {
         cout<<"Opening page 2";
         pg2();
         exit (0);
     }

     if(page==3)
{   
             do
                {
                    pg3(); 
                        break;
                }
            while (page==3);

              if(page>=2)
            { 
             do
                {
                    pg2(); 
                        break;
                }
            while (page>=2);
        }



     if (page<1)
     {
     abortlessthan();
     }

     else if (page>=4)
     {
     abortit();
     }


 }
 }


```



Function 11: Prompts the user for their major.

```
  void mymajor()

   {
       cout<<" "<<endl;
       cout<<"Enter your major: "<<endl;
       cin>>major;
       cout<<"";


   };


```



Function 12 (rather large, converts the input CRNs into the actual class names. Just a bunch of if statements.)

```
  void mycrntoclasses()

   {
       if (crn2=123)
       {
       cout<<"Literature: CRN 123"<<endl;
       }
        if (crn2=124)
       {
       cout<<"Computer Programming: CRN 124"<<endl;
       }
        if (crn2=125)
       {
       cout<<"Web Design: CRN 125"<<endl;
       }
        if (crn2=126)
       {
       cout<<"Management of security and forensics: CRN 126"<<endl;
       }
        if (crn2=127)
       {
       cout<<"Introduction to E-commerce: CRN 127"<<endl;
       }
        if (crn2=128)
       {
       cout<<"Science: CRN 128"<<endl;
       }
        if (crn2=129)
       {
       cout<<"Science (lab): CRN 129"<<endl;
       }
     if (crn2=130)
       {
       cout<<"Psychology: CRN 130"<<endl;
       }
        if (crn2=131)
       {
       cout<<"Foreign language: CRN 131"<<endl;
       }
    if (crn2=132)
       {
       cout<<"Calculus: CRN 132"<<endl;
       } 


       if (crn3=123)
       {
       cout<<"Literature: CRN 123"<<endl;
       }
        if (crn3=124)
       {
       cout<<"Computer Programming: CRN 124"<<endl;
       }
        if (crn3=125)
       {
       cout<<"Web Design: CRN 125"<<endl;
       }
        if (crn3=126)
       {
       cout<<"Management of security and forensics: CRN 126"<<endl;
       }
        if (crn3=127)
       {
       cout<<"Introduction to E-commerce: CRN 127"<<endl;
       }
        if (crn3=128)
       {
       cout<<"Science: CRN 128"<<endl;
       }
        if (crn3=129)
       {
       cout<<"Science (lab): CRN 129"<<endl;
       }
        if (crn3=130)
       {
       cout<<"Psychology: CRN 130"<<endl;
       }
        if (crn3=131)
       {
       cout<<"Foreign language: CRN 131"<<endl;
       }
        if (crn3=132)
       {
       cout<<"Calculus: CRN 132"<<endl;
       } 



       if (crn4=123)
       {
       cout<<"Literature: CRN 123"<<endl;
       }
        if (crn4=124)
       {
       cout<<"Computer Programming: CRN 124"<<endl;
       }
        if (crn4=125)
       {
       cout<<"Web Design: CRN 125"<<endl;
       }
        if (crn4=126)
       {
       cout<<"Management of security and forensics: CRN 126"<<endl;
       }
        if (crn4=127)
       {
       cout<<"Introduction to E-commerce: CRN 127"<<endl;
       }
        if (crn4=128)
       {
       cout<<"Science: CRN 128"<<endl;
       }
        if (crn4=129)
       {
       cout<<"Science (lab): CRN 129"<<endl;
       }
        if (crn4=130)
       {
       cout<<"Psychology: CRN 130"<<endl;
       }
        if (crn4=131)
       {
       cout<<"Foreign language: CRN 131"<<endl;
       }
        if (crn4=132)
       {
       cout<<"Calculus: CRN 132"<<endl;
       } 



       if (crn5=123)
       {
       cout<<"Literature: CRN 123"<<endl;
       }
        if (crn5=124)
       {
       cout<<"Computer Programming: CRN 124"<<endl;
       }
        if (crn5=125)
       {
       cout<<"Web Design: CRN 125"<<endl;
       }
        if (crn5=126)
       {
       cout<<"Management of security and forensics: CRN 126"<<endl;
       }
        if (crn5=127)
       {
       cout<<"Introduction to E-commerce: CRN 127"<<endl;
       }
        if (crn5=128)
       {
       cout<<"Science: CRN 128"<<endl;
       }
        if (crn5=129)
       {
       cout<<"Science (lab): CRN 129"<<endl;
       }
        if (crn5=130)
       {
       cout<<"Psychology: CRN 130"<<endl;
       }
        if (crn5=131)
       {
       cout<<"Foreign language: CRN 131"<<endl;
       }
        if (crn5=132)
       {
       cout<<"Calculus: CRN 132"<<endl;
       } 



       if (crn6=123)
       {
       cout<<"Literature: CRN 123"<<endl;
       }
        if (crn6=124)
       {
       cout<<"Computer Programming: CRN 124"<<endl;
       }
        if (crn6=125)
       {
       cout<<"Web Design: CRN 125"<<endl;
       }
        if (crn6=126)
       {
       cout<<"Management of security and forensics: CRN 126"<<endl;
       }
        if (crn6=127)
       {
       cout<<"Introduction to E-commerce: CRN 127"<<endl;
       }
        if (crn6=128)
       {
       cout<<"Science: CRN 128"<<endl;
       }
        if (crn6=129)
       {
       cout<<"Science (lab): CRN 129"<<endl;
       }
        if (crn6=130)
       {
       cout<<"Psychology: CRN 130"<<endl;
       }
        if (crn6=131)
       {
       cout<<"Foreign language: CRN 131"<<endl;
       }
        if (crn6=132)
       {
       cout<<"Calculus: CRN 132"<<endl;
       } 



       if (crn7=123)
       {
       cout<<"Literature: CRN 123"<<endl;
       }
        if (crn7=124)
       {
       cout<<"Computer Programming: CRN 124"<<endl;
       }
        if (crn7=125)
       {
       cout<<"Web Design: CRN 125"<<endl;
       }
        if (crn7=126)
       {
       cout<<"Management of security and forensics: CRN 126"<<endl;
       }
        if (crn7=127)
       {
       cout<<"Introduction to E-commerce: CRN 127"<<endl;
       }
        if (crn7=128)
       {
       cout<<"Science: CRN 128"<<endl;
       }
        if (crn7=129)
       {
       cout<<"Science (lab): CRN 129"<<endl;
       }
        if (crn7=130)
       {
       cout<<"Psychology: CRN 130"<<endl;
       }
        if (crn7=131)
       {
       cout<<"Foreign language: CRN 131"<<endl;
       }
        if (crn7=132)
       {
       cout<<"Calculus: CRN 132"<<endl;
       } 


   };

```



Main: This lets everything execute. The if statement controls when/if page two and 3 open (page 1 always opens). 

```
int main () 
{

    Cpage1 obj1;

     //Functions
     myfirstname();
     mylastname();
     mystunumber();
     myssn();
     mymajor();
     mypage();
     mypagenumber();
     switchcrn();
     viewcrn();




if(page>=3)
{   
             do
                {
                    pg3(); 
                        break;
                }
            while (page>=3);
        }

            if(page>=2)
            { 
             do
                {
                    pg2(); 
                        break;
                }
            while (page>=2);
        }




 return 0;    
}
    
