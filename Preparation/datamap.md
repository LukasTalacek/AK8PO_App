enum Studium {
	case Prezencni
	case Kombinovane
}

enum TypStudia {
	case Bc.
	case Mgr.
}

enum Jazyk {
	case Eng
	case Cz
}

enum Zakonceni {
	case Zapocet
	case KlZ
	case Zkouska
}

enum TypStitku {
	case Prednaska
	case Cviceni
	case Seminar
	case Zapocet
	case KlZ
	case Zkouska
}

Struct Kontakt {
	var email: String
	var telefon: String
}

1) Skupina
	var zkratka: String
	var nazev: String
	var rocnik: Int
	var pocetStudentu: Int
	var formaStudia: Studium
	var typStudia: TypStudia
	var jazyk: Jazyk

2) Predmet
	var zkratka: String
	var nazev: String
	var garant: Zamestnanec
	var kredity: Int
	var pocetTydnu: Int
	var prednasky: Int
	var cviceni: Int
	var seminare: Int
	var zakonceni: Zakonceni
	var jazyk: Jazyk
	var pocetStudentu: Int

3) Zamestnanec
	var jmeno: String
	var prijmeni: String
	var celeJmeno: String	// "computed prop" -> jmeno + prijmeni
	var osobniKontakt: Kontakt
	var pracovniKontakt: Kontakt
	var doktorand: Bool
	var uvazek: Double
	var stitky: <Stitky>
	func pracBodyEng -> Int
	func pracBodyCz -> Int

4) Stitky
	var nazev: String
	var zamestnanec: Zamestnanec
	var predmet: Predmet
	var typ: TypStitku
	var pocetStudentu: Int
	var pocetHodin: Int
	var pocetTydnu: Int
	var jazyk: Jazyk
	func bodyZaStitek -> Double

5) Vahy pracovnich bodu
	Hodina přednášky – double – 1,8
	Hodina cvičení – double – 1,2
	Hodina semináře – double – 1,2
	Hodina přednášky anglicky – double – 2,4
	Hodina cvičení anglicky – double – 1,8
	Hodina semináře anglicky – double – 1,8
	Udělení jednoho zápočtu – double – 0,2
	Udělení jednoho klasifikovaného zápočtu – double – 0,3
	Udělení jedné zkoušky – double – 0,4
	Udělení jednoho zápočtu anglicky – double – 0,2
	Udělení jednoho klasifikovaného zápočtu anglicky – double – 0,3
	Udělení jedné zkoušky – anglicky - double – 0,4






