# General concepts

## Current Knowledge

## 4 Main concepts of OOP

- Encapsulation, Abstraction, Inheritance, Polymorphism

## Core OOP Terms

- Class, Object, Interface, Constructor, Abstract class, Sealed class

## Encapsulation

- Koncept koji govori o sakrivanju atributa klase, to se postiže pomoću `protected` i `private` i da bi se pristupilo tim atributima koristimo getere i settere. Na ovaj način imamo punu kontrolu nad atributima.

## Inheritance (Nasleđivanje)

- Koncept gde druge klase mogu da koriste već postojeće klase.

## Abstraction

- Način sakrivanja kompleksnih delova koda korišćenjem interfejsa i abstraktnih klasa kako bi kod bio čitljiviji.

## Polymorphism (Polimorfizam)

- Sposobnost objekta da se ponaša na različite načine.

## SOLID Principles

SOLID principi su MEHANIZMI za transformaciju TIGHT COUPLED aplikacija u LOOSE COUPLED aplikacije!

### Single Responsibility Principle (SRP)

- Design princip: kada kodiramo, moramo misliti unapred - u budućnosti će doći izmene, i treba da dizajniramo tako da te izmene budu lokalizovane.
- Glavna suština je **izolacija** delova sistema, da kada želimo da promenimo jedan deo, ne moramo da prilagođavamo ceo codebase tim izmenama, već samo da zamenimo/izmenimo taj specifičan segment.
- **SRP vodi ka LOOSE COUPLING** - klase su manje zavisne jedne od drugih, jer svaka ima jasnu, jedinstvenu odgovornost.
- **Bez SRP-a imamo TIGHT COUPLING** - sve je isprepletano, pa promena u jednom mestu zahteva promene na mnogo mesta.
- **Kriterijum za dobro napisan kod prema SRP-u:**
  - Dovoljno je da pokrenem testove samo za tu specifičnu klasu
  - Ne moram da testiram još 10 stvari
  - Nema "shotgun surgery" efekta gde jedna promena zahteva modifikacije na mnogo mesta
- **Ključna vrednost SRP-a za održavanje sistema:**
  - Smanjuje kognitivno opterećenje - ne moram da razumem ceo sistem da bih napravio jednu promenu
  - Ubrzava razvoj - timovi mogu raditi paralelno na različitim delovima
  - Smanjuje rizik - promena u jednom modulu ne ugrožava druge module

### Open-Closed Principle (OCP)

- Klase su otvorene za ekstenzije ali zatvorene za modifikaciju.
- Treba organizovati kod tako da ako se u budućnosti pojave novi zahtevi, mogu lako da ih dodam kroz novu integraciju.
- Možemo dodati NOVE funkcionalnosti bez da menjamo POSTOJEĆI kod.
- Primer: kreiramo novi payment provider - ideja je da ekstendujemo postojeću klasu sa tim providerom ali da taj provider radi samostalno.
- Dizajniraj tako da za novu funkcionalnost pišeš NOV kod, a ne menjaš STARI kod.

### Liskov Substitution Principle (LSP)

- **"Ako kažeš da je nešto PATKA, onda to mora da se PONAŠA kao patka. Ako ne može da leti ili ne može da kvace, onda to NIJE patka."**
- **Problem:** Kada klasa nasleđuje drugu klasu, ali NE POŠTUJE njena pravila ponašanja, tada:
  1. Kod postaje nepredvidiv
  2. Testovi padaju kada zamenimo baznu klasu
  3. Moramo dodavati provere tipa (`instanceof`)
  4. Gubimo prednosti polimorfizma
- **Liskov Substitution Principle je garancija za polimorfizam:**
  - "Ako kažeš da je `B` podtip od `A`, onda SVUDA gde koristiš `A` moraš moći da koristiš `B` bez da se ponašanje promeni."
- **LSP nam omogućava da:**
  1. Bezbedno koristimo polimorfizam - ne moramo proveravati `instanceof`
  2. Pišemo čistije testove - možemo koristiti mock objekte
  3. Imamo predvidiv kod - nasleđivanje ne donosi iznenađenja
  4. Pravimo fleksibilne sisteme - lako dodajemo nove podtipove
- **Najvažnija lekcija:** "Ne pitaj da li je B podklasa od A. Pitanje je: da li se B PONAŠA kao A? Ako ne, onda ne nasleđuj!"

### Interface Segregation Principle (ISP)

