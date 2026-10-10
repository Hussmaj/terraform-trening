Tirsdag 01/09/2026

## Arbeids journal


### 1. Mål for dagen

Forstå konseptet Infrastructure as Code (IaC) og forskjellen på skyleverandører (AWS/Azure) og automasjonsverktøy (Terraform).
Sette opp et fungerende utviklingsmiljø med Terraform på egen maskin.
Gjennomføre en komplett livssyklus (opprette, endre, slette) for en lokal ressurs ved hjelp av Terraform-kode.
Rulle ut en ekte, virtuell server (EC2-instans) i AWS via kode.


### 2. Utført arbeid & Framgang

**Miljø oppsett:**

Installert Terraform CLI (v1.16.0) i WSL. Løst en nettverksblokkering (Error 429) ved å hente GPG-nøkler med "curl" i stedet for "wget".

**Lokal testing:**

Skrev en main.tf-fil som opprettet en lokal fil med Terraform. Testet også hvordan man kan endre filinnholdet med flerlinsjesyntaks (<<EOT), og lærte hvordan Terraform erstatter ressurser når konfigurasjonen endres.

**AWS-integrasjon og feilsøking:**

Koblet terminalen til AWS ved hjelp av miljøvariabler for tilgangsnøkler. Endret Terraform-koden for å opprette en EC2-instans i AWS-regionen Stockholm (eu-north-1).

**Feilsøking:**  

Rettet feil knyttet til en ugyldig AMI-ID ved å oppdatere til en gyldig Ubuntu 24.04 LTS-versjon.   
Jeg løste også tilgangsproblemer i AWS IAM ved å oppdatere nødvendige rettigheter.

**Oppsett av skyserver:**   

Etter at feilene var rettet, kjørte koden som forventet, og jeg fikk opprettet en skyserver i AWS.  

### 3. Viktige verktøy og kommandoer lært i dag

terraform init: Klargjør mappen og laster ned plugins/providers.  
terraform plan: Viser en trygg forhåndsvisning av hva koden vil gjøre.  
terraform apply: Utfører koden og bygger infrastrukturen i praksis.  
terraform destroy: Sletter alt koden har bygget og stopper eventuelle kostnader.  
terraform.tfstate: Lært at dette er "hjernen" (state-filen) til Terraform som man aldri må slette manuelt.  

## 4. Veien videre / Neste steg

Koble WSL-terminalen opp mot en ekte AWS-konto ved hjelp av miljøvariabler for Access Keys (AWS_ACCESS_KEY_ID og AWS_SECRET_ACCESS_KEY).  
Gjøre om main.tf fra å lage en lokal tekstfil til å rulle ut en ekte, virtuell Linux-server (EC2-instans) i AWS sitt datasenter i Stockholm.  

Sammendrag:
Jeg har installert og lært det grunnleggende i Terraform gjennom WSL-terminalen. Jeg har også jobbet med å skrive og endre HCL-kode, feilsøke og rette tilgangsrettigheter i AWS IAM, samt sette opp og rydde opp etter en skyserver.
