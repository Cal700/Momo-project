# Momo-project
mimics as momo
#include<iostream>
using namespace std;

int main() {
	int balance = 1000;
    string pin = "0000";
    int attempts = 0;
    int choice;
    
    do {
        cout << "Enter your PIN: ";
        cin >> pin;
        attempts++;
        
        if (pin == "0000") {
            cout << "Authentication successful!" << endl;
            do {
                cout << "What would you like to do?" << endl;
                cout << "1. Check balance" << endl;
                cout << "2. Send money" << endl;
                cout << "3. Reset PIN" << endl;
                cout << "4. Exit" << endl;
                cin >> choice;
                
                switch (choice) {
                    case 1:
                        cout << "Your balance is " << balance << endl;
                        break;
                    case 2:
                        int amount,num,num1,rnum,pin,attempt;
                        cout << "Enter amount: ";
                        cin >> amount;
                        cout<<"Enter mobile number:"<<endl;
                        cin>>num;
                        
                        cout<<"Confirm number:"<<endl;
                        cin>>num1;
                        if(num1!=num){
                        	cout<<"wrong number"<<endl;
                        	break;
						} else{
							
					
						}
                        cout<<"Enter Reference:"<<endl;
                        cin>>rnum;
                        
                        cout<<"Enter mm.pin:"<<endl;
                        cin>>pin;
                        attempt++;
                        if (pin == 0000) {
                           cout << "Done!" << endl;
                       } else if(pin!=0000){
                       	cout<<"Failed!";
					   }
					   
                        if (amount <= balance) {
                            balance -= amount;
                            cout << "Money sent successfully!" << endl;
                        } else {
                            cout << "Insufficient balance." << endl;
                        }
                        break;
                    case 3:
                        cout << "Enter your new PIN: ";
                        cin >> pin;
                        cout << "Confirm PIN: "<<endl;
                        cin >> pin;
                        if (pin!=pin){
                        	cout<<"Unmatch PIN";
						} else { break;
						}
                        cout << "PIN changed successfully";
                        break;
                    case 4:
                        cout << "Exiting program." << endl;
                        break;
                    default:
                        cout << "Invalid choice. Please try again." << endl;
                        break;
                }
            } while (choice != 4);
        } else {
            cout << "Authentication failed. Please try again." << endl;
        }
        
        if (attempts == 3) {
            cout << "Too many incorrect attempts. Exiting program." << endl;
            break;
        }
    } while (true);

	
	
	
	
	
	
	return 0;
}