- Podeli velike interfejse na manje, specifičnije interfejse kako bi klijenti zavísili samo od metoda koje zaista koriste.
- **Ne teraj klase da lažu. Ako kažeš da implementiraš interfejs, onda implementiraj sve metode. Ako nećeš sve, onda nemoj taj interfejs.**
- **ISP nas sprečava da:**
  1. Imamo klase sa praznim ili lažnim implementacijama
  2. Povežemo stvari koje nisu povezane
  3. Učinimo sistem krutim i teškim za održavanje
- **Problem:** Kada imate preveliki interfejs (tzv. "fat interface" ili "god object"), klase su primorane da implementiraju metode koje im ne trebaju. To vodi ka:
  1. Praznim implementacijama (`throw new Error()`)
  2. Lažnim implementacijama koje ne rade ništa
  3. Visokom coupling između nepotrebnih stvari
  4. Teškom održavanju

### Dependency Inversion Principle (DIP)

- Govori o zavisnostima modula i uvođenjem abstrakcije kroz upotrebu interfejsa.
- Biznis logika ne bi trebala da zavisi od ORM-a.
- Clean arhitektura je primer Dependency Inversion principa u praksi.
- Pri designu koristimo Dependency Injection da kroz konstruktor kreiramo objekte, a ne da u okviru klase imamo implementaciju za niže nivoe.
- Bitno je da viši nivoi ne zavise od nižih i da se uvede abstrakcija kroz razdvajanje logike od interfejsa.
- Ovo nam omogućava da je aplikacija loose coupled i da nam u budućnosti daje prostor da menjamo određene delove koda bez da menjamo ceo code base.

## Dependency Injection (DI)

- Kao i SOLID principi, DI pomaže da aplikacija ne bude tight coupled.
- Obezbeđuje nam da injektujemo neki objekat u klasu koju želimo da instanciramo bez da ta klasa mora da kreira zavisnosti.
- Pojednostavljuje testiranje.
- Dependency Injection je kada kroz konstruktor injektiramo objekat neke druge klase u našu klasu koju želimo da instanciramo.
- Constructor je samo jedan način da se izvrši DI, može i kroz settere.

## Access Modifiers

- Definiše vidljivost metoda, klasa i interfejsa, ko ima pravo da pristupi određenim promenljivim.

## Examples / Notes

## Primer za Dependency Inversion Principle

```typescript
// ❌ BEZ DIP-a
class UserService {
  private logger = new FileLogger(); // Zavisi od konkretne implementacije

  createUser(user: User): void {
    // Business logika...
    this.logger.log(`Created user: ${user.name}`); // Uvek u fajl
  }
}

// ✅ SA DIP-om
interface Logger {
  log(message: string): void;
}

class UserService {
  constructor(private logger: Logger) {} // Zavisi od apstrakcije

  createUser(user: User): void {
    // Business logika...
    this.logger.log(`Created user: ${user.name}`);
    // Može biti bilo koji logger!
  }
}

// Različite implementacije
class FileLogger implements Logger {
  log(message: string): void {
    // Log u fajl
  }
}

class ConsoleLogger implements Logger {
  log(message: string): void {
    console.log(message);
  }
}

class DatabaseLogger implements Logger {
  log(message: string): void {
    // Log u bazu
  }
}

class ElasticsearchLogger implements Logger {
  log(message: string): void {
    // Log u Elasticsearch
  }
}

// Koristimo ono što nam treba
const userService1 = new UserService(new ConsoleLogger()); // Dev okruženje
const userService2 = new UserService(new FileLogger()); // Production
const userService3 = new UserService(new ElasticsearchLogger()); // Monitoring
```

## Questions / Confusions

- **Design patterns** - sekcija je prazna, treba dodati konkretne design patterns koje poznajem
- **Encapsulation vs Abstraction** - potrebno je bolje razumevanje razlike između ova dva koncepta
- **Abstract class vs Interface** - kada koristiti koji pristup?
- **Sealed class** - šta je tačno i kada se koristi?
- **Loose vs Tight Coupling** - potrebno je više praktičnih primera kako se ovo manifestuje u kodu
- **Clean Architecture** - spomenuta je u kontekstu DIP-a, ali nije jasno kako tačno izgleda struktura
- **Dependency Injection Container/IoC Container** - razlika između ručne DI i korišćenja DI kontejnera
- **ISP - konkretni primer "fat interface" problema** - kako izgleda loš interfejs i kako ga podeliti
