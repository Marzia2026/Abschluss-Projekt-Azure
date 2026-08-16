# Azure Abschlussprojekt

## Projektübersicht

In diesem Abschlussprojekt wurde eine vollständige Cloud-Infrastruktur in **Microsoft Azure** aufgebaut, konfiguriert, abgesichert und überwacht.

Dabei wurden verschiedene Azure-Dienste eingesetzt, darunter **Microsoft Entra ID, Virtual Networks, Network Security Groups, Virtual Machines, Azure Storage, Azure SQL Database, Azure Backup, Azure Monitor, Microsoft Defender for Cloud, Azure Policy und App Service**.

Die einzelnen Arbeitsschritte wurden durch Screenshots dokumentiert und im Repository abgelegt.
## 0A1 – Azure Pricing & Kostenoptimierung

In diesem Abschnitt wurde mit dem **Azure Pricing Calculator** untersucht, wie sich die Kosten einer Azure-Umgebung verändern. Dabei wurde deutlich, dass der Preis unter anderem von der **Region, der VM-Größe und dem VM-Typ, dem Betriebssystem, der Disk-Größe und dem Storage-Typ** abhängt. Eine größere VM oder eine andere Region kann beispielsweise zu deutlich höheren monatlichen Kosten führen.

Anschließend wurde die ursprüngliche Konfiguration mit einer günstigeren **Alternative** verglichen. Durch die Auswahl einer passenden Region, einer angemessenen VM-Größe, eines geeigneten Storage-Typs und einer optimierten Laufzeit können die Kosten reduziert werden, ohne die benötigte Funktionalität wesentlich zu beeinträchtigen.
**Screenshots:**

