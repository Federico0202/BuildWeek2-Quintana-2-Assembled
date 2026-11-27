# 🛡️ Build Week 2: End-to-End Penetration Testing

## 📋 Descrizione del Progetto
Questo repository contiene la documentazione, gli script, gli exploit e i report tecnici sviluppati durante la **Build Week 2** del Master in Cybersecurity & Ethical Hacking di EPICODE. Il progetto simula un'attività completa di **End-to-End Penetration Testing** articolata su 5 giornate operative, coprendo vulnerabilità Web Application (SQL Injection, Stored XSS), Adversarial AI (LLM Exploitation), Buffer Overflow e post-exploitation su ambienti Linux e Windows.

---

## 🎯 Obiettivi e Attività Giornaliere

### 💉 Giorno 1 — Web Application Exploit: SQL Injection (SQLi)
* **Target:** Web Application DVWA (`192.168.13.150/24`) | **Attacker:** Kali Linux (`192.168.13.100/24`)
* **Difficoltà DVWA:** `LOW`
* **Obiettivo:** Sfruttare manualmente (senza tool automatici come `sqlmap`, ammesso solo Burp Suite Repeater) la vulnerabilità SQL Injection presente su DVWA per estrarre l'hash della password dell'utente **Pablo Picasso** e decifrarla per recuperarla in chiaro.
* **🚀 Bonus:**
  * Replicare l'attacco impostando il livello di difficoltà su `MEDIUM`.
  * Estrarre informazioni critiche da altri database collegati.
  * Redigere una guida illustrata step-by-step per permettere a un utente medio di replicare l'attacco.

### 🍪 Giorno 2 — Web Application Exploit: Stored Cross-Site Scripting (XSS)
* **Target:** Web Application DVWA (`192.168.104.150/24`) | **Attacker:** Kali Linux (`192.168.104.100/24`)
* **Difficoltà DVWA:** `LOW`
* **Obiettivo:** Sfruttare la vulnerabilità **XSS persistente** per simulare il furto di sessione (Session Hijacking) di un utente legittimo, inoltrando i cookie catturati verso un Web Server in ascolto su Kali Linux sulla porta `4444` e documentando la logica dello script utilizzato.
* **🚀 Extra Facoltativi:**
  * Replicare l'attacco impostando il livello di difficoltà su `MEDIUM`.
  * Effettuare il dump completo dei dati della vittima (cookie, versione browser, indirizzo IP, data).
  * Redigere una guida illustrata per replicare l'attacco.

### 🤖 Giorno 3 — Adversarial AI: LLM Exploitation
* **Obiettivo:** Progettare e sviluppare un bot in Python basato sull'API di **Google Gemini** contenente una vulnerabilità intenzionale scelta dalla **OWASP Top 10 for LLM Applications** (es. Prompt Injection / System Prompt Leakage).
* **Fasi operative:**
  * Dimostrare la falla tramite un exploit funzionante e documentarla in un file dedicato.
  * Condividere il codice sorgente con le altre squadre fornendo un indizio pubblico di massimo due righe.
  * Testare e compromettere i bot delle squadre avversarie interagendo esclusivamente via chat, senza leggere il loro codice sorgente.
* **🚀 Bonus (Buffer Overflow in C):**
  * Analizzare il comportamento di un programma C fornito prima dell'esecuzione.
  * Eseguire il codice in laboratorio e verificare le ipotesi formulate.
  * Modificare il sorgente per provocare un **Segmentation Fault** sfruttando la mancanza di controllo sull'input.
  * Implementare i controlli sull'input e creare un menù interattivo per selezionare la versione vulnerabile o quella corretta.

### 🐧 Giorno 4 — Exploit Linux con Metasploit (Metasploitable)
* **Target:** Metasploitable (`192.168.50.150`) | **Attacker:** Kali Linux (`192.168.50.100`) | **LPORT:** `5555`
* **Obiettivo:**
  * Eseguire un Vulnerability Scanning (`Basic Scan`) con **Nessus** sulla macchina target.
  * Sfruttare la vulnerabilità del servizio Samba attivo sulla porta `445/TCP` tramite `msfconsole` (modulo `exploit/multi/samba/usermap_script`).
  * Ottenere una shell remota e confermare la compromissione verificando la configurazione di rete tramite il comando `ifconfig`.

### 🪟 Giorno 5 — Exploit Windows con Metasploit
* **Target:** Windows 10 (`192.168.200.200`) | **Attacker:** Kali Linux (`192.168.200.100`) | **LPORT:** `7777`
* **Obiettivo:**
  * Avviare i servizi vulnerabili sulla macchina target ed eseguire una scansione con **Nessus**.
  * Sfruttare il servizio **Apache Tomcat** tramite Metasploit per ottenere una sessione **Meterpreter**.
  * Raccogliere le evidenze di post-exploitation:
    1. Determinare se il target è una macchina fisica o virtuale.
    2. Estrarre le impostazioni di rete della macchina compromessa.
    3. Verificare la presenza di webcam attive.
    4. Acquisire uno screenshot del desktop della vittima.
* **🚀 Bonus (CTF Black-Box):**
  * **Jangow 01 (Facile):** Compromissione completa ed escalation dei privilegi fino a `root` in modalità Black-Box pura (senza consultare walkthrough online).
  * **Empire Lupin One (Media):** Enumerazione avanzata e privilege escalation fino a `root` in modalità Black-Box pura.

---

## 🛠️ Strumenti e Tecnologie Utilizzate
* **Sistemi Operativi:** Kali Linux, Metasploitable 2, Windows 10
* **Penetration Testing & Exploitation:** Metasploit Framework (`msfconsole` / Meterpreter), Burp Suite (Repeater), Nessus
* **Sviluppo & AI:** Python, Google Gemini API, Linguaggio C
* **Analisi & Reporting:** Documentazione tecnica strutturata con evidenze, PoC (Proof of Concept) e remediation

---

## 👥 Team di Progetto e Contributi
La squadra **Quintana 2** ha collaborato alla realizzazione delle attività di penetration testing e alla stesura dei report tecnici suddividendo i compiti come segue:

* **Federico Capranica** (`@Federico0202`): *[Inserisci qui i file/attività specifiche svolte]*
* **[Nome Cognome Teammate 2]** (`@username`): *[Inserisci qui i file/attività specifiche svolte]*
* **[Nome Cognome Teammate 3]** (`@username`): *[Inserisci qui i file/attività specifiche svolte]*
* **[Nome Cognome Teammate 4]** (`@username`): *[Inserisci qui i file/attività specifiche svolte]*
* **Lavoro di Gruppo (Tutti):** Stesura del report tecnico finale di Build Week 2, raccolta delle evidenze e validazione degli exploit[cite: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10].  
