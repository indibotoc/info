> by Indi Boțoc  
indibotoc@gmail.com  
*Timisoara, Romania, 13.11.2025*

# Atestatul la informatică
![Descrierea imaginii](https://github.com/indibotoc/info/blob/main/assets/atf.png)
# Ce facem la atesat?

Limbajul C a fost inventat de către **Dennis Ritchie** pentru a realiza sistemul de operare **Unix** (noi îl știm ca Linux). Astfel, aproape toate programele scrise în C pot fi compilate în C++, eventual cu foarte puține modificări.

## Limbaje de programare
**Limbajele de programare** sunt limbaje asemănătoare cu limbajul uman. Conțin cuvinte (destul de puține), semne de punctuație, operații matematice și au reguli de scriere. Programele care rulează pe orice calculator au fost scrise într-un limbaj de programare. Există numeroase limbaje de programare, precum C, C++, Pascal, Java, Python, PHP, Javascript, etc. 

Programul scris într-un limbaj de programare se numește **program sursă** și trebuie traduse într-un limbaj pe care îl înțelege procesorul, numit **cod mașină**, sau **program executabil**. Pentru anumite limbaje de programare operația de traducere se numește **compilare** (cazul lui C, C++, Pascal, etc.), pentru alte limbaje (PHP, Python, Javascript, etc.) operația de traducere se numește *interpretare*. Traducerea este realizată de un program specializat numit **compilator** sau interpretor.

Limbajul C++ este un limbaj compilat. Etapele scrierii unui program în C++ sunt:

- editarea programului C++; se obține fișierul sursă, cu extensia `.cpp`
- compilarea fișierului sursă; aici se verifică corectitudinea sintactică a programului (corectitudinea cuvintelor folosite, prezența semnelor de punctuație, etc.); dacă programul este corect sintactic, se va obține fișierul obiect, cu extensia `.o`
- editarea de legături; se stabilesc legături între fișierul obiect curent și alte fișiere obiect, ale programatorului sau incluse în compilator; în urma acestei etape se obține programul executabil. În Windows, fișierele executabile au extensia `.exe`
- programul executabil poate fi lansat în execuție (rulat).

## Primul program C++
Cum scriem un program C++? Avem nevoie cel puțin de un **editor de text** pentru scrierea sursei și de un compilator C++. Deși fișierul sursă poate fi realizat cu orice editor de text, de cele mai multe ori folosim un **IDE** (IDE = mediu de dezvoltare). Un IDE pentru C/C++ foarte utilizat este Code::Blocks.

Să considerăm un prim program C++:

```cpp
// primul program C++
#include <iostream>
using namespace std;
int main()
{
    /*
      primul program C++
      il scriem in Code::Blocks
    */
    cout << "Hello world";
    return 0; 
}
```
Dacă vom compila și rula acest program, pe ecran va apărea:
```bash
Hello world
```
Să analizăm acest program. El este alcătuit din mai multe linii:
- ```// primul program C++```  
    această linie reprezintă un comentariu. Comentariile sunt texte explicative care nu influențează comportamentul programului. Ele sunt pentru programatori, pentru a înțelege mai repede semnificația programului. Acest comentariu începe de la cele două caractere slash `//` și se termină la sfârșitul liniei.
- ```#include <iostream>```  
    liniile care încep cu `#` sunt interpretate înainte de compilarea propriu-zisă, de către un program numit *preprocesor*. În cazul nostru, directiva `#include` cere preprocesorului să includă în sursă o secțiune a codului C++ standard, **header**-ul `iostream`, care permite realizarea operațiilor de citire și afișare – la noi afișarea mesajului `Hello world` pe ecran.  
- ```using namespace std;```
în C++, identificatorii sunt grupați în spații de nume – **namespaces**. Există un spațiu de nume predefinit, cu numele `std`, din care fac parte toți identificatorii din biblioteca C++ standard.  
`cout`, ca și `endl`, este un identificator din spațiul de nume std și pentru a-l putea folosi trebuie folosită expresia `std::cout`. Pentru a ne referi mai simplu la identificatorii din spațiul de nume std se poate folosi instructiunea `using namespace std;`
- `int main()`  
    această linie reprezintă *declararea unei funcții*. În esență, o funcție este un grup de instrucțiuni care are un nume dat; în acest caz, funcția se numește main și este alcătuită din toate instrucțiunile care urmează. Vom discuta pe larg despre functii mai târziu.
    Funcția numită main este specială în toate programele C++; această funcție este apelată când se lansează în execuție programul și trebuie să apară în orice program C++, o singură dată.
- `{`  
    Parantezele acolade de la liniile 4 și 10 delimitează instrucțiunile care fac parte din funcția main

-  ```c
    /*  
    primul program C++  
    il scriem in Code::Blocks  
    */
    ```
    și acesta este un comentariu. Textele cuprinse între `/*` și `*/` nu influențează comportamentul programului. Ele pot să ocupe mai multe linii, sau pot să apară în interiorul unei linii.
- ` cout << “Hello world”;`  
    aceasta este o **instrucțiune** C++. O instrucțiune este o construcție (expresie, comandă) care face ceva. Instrucțiunile sunt “miezul” programelor, ele stabilind comportamentul acestora. Instrucțiunile dintr-un program se execută *în ordine, una după alta*.  
    → această instrucțiune produce afișarea pe ecran a textului Hello world. Ea este alcătuită din trei părți. cout semnifică dispozitivul standard de ieșire (**c**haracter **out**put) – de cele mai multe ori ecranul calculatorului. A doua parte este operatorul de inserție `<<`, care indică faptul că ceea ce urmează este trimis spre ecran. A treia parte este textul, `"Hello world"`, cuprins între ghilimele.  
    Să observăm prezența caracterului `;` la sfârșitul instrucțiunii. Orice instructiune C++ trebuie să se termine cu `;`, la fel cum orice propoziție în limba română se termină cu caracterul `.` (punct).  
    `Una dintre cele mai frecvente erori de sintaxă este să uităm să scriem ; la finalul unei instrucțiuni.`
- `return 0;`
    Această instrucțiune marchează finalul execuției funcției `main` și a programului nostru. Valoarea 0 semnifica faptul că programul s-a încheiat cu succes!
    Dacă în programul nostru ar fi fost și alte instrucțiuni după instrucțiunea `return 0;`, acestea **nu** s-ar mai fi executat.  
- `}`
    Acolada închisă `}` reprezintă finalul funcției `main`.


## Comentarii

Comentariile sunt texte care pot să apară în programul sursă și nu sunt luate în considerare la compilare. Ele sunt citite doar de către oameni, pentru a explica anumite secțiuni mai importante din program. Așa cum am văzut mai sus, în C++ sunt două tipuri de comentarii:
```c
// comentariu pe o linie
/* comentariu de tip bloc */
```
Comentariul pe o linie începe de caracterele `//` și se termină la finalul liniei. Comentariul de tip bloc începe la `/*`, se termină la `*/` și se poate întinde pe mai multe linii.

Comentariile sunt **importante**! Trebuie să învățăm să scriem cod pe care să-l înțelegem și peste o zi sau un an, iar prezența comentariilor este un pas înainte.