- `0A1-allprice.png 
- `0A1-price-Alternative.png`
- `0A1-priceCalculating.png`
- `0A1-VMnewprice.png`
- `0A1-allprice.png`

---

## A – Identity & Access Management

### A1 – Microsoft Entra ID
- Benutzer und Identitäten in **Microsoft Entra ID** verwaltet.
- Die vorhandenen Benutzerkonten überprüft und dokumentiert.

### A3 – Security Admin Group
- Eine Sicherheits-/Administratoren-Gruppe eingerichtet.
- Benutzer bzw. Administratoren entsprechend organisiert.

### A4 – Role-Based Access Control (RBAC)
- Berechtigungen über **Azure RBAC** umgesetzt.
- Rollen und Zugriffsrechte entsprechend dem Prinzip der minimalen Berechtigung konfiguriert.

**Screenshots:**
- `A-A2-EntraUsers.png`
- `A-A3-SecurityAdminGroup.png`
- `A-A4-RBC-IAM.png`

---

## B – Netzwerk

### B1 – Virtual Networks & Network Security Groups

- Azure Virtual Networks erstellt und konfiguriert.
- Netzwerkstruktur für die verwendeten Ressourcen aufgebaut.
- **Network Security Groups (NSG)** eingerichtet.
- Eingehende und ausgehende Regeln definiert.
- Netzwerkzugriffe entsprechend den Anforderungen eingeschränkt.

### B2 – VNet Peering

- Verbindung zwischen Virtual Networks über **VNet Peering** eingerichtet.
- Peering-Konfiguration überprüft.
- Status der Verbindung kontrolliert.

**Screenshots:**
- `B-B1-VNETS.png`
- `B-B1-NSG-Rules.png`
- `B-B1-NSG-Rules-Data.png`
- `B-B2-Peering2.png`
- `B-B2-PeeringStatus.png`

---

## C – Virtual Machines

### C1 – VM Deployment & Connectivity

- Azure Virtual Machines bereitgestellt.
- VM-Status und laufende Ressourcen überprüft.
- Zugriff auf Linux-VMs über **SSH** getestet.
- Netzwerkverbindung zwischen den VMs überprüft.
- Eine Anwendung auf einer VM ausgeführt und deren Erreichbarkeit kontrolliert.

**Screenshots:**
- `C-C1-VM-Runnings.png`
- `C-C1-VM-APP-Running.png`
- `C-C1-VM-ssh-succeed.png`
- `C-C1-VM-Data01-SSh-Success.png`
- `C-C1-AddPing.png`

---

## D – Blob Storage

### D1 / D2 – Azure Blob Storage

- Einen Azure Storage Account bzw. Blob Storage eingerichtet.
- Container erstellt und Dateien hochgeladen.
- Zugriff auf Blob-Dateien über eine **SAS-URL** getestet.
- Die Berechtigungen und den Zugriff auf die gespeicherten Dateien überprüft.

**Screenshots:**
- `D-D1-BLOB-SAS-URL (2).png`
- `D-d2-blob-container-files.png`

---

## E – Azure File Share

### E1 / E2 – File Share

- Azure File Share eingerichtet.
- Dateien innerhalb der Freigabe erstellt und verwaltet.
- Zugriff auf die Dateien über das Azure Portal überprüft.
- Die Azure File Share auf einem System als Laufwerk eingebunden.
- Schreib-/Lesezugriff erfolgreich getestet.

**Screenshots:**
- `E-E1-Fileshare-files.png`
- `E-E2-Freigabe.png`
- `E-E2-mounted-DRIVE.png`
- `E-E2-portal-Newfile.png`

---

## F – Azure SQL Database

### F1 – SQL Database

- Eine **Azure SQL Database** eingerichtet.
- Datenbank und SQL-Ressourcen überprüft.
- SQL-Abfragen ausgeführt.
- Die erfolgreiche Verbindung und Funktionalität der Datenbank dokumentiert.

**Screenshots:**
- `F-f1.png`
- `F-F1-sqldb-overview.png`
- `F-F1-sqlqeuery.png`

---

## G – Backup & Recovery

### G1 – Recovery Services Vault

- Einen **Recovery Services Vault** eingerichtet.
- Lokale Redundanz (**LRS**) für die Backup-Infrastruktur verwendet.

### G2 / G3 – VM Backup

- Backup einer Azure VM konfiguriert.
- Eine Backup Policy erstellt.
- Sicherungsintervalle und Aufbewahrung entsprechend der Anforderungen definiert.
- Einen erfolgreichen Backup Job überprüft.

### G4 – File Share Backup

- Backup für eine Azure File Share eingerichtet.
- Backup-Konfiguration und Sicherungsstatus überprüft.

**Screenshots:**
- `G-G1-Vault-LRS.png`
- `G-G2-backuppolicy.png`
- `G-G2-backuppolicy1.png`
- `G-G2-VMbackup.png`
- `G-G3-VM.Backup-job.png`
- `G-G4-fileshare-backup.png`

---

## H – Monitoring & Kostenkontrolle

### H1 – Azure Monitor & Log Analytics

- **Log Analytics Workspace** eingerichtet bzw. verbunden.
- Monitoring-Daten gesammelt und überprüft.
- Eine CPU-basierte Alert Rule für eine VM erstellt.

### H2 – Budget Alert

- Ein Azure Budget eingerichtet.
- Kostenüberwachung aktiviert.
- Ein Budget Alert zur frühzeitigen Erkennung steigender Kosten konfiguriert.

**Screenshots:**
- `H-H1-LogAnalytics-connected.png`
- `H-H1-Alert-rule-CPU.png`
- `H-H2-Budget.Alert.png`

---

## I – Security & Governance

### I1 – Microsoft Defender for Cloud

- Sicherheitsstatus der Azure-Umgebung überprüft.
- **Secure Score** analysiert.
- Security Recommendations überprüft und gefiltert.
- Sicherheitsverbesserungen identifiziert.

### I2 – Azure Policy

- Eine Azure Policy erstellt bzw. zugewiesen.
- Die Policy auf Ressourcen angewendet.
- Einen Test mit einer nicht erlaubten Ressourcenkonfiguration durchgeführt.
- Die erfolgreiche Policy-Verweigerung dokumentiert.

**Screenshots:**
- `I-I1-Secure-Score.png`
- `I-I1-Recommendations.filter.png`
- `I-I1-Recommendations.filtering.png`
- `I-I2-policyassignment.png`
- `I-i2-policytest-denied.png`
- `I-I2-AppService.png`

---

## J – App Service

### J1 – Web App

- Einen Azure **App Service** erstellt und konfiguriert.
- Eine Webanwendung bereitgestellt.
- Die laufende Webanwendung über den Browser getestet.
- Die erfolgreiche Erreichbarkeit der Anwendung dokumentiert.

**Screenshots:**
- `J-J1-2.png`
- `J-J1-WebAppRunning.png`

---

## K – Logging & PowerShell

### K1 – Azure Logs

- Azure-Ressourcen und deren Logs überprüft.
- Logs über das Azure Portal analysiert.
- Zusätzlich über **Azure Cloud Shell / PowerShell** auf Logs zugegriffen.

### K2 – VM Status

- Den Status der Azure VM über die Azure-Umgebung überprüft.
- Der laufende Zustand der VM wurde dokumentiert.

**Screenshots:**
- `K-K1-logs auf portal.png`
- `K-K1_CloudShell_PowerShell_Logs.png`
- `K-K2-VM-statusRunning.png`

---

## Bonus – Azure Architecture

### Bonus – Architecture

- Die Azure-Infrastruktur und die verwendeten Komponenten als Architektur betrachtet bzw. dokumentiert.
- Die Verbindung zwischen Netzwerk, Compute, Storage, Datenbank, Security, Monitoring und Backup berücksichtigt.

**Screenshot:**
- `Bonus-Arc.png`

---

# Zusammenfassung

Im Rahmen des Projekts wurde eine umfangreiche Azure-Umgebung aufgebaut und praktisch umgesetzt.

Dabei wurden folgende zentrale Bereiche abgedeckt:

- **Identity & Access Management**
- **Netzwerk und Netzwerksicherheit**
- **Virtual Machines**
- **Blob Storage**
- **Azure File Share**
- **Azure SQL Database**
- **Backup & Recovery**
- **Monitoring und Logging**
- **Kostenkontrolle**
- **Microsoft Defender for Cloud**
- **Azure Policy & Governance**
- **Azure App Service**
- **PowerShell / Cloud Shell**
- **Azure Architecture**

Die einzelnen Konfigurationen und Funktionstests wurden durch Screenshots dokumentiert und im Repository unter `Abschluss Projekt-Screens` abgelegt.

Damit bildet das Projekt einen praktischen Überblick über die Planung, Implementierung, Absicherung, Überwachung und Verwaltung einer Azure-Cloud-Umgebung.