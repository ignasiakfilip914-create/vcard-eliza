import { motion } from "framer-motion";
import {
  Phone,
  Mail,
  MapPin,
  Download,
  MessageCircle,
  GraduationCap,
  CheckCircle,
  Star,
} from "lucide-react";

export default function App() {
  const contact = {
    name: "Korepetycje z Angielskiego",
    person: "Eliza Motyka",
    phone: "661413521",
    email: "eliza.motyka74@gmail.com",
    location: "Radomsko i okolice",
    whatsapp: "48661413521",
  };

  const vcard = `BEGIN:VCARD\nVERSION:3.0\nFN:${contact.person}\nORG:${contact.name}\nTITLE:Korepetycje z angielskiego dla uczniów klas 1-8\nTEL;TYPE=CELL:${contact.phone}\nEMAIL:${contact.email}\nADR;TYPE=HOME:;;${contact.location};;;;\nNOTE:Indywidualne korepetycje z języka angielskiego. Nauka praktycznej komunikacji. Dojazd do ucznia.\nEND:VCARD`;

  const downloadVCard = () => {
    const blob = new Blob([vcard], { type: "text/vcard;charset=utf-8" });
    const url = URL.createObjectURL(blob);
    const link = document.createElement("a");
    link.href = url;
    link.download = "eliza-motyka-korepetycje.vcf";
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
    URL.revokeObjectURL(url);
  };

  const benefits = [
    "Klasy 1–8 szkoły podstawowej",
    "Praktyczna komunikacja po angielsku",
    "Indywidualne podejście do każdego ucznia",
    "Dojazd na terenie Radomska i okolic",
  ];

  return (
    <div className="page">
      <motion.main
        initial={{ opacity: 0, y: 30 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.6 }}
        className="card"
      >
        <section className="hero">
          <div className="glow glow-one" />
          <div className="glow glow-two" />

          <div className="hero-content">
            <div className="badge">
              <GraduationCap size={16} />
              Korepetycje • Radomsko
            </div>

            <div className="icon-box">
              <GraduationCap size={48} />
            </div>

            <h1>
              Angielski,
              <br />
              który dziecko
              <br />
              naprawdę używa.
            </h1>

            <p>
              Indywidualne korepetycje dla uczniów klas 1–8. Przyjazna atmosfera,
              praktyczne ćwiczenia i nauka bez stresu.
            </p>
          </div>

          <div className="notice">
            <div>
              <Star size={20} />
              <strong>Zapisy na wakacyjne korepetycje</strong>
            </div>
            <p>Szybki kontakt telefoniczny lub przez WhatsApp.</p>
          </div>
        </section>

        <section className="content">
          <div className="top-row">
            <div>
              <p className="eyebrow">vCard</p>
              <h2>{contact.name}</h2>
              <p className="muted">{contact.person}</p>
            </div>
          </div>

          <div className="contact-grid">
            <a href={`tel:${contact.phone}`} className="contact-tile">
              <div className="tile-icon blue">
                <Phone size={20} />
              </div>
              <div>
                <p>Telefon</p>
                <strong>{contact.phone}</strong>
              </div>
            </a>

            <a href={`mailto:${contact.email}`} className="contact-tile">
              <div className="tile-icon blue">
                <Mail size={20} />
              </div>
              <div>
                <p>E-mail</p>
                <strong>{contact.email}</strong>
              </div>
            </a>

            <a
              href={`https://wa.me/${contact.whatsapp}`}
              target="_blank"
              rel="noreferrer"
              className="contact-tile"
            >
              <div className="tile-icon green">
                <MessageCircle size={20} />
              </div>
              <div>
                <p>WhatsApp</p>
                <strong>Napisz wiadomość</strong>
              </div>
            </a>

            <div className="contact-tile">
              <div className="tile-icon blue">
                <MapPin size={20} />
              </div>
              <div>
                <p>Lokalizacja</p>
                <strong>{contact.location}</strong>
              </div>
            </div>
          </div>

          <button onClick={downloadVCard} className="download-button">
            <Download size={20} />
            Dodaj do kontaktów
          </button>

          <div className="benefits">
            <h3>Dlaczego warto?</h3>
            <ul>
              {benefits.map((item) => (
                <li key={item}>
                  <CheckCircle size={24} />
                  <span>{item}</span>
                </li>
              ))}
            </ul>
          </div>

          <p className="footer">
            © {new Date().getFullYear()} Korepetycje z Angielskiego • Radomsko
          </p>
        </section>
      </motion.main>
    </div>
  );
}
