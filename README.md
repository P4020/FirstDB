# FirstDB

### Descrizione progetto

###### Creare una cartella sul desktop nominandola con il proprio : "cognome.nome.classe.nomedelprogetto"

![image](https://user-images.githubusercontent.com/117436985/235085824-335c42ce-4538-4929-ae9f-4995d9ffc6b7.png)

###### Aprire la cartella in VisualStudio Code e, aprendo un nuovo terminale, digitare la riga di comando : "dotnet new console". Questo comando andrà a generare dei file nella cartella che abbiamo aperto in Code.


![image](https://user-images.githubusercontent.com/117436985/235087757-cebe3990-ddc3-4d95-b4fa-94a364c6e10a.png)


![image](https://user-images.githubusercontent.com/117436985/235088243-ec7f129e-3ace-4355-b198-8681ab9f4c89.png)

### Dove trovare il file db chinook.db
###### Il link per scaricare il file db chinook.db è : 

https://www.sqlitetutorial.net/sqlite-sample-database/#:~:text=the%20following%20link.-,Download%20SQLite%20sample%20database,-In%20case%20you

###### Appena entrati nel sito scaricare il file dal link evidenziato!

### Codice per visualizzare gli artisti

###### Per andare a visualizzare gli artisti nel file SQL chinook.db bisogna utilizzare il codice sottostante :

using SQLite;


Console.WriteLine("Hello World");

SQLiteConnection cnl = new SQLiteConnection("chinook.db");

var tblArtist = cnl.Query<Artist>("select * from artists");

Console.WriteLine( $"In questa tabella ci sono {tblArtist.Count} record!");

public class Artist

{

    public int ArtistId{get; set;}
    
    public string Name{get; set;}
    
}
    
###### Questa immagine rappresenta il codice usato per la visualizzazione degli artisti.
![image](https://user-images.githubusercontent.com/117436985/235088812-f6029c04-12a4-4f35-9594-6de4aa0c02f4.png)

### Libreria SQL

###### La libreria da usare per far funzionare il codice SQL è : "using SQLite;"
###### e digitare nel terminale la seguente riga di codice : "dotnet add package sqlite-net-pcl".
###### Inoltre su VisualStudio Code installare l'estenzione : "SQLite"

![image](https://user-images.githubusercontent.com/117436985/236143761-ec2f2076-6105-4c3d-9523-8816d9f4f4cd.png)

###### e se vuoi anche visualizzare tutti gli artisti del file chinook.db installare l'estenzione : "SQLite Viewer"

![image](https://user-images.githubusercontent.com/117436985/236144223-1c71779c-6e3b-4417-8a98-ede510d16759.png)







