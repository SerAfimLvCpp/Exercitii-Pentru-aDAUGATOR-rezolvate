Welcome to the Exercitii-Pentru-aDAUGATOR-rezolvate wiki!
Ziua 1
Calcularea Mediei:
Scrie un program care primește două numere de la utilizator și afișează media lor

#include <stdio.h>
int main(){
	
	int a, b;
	float media;
	
		printf("Introdu primul numar: ");
	scanf("%d", &a);
	
		printf("Introdu al doilea numar: ");
	scanf("%d", &b);
	
	media = a + b;
	media /= 2;
	
		printf("Media este: %.2f", media);
	
}

Joc de Ghicire:
Creează un program care generează un număr aleatoriu între 1 și 100. Utilizatorul încearcă să ghicească numărul și primește indicii dacă răspunsul său este prea mare sau prea mic.
#include <iostream>
#include <time.h>
using namespace std;

string drop;
int number;
int n;

void game() {
    n = 0;
    cout << "\nPentru a incepe jocul, tastati: START\n";
    cin >> drop;

    srand((unsigned) time(NULL));
    int random = rand() % 100;
    
    if (drop == "START" || drop == "start" || drop == "Start" ) {
        cout << "Jocul a inceput.";
    } else {
        cout << "EROARE";
    }

    while (n == 0) {
        cout << "\nGhiceste numarul. Scrie la ce numar te gandesti: \n";
        cin >> number;
        
        if (number < random)
            cout << "\nEste prea mic.";
        else if (number > random)
            cout << "\nEste prea mare";
        else {
            cout << "Este corect\n";
            cout << random;
            n++;
        }
    }
}

int main() {
    string rs;
    int m = 0;
    for(int i = 1; i > m;) {
        game();
        cout << "\nVei relua jocul?\n";
        cin >> rs;
        
        if (rs == "Da" || rs == "da" || rs == "DA") 
            m = 0;
        else if (rs == "Nu" || rs == "nu" || rs == "NU") 
            m++;
    }
    
    return 0;
}

Zaruri
Implementează un joc de zaruri în care utilizatorul încearcă să ghicească suma a două zaruri aruncate. Dacă suma este 7 sau 11, utilizatorul câștigă; dacă este 2, 3 sau 12, utilizatorul pierde; în orice alt caz, jocul continuă.


#include <iostream>
#include <time.h>
using namespace std;

string drop;
int number;
int n;

void game() {
    n = 0;
    cout << "\nPentru a arunca zarul, tastati: DROP\n";
    cin >> drop;
    int sumaZar;
    
    if (drop == "DROP" || drop == "drop" || drop == "Drop" ) {
		srand((unsigned) time(NULL));
    		int random1 = rand() % 6+1;
    	srand((unsigned) time(NULL));
    		int random2 = rand() % 6+1;
        sumaZar = random1 + random2;
		cout << "Zarul a fost arucat.";
        
    } else {
        cout << "EROARE";
    }

    while (n == 0) {
        cout << "\nGhiceste suma zarurilor. Scrie la ce numar te gandesti: \n";
        cin >> number;
        
       
         if(sumaZar == 2 || sumaZar == 3 || sumaZar == 12){
        	cout << "\nCondoleante! Ai pierdut!";
        	n++;
		}
		else if(number != sumaZar)
		{
			cout << "\nGresit! Mai incearca!\n";
		}
        else if (sumaZar == 7 || sumaZar == 11){
			cout << "\nFelicitari! Ai cistigat!\n";
			n++;
				}
				
		else if(sumaZar == number){
			cout << "\nAi ghicit! Jocul Continua!\n";
			n++;
				}  
    }
}

int main() {
    string rs;
    int m = 0;
    for(int i = 1; i > m;) {
        game();
        cout << "\nVei relua jocul?\n";
        cin >> rs;
        
        if (rs == "Da" || rs == "da" || rs == "DA") 
            m = 0;
        else if (rs == "Nu" || rs == "nu" || rs == "NU") 
            m++;
    }
    
    return 0;
}
