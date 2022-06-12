# Klasifikacija delova politike privatnosti

Ovaj rad se bavi klasifikacijom delova politike privatnosti.
Postojeće klase su sledeće: 
  - First Party Collection/Use
  - Third Party Sharing/Collection
  - User Access, Edit and Deletion
  - Data Retention
  - Data Security
  - International and Specific Audiences
  - Do Not Track
  - Policy Change
  - User Choice/Control
  - Introductory/Generic
  - Practice not covered
  - Privacy contact information
  
## Struktura repozitorijuma
U ovoj podsekciji je detaljno objašnjena struktura repozitorijuma, sadržaj i svrha svakog foldera i fajla.

### Folder annotations
U ovom folderu se nalaze podaci u sirovom obliku. Ovi podaci su wranglovani kako bi se napravio dataset pogodan za treniranje i test modela.

Link do sirovog dataseta: https://www.usableprivacy.org/data

### Folder datasets
U ovom folder se nalaze fajlovi:
 - wrangled_data.csv sadrži filtrirane podatke iz fajlova pod annotations folderom, koji su pogodni za dalju obradu.
 - train_preprocessed.csv sadrži pretprocesirane podatke za trening modela. Predstavlja 70% wrangled_data.csv podataka.
 - test_preprocessed.csv sadrži pretprocesirane podatke za test modela. Predstavlja 30% wrangled_data.csv podataka.

### Folder models
Ovaj folder sadrži fajlove u kojima su sačuvani trenirani modeli (težine). Naziv svakog fajla govori koji model ima sačuvan u sebi.

### .ipnyb fajlovi
- DataWrangling.ipynb i Preprocessing.ipynb sadrže implementaciju manipulacije nad podacima.
- KNN, BERT, LSTM, LSTM_GloVe i SVM.ipynb sadrže implemenacije navedenih modela pojedinačno. U ovim fajlovima se vršilo treniranje i čuvanje istreniranih modela.
- Tests.ipynb sadrži testove svih korišćenih modela. Testovi su izvršeni tako da se rezultati mogu videti bez pokretanja samog koda. 

## Upustvo za pokretanje
Za pokretanje je poželjno imati najnovije stabilne verzije biblioteka tensorflow, keras i sci-kit learn (pisano 12.06.2022.).  
Pokretanje je moguće izvršiti iz okruženja jupyter notebook.  
U slučaju potrebe za pokretanjem (moguće videti rezultate i bez pokretanja) predlaže se pokretanje samo Tests.ipynb.  
Pokretanje ostalih fajlove može dovesti do promene u sačuvanim modelima.  

**Napomena**!!!
Za pokretanje LSTM_GloVe.ipynb neophodno je skinuti GloVe fajl i napraviti GloVe folder u repozitorijumu. Potom skinut fajl dodati u novonastali folder.  
Fajl dostupan na linku: https://drive.google.com/file/d/12iAJo3p-f6hk72cg7Zd4w8SsgIX3x__O/view?usp=sharing

Za pokretanje BERT sekcije u Tests.ipynb potrebno je skinuti fajl sa linka: https://drive.google.com/file/d/1HRMNs2gOdSB0jevEA36DTY5KYqz1NPI-/view?usp=sharing  
Nakon sto se skine i raspakuje, dodati fajl u folder models.
