# HotTo Upute za razlicite probleme


## VSCode i GitHub

U Dokumentima u mapi gdje spremate sve vježbe
napravite novi folder vjezba003

Otvorite VSCode

Otvoriti CMD / PowerShell u VS Code pomocu 
naredbe CTRL + J

prebacite se u mapu vjezba003

kada ste u mapi 
```bash

git clone https://github.com/USER/zadatak.git

// zatim otvorite cijeli projekt
code .

```

Za testiranje zadatka u terminalu upišite

```bash
dotnet build  → kompajlira, prevodi u strojni jezik

dotnet run    → pokreće cijeli program za provjeru
```



## KAKO PREDATI ZADATAK NA KRAJU

Sačuvati datoteku Program.cs pomoću CTRL+S

Zatim upisati sljedeći niz naredbi u VSCode terminalu 
koji se aktivira pomoću CTRL + J

```bash

git add .
git commit -m "Rješenje zadatka"
git push


```

Idi na svoj GitHub Classroom repo na webu

Ako vidiš svoj commit:
Rješenje zadatka

→ Zadatak je predan. 
U Classroomu će pisati "Delivered".



## Ispis podataka

✔️ Console.WriteLine()
Ispisuje tekst i prelazi u novi red nakon ispisa
Primjer:
```csharp
Console.WriteLine("Pozdrav!");
```

✔️ Ispis varijabli

Primjer:
```csharp
string ime = "Marko";
Console.WriteLine(ime);
```

✔️ Interpolacija stringa
Primjer:
```csharp
Console.WriteLine($"Ime: {ime}");
```

✔️ Ispis više podataka odjednom
Primjer:
```csharp
int godine = 17;
Console.WriteLine($"Ime: {ime}, Godine: {godine}");
```

# Rješenje problema sa NULL pogreškom

U .NET 10 (C# 13) najčešći uzrok “null literal or possible null value to non-nullable type” 
i drugih nullability upozorenja je to što kompajler strogo prati nullable anotacije.

Console.ReadLine() može vratiti null → warning.

Rješenje:
```csharp
string ime = Console.ReadLine() ?? "";
```