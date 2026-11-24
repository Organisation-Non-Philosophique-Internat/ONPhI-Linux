# ONPhI Linux


> **ROBUR TUTI LIGAS,**
> **SANAS,**
> **SAGIL IT UT RUBOR**


*Un poste de travail technique, sûr dès la conception, entièrement en français, avec une identité visuelle à lui.*

---

## En quelques mots

ONPhI GNU/Linux est une distribution construite sur **Debian 13 « trixie »** (branche stable). Elle s'adresse à un **public restreint** : des personnes qui veulent, sur une seule machine, un bureau soigné et cohérent **et** une boîte à outils complète pour la maintenance, la sécurité, l'analyse, le réseau, la surveillance du système, les médias et l'intelligence artificielle locale.

Trois idées la guident :

1. **Un bureau qui a une identité.** Une charte graphique unique (crème et brun), un logo, un petit danseur qui anime le démarrage, l'ouverture de session et l'économiseur d'écran, des sons et des notifications faits pour l'ensemble.
2. **Des outils techniques à portée de main**, rangés dans un menu Applications en français, par familles.
3. **La sécurité dès la conception** : chiffrement du disque, Secure Boot, pare-feu actif, confinement des programmes, aucune télémétrie, aucune dépendance à un site web.

---

## L'expérience ONPhI

### Du démarrage au bureau

| Moment | Ce qu'on voit |
| --- | --- |
| **GRUB** | le logo ONPhI, fixe, sur un écran aux couleurs de la charte |
| **Démarrage (Plymouth)** | le b-boy du logo qui danse pendant le chargement du système |
| **Connexion (LightDM)** | un écran de connexion aux couleurs ONPhI |
| **Ouverture de session** | le petit bonhomme entre par la droite en dansant, sabre en main, puis se pose sous la croix du logo ; le bureau apparaît derrière lui |
| **Économiseur d'écran** | le bonhomme, clair sur fond sombre, quitte sa place, se promène le long de sa ligne de sol, danse quelques pas à chaque halte, puis revient ; l'écran s'éteint au bout de 10 minutes ; verrou par xsecurelock, sans MATE |

Le fond d'écran porte, en trois lignes au-dessus du logo, le palindrome latin **ROBUR TUTI LIGAS, / SANAS, / SAGIL IT UT RUBOR**.

### Un bureau repensé

- **Bureau ONPhI, sans MATE** (depuis 1.8.0) : la session `onphi-session` réunit des pièces légères — xfwm4 pour les fenêtres, xfsettingsd pour le thème et les raccourcis, xfce4-power-manager pour l'énergie — et les programmes ONPhI : `onphi-bureau` (fond et icônes) et `onphi-barre`, deux barres écrites pour ONPhI (menus, lanceurs, recherche, bouton du son bien visible, horloge et fuseaux ; fenêtres et bureaux en bas). **Réglages ONPhI** réunit tous les réglages ; **Quitter** propose veille, redémarrage, arrêt.
- **Sans Caja** : le bureau est assuré par `onphi-bureau`, un programme ONPhI qui affiche les icônes (Ordinateur, Dossier personnel, Réseau, Corbeille, clés USB, contenu du dossier Bureau), gère le clic droit, le glisser-déposer et le montage automatique des disques amovibles.
- **Titi** comme gestionnaire de fichiers : tout dossier, d'où qu'on l'ouvre, s'ouvre dans Titi (deux panneaux, un terminal sous chacun, assistant IA).
- **Thème complet** : fenêtres, GTK, applications Qt/KDE, icônes de dossiers et de menus dessinées à partir de Font Awesome.
- **Mode clair et mode sombre** : la même charte en deux tons (crème et brun, ou brun nuit et crème). Un seul geste — menu Système, Réglages ONPhI ou `onphi-apparence` — change les fenêtres, les barres, les icônes, le fond d'écran, les applications Qt, le terminal et Conky.
- **Barre du haut** avec les menus Applications et Dossiers, les lanceurs, un champ de recherche au centre (Super+S), un menu Système et le bouton Éteindre. L'horloge ouvre le calendrier et les fuseaux (Paris, UTC, outre-mer, et ceux qu'on ajoute dans **Horloge**).
- **Menu Applications en français**, réorganisé : catégories habituelles (Accessoires, Bureautique, Internet…) et familles d'outils au premier niveau, trois niveaux de sous-menus au plus.

### Notifications et sons

- **`onphi-notifications`** remplace le démon de notifications : bulles aux couleurs ONPhI, historique conservé, panneau latéral avec notifications groupées par application, « Tout effacer » et mode **Ne pas déranger**.
- **Fenêtres** : elles se superposent sur le même bureau. On peut les aimanter en moitiés, quarts et tiers (raccourcis et bords de l'écran, comme sur Pop!_OS) puis les rendre flottantes. La transparence de la fenêtre active se règle (Super+O) et se mémorise par application. Marco compose l'écran ; picom n'est pas installé.
- **`onphi-sounds`** synthétise un thème sonore cohérent, en deux styles : **Jungle** (breakbeat des années 1990, par défaut) et **Doux** (notes boisées façon marimba).

### Réf/Aide : la documentation intégrée

**Réf/Aide** est l'aide d'ONPhI : une application locale, **sans navigateur et sans connexion internet**, entièrement en français.

- Un **Guide** pour apprendre le bureau : bureau, fichiers, barre du haut, raccourcis, notifications, session, apparence, maintenance.
- Une **Référence** pour aller plus loin : commandes ONPhI, scripts, emplacement des fichiers système, terminal, dépannage.
- Recherche dans tout le texte (Ctrl+F, insensible aux accents), boutons **Copier** sur chaque exemple de commande, liens entre les pages.
- Ouverture par la première ligne du menu Applications (à gauche), le menu Système, le raccourci **Super+F1** ou la commande `onphi-aide`.

### Surveillance du système en direct

Un **Conky** configuré pour ONPhI affiche sur le bureau, en transparence et sur plusieurs écrans si besoin : système, stockage, réseau, services, activité, état de Tor, état des outils d'IA et processus. Les flux se distinguent par la couleur : reçu en sarcelle, envoyé en terre cuite, lecture disque en acier, écriture disque en or.

---

## La boîte à outils

ONPhI rassemble des outils regroupés en familles. Chaque famille est un méta-paquet (`onphi-multimedia`, `onphi-dessin`, `onphi-tor`, `onphi-osint`, `onphi-forensic`, `onphi-fichiers`, `onphi-maintenance`, `onphi-sauvegarde`, `onphi-reseau`, `onphi-mots-de-passe`, `onphi-distant`, `onphi-virtualisation`, `onphi-devops`, `onphi-disques`, `onphi-ingenierie`, `onphi-robotique`, `onphi-drones`, `onphi-ia`, `onphi-editeurs`, `onphi-securite`, `onphi-divers`, `onphi-developpement`). Le bureau `onphi-desktop` installe déjà le développement et les éditeurs Debian (`onphi-developpement`, `onphi-editeurs`). Les autres familles : `onphi-familles`, ou `sudo install-tech-tools` / `--section multimedia`. Les outils absents de Debian (Cursor, Claude, VirtualBox, Ollama, GNS3, ROS, stations sol de drones) restent lancés par le script, ou ne sont pas installés du tout quand aucun paquet Debian ne les fournit.

### Maintenance et matériel
Santé des disques (`smartmontools`, GSmartControl, `nvme-cli`), inventaire matériel (`inxi`, `lshw`, HardInfo), capteurs de température, bancs d'essai et tests de charge (`fio`, `stress-ng`, `memtester`), occupation du disque (`ncdu`, Baobab), recherche de doublons (dupeGuru, Czkawka, `fdupes`).

### Sauvegarde et instantanés
Clonage de disques (Clonezilla, `partclone`, Guymager), sauvegardes incrémentales et chiffrées (BorgBackup et Vorta, Restic, Duplicity, `rclone`, Grsync), instantanés du système (**Timeshift**, Snapper, btrbk).

### Disques, systèmes de fichiers et chiffrement
Partitionnement (GParted, `gdisk`), chiffrement (**LUKS/cryptsetup**, VeraCrypt, zuluCrypt, `fscrypt`), prise en charge étendue des systèmes de fichiers (btrfs, ZFS, XFS, exFAT, NTFS, APFS en lecture, BitLocker via `dislocker`…), effacement sécurisé (`nwipe`, `secure-delete`, BleachBit).

### Récupération de données et analyse forensique
- **Récupération** : TestDisk/PhotoRec, `ddrescue`, Foremost, Scalpel, `ext4magic`.
- **Acquisition** : images disque vérifiées (`dc3dd`, Guymager, formats EWF/AFF), empreintes (`hashdeep`, `ssdeep`).
- **Analyse** : The Sleuth Kit et Autopsy, Plaso (super-chronologie), RegRipper, lecteurs d'artefacts Windows (`chntpw`, `pff-tools`).
- **Fichiers suspects** : YARA, `binwalk`, GDB, outils de stéganographie (steghide, StegoSuite, OutGuess).
Famille `onphi-forensic` : `sudo install-tech-tools --section forensic`. Volatility, Bulk Extractor, radare2 et Ghidra ne sont pas dans Debian 13.

### Disques, gravure et récupération
Famille `onphi-disques` : Brasero et Xfburn pour graver, Sound Juicer, Asunder et cdparanoia pour un CD audio, `dvdbackup` et `vobcopy` pour copier les fichiers d'un DVD, dvdisaster, ddrescue et TestDisk pour un support abîmé, fdutils et Greaseweazle pour une disquette. `sudo install-tech-tools --section disques`. Le contournement CSS des DVD du commerce n'est pas installé.

### Réseau
- **Diagnostic** : DNS, DHCP, IP, `mtr`, `traceroute`, `ethtool`.
- **Surveillance du trafic** : Wireshark/`tshark`, `tcpdump`, `iftop`, `nethogs`, `vnstat`, `bmon`.
- **Cartographie et audit** : `nmap`, `masscan`, `arp-scan`, `netdiscover`, `mitmproxy`, Bettercap.
- **TLS** : `testssl.sh`, `sslscan`, `sslyze`.
- **Wi-Fi** : `wavemon`, LinSSID, Kismet, suite Aircrack-ng.
- **VPN** : WireGuard, OpenVPN, OpenConnect, OpenFortiVPN (intégrés à NetworkManager).
- **Console série** et laboratoire réseau **GNS3**.

### Audit de mots de passe
John the Ripper, Hashcat, Hydra, Ophcrack, outils de récupération pour archives, PDF et volumes LUKS — pour tester la solidité de ses propres mots de passe ou récupérer l'accès à ses propres données. Gestion des secrets au quotidien avec **KeePassXC**.

### Renseignement en sources ouvertes (OSINT)
Famille `onphi-osint`. Dans Debian : ExifTool et `mat2` (lire ou effacer les métadonnées), Sherlock (pseudonymes), dnsrecon, sublist3r et Recon-ng (domaines), whatweb (pages publiques). Maigret, Holehe, Amass, theHarvester, SpiderFoot et PhoneInfoga s'ajoutent avec `sudo install-tech-tools --section osint` : ils ne sont pas des paquets Debian.

### Confidentialité et anonymat
Tor, Tor Browser, `torsocks`, Nyx, et **onphi-anonsurf** (routage transparent de tout le trafic par Tor, nouvelle identité à la demande).

### Sécurité du poste
Pare-feu UFW et Gufw, Fail2ban, antivirus ClamAV (avec ClamTk), détection de rootkits (`rkhunter`, `chkrootkit`), audit et durcissement (**Lynis**, `auditd`, AIDE, `debsums`), confinement (AppArmor, Firejail).

### Accès distant
Remmina (RDP, VNC, SSH), FreeRDP, `sshfs`, ClusterSSH, `tmux`, FileZilla, `lftp`.

### Virtualisation
**virt-manager** (QEMU/KVM) est installé avec le bureau. La famille `onphi-virtualisation` ajoute GNOME Boxes, AQEMU, virt-viewer, libvirt, LXC, Docker et Podman. VirtualBox n'est pas dans Debian : `install-tech-tools --section virtualisation`. Les clients MariaDB, PostgreSQL, SQLite et Redis sont dans la même famille.

### DevOps
Famille `onphi-devops`, à part de la virtualisation : Ansible, Docker, Podman, Buildah, Skopeo, `kubectl`, les clients `gh` et `glab`, Vagrant et Distrobox. `sudo install-tech-tools --section devops` (alias `docker` ou `ansible`) ajoute aussi minikube et lazydocker. Helm, k9s et Terraform ne sont pas dans Debian 13.

### Ingénierie
Conception et fabrication fournies par Debian : FreeCAD, KiCad, LibreCAD, OpenSCAD, SolveSpace, QElectroTech, Fritzing, Octave, wxMaxima, Arduino, ngspice, GTKWave, PrusaSlicer, MeshLab, CloudCompare.

### Robotique
Arduino, terminaux série (CuteCom, GTKTerm, picocom) et vision (OpenCV). ROS n'est pas dans Debian 13 : la famille ne l'installe pas.

### Drones
Liaison série (CuteCom, Minicom, picocom) et vision (OpenCV) vers un contrôleur de vol. Les stations sol (QGroundControl, Mission Planner, Betaflight Configurator) ne sont pas dans Debian : la famille ne les installe pas.

### Intelligence artificielle locale
**Ollama** et `llama.cpp` pour faire tourner des modèles de langage sur la machine, Open WebUI comme interface, **Whisper** pour la transcription audio, Tesseract et OCRmyPDF pour la reconnaissance de texte (français et anglais), JupyterLab, outil `llm`, client Hugging Face, Claude Code.

### Médias et création
- **Lecture** : VLC, mpv, Celluloid, Audacious, Strawberry.
- **Vidéo** : Kdenlive, Shotcut, **OBS Studio**, HandBrake, MKVToolNix, LosslessCut, éditeurs de sous-titres.
- **Audio** : Audacity, Ardour, EasyEffects, Picard, conversion et extraction de CD.
- **Capture** : Flameshot, SimpleScreenRecorder, webcam.
- **Image et 3D** : GIMP, Inkscape, Krita, darktable, Blender, ImageMagick.
- Codecs complets (FFmpeg, GStreamer).

### Dessin au stylet
Famille `onphi-dessin`, à part du multimédia : Krita, MyPaint, GIMP, Inkscape, Xournal++, Drawing et Pencil2D. Ces programmes lisent la pression du stylet. La famille installe aussi le pilote de tablette (`xserver-xorg-input-wacom`, libwacom) : pression, gomme et boutons sur une tablette branchée. `sudo install-tech-tools --section dessin` (alias `graphisme` ou `stylet`).

### Développement et ligne de commande
Chaîne de compilation, Git et Git LFS, ShellCheck, `uv` pour Python ; outils en ligne de commande modernes : `ripgrep`, `fd`, `bat`, `fzf`, `eza`, `zoxide`, `btop`, `jq`, `tldr`.

### Éditeurs
À la demande (`sudo install-tech-tools --section editors`) : Neovim, Vim, Emacs, Helix, Kate, Geany, Kakoune, Micro, Meld, Code::Blocks, Qt Creator, GNOME Builder, Pluma, Joe, **VSCodium**, **Cursor**, **Claude Code**, et **Claude Desktop**. Les quatre derniers viennent de dépôts ou de paquets vérifiés en dehors de Debian ; ils ne font pas partie du dépôt local ONPhI.

> **Usage responsable.** Une partie de ces outils (audit de mots de passe, analyse réseau, OSINT) sert aussi bien à se défendre qu'à attaquer. Ils sont destinés à l'administration de ses propres systèmes, à la récupération de ses propres données, aux audits autorisés et à l'apprentissage. Leur usage contre des systèmes ou des personnes sans autorisation est illégal.

---

## La sécurité dès la conception

| Domaine | Ce que fait ONPhI |
| --- | --- |
| Démarrage | **Secure Boot** avec le `shim` et le GRUB signés de Debian, noyau Debian signé ; GRUB protégé par mot de passe pour l'édition des entrées |
| Disque | **chiffrement complet LUKS** proposé dès l'installation |
| Mises à jour | mises à jour de sécurité Debian automatiques ; **instantané du système avant chaque mise à jour**, pour pouvoir revenir en arrière |
| Pare-feu | actif dès l'installation, **tout entrant refusé** |
| Confinement | AppArmor actif avec les profils Debian |
| Comptes | pas de connexion root ; `sudo` avec mot de passe ; verrouillage automatique de l'écran |
| Vie privée | **aucune télémétrie** ; aucune adresse web dans l'interface ; aide entièrement locale |
| Logiciels | dépôts admis : Debian et ONPhI ; tout dépôt tiers est une décision explicite et documentée |
| Code ONPhI | programmes Python lancés en mode isolé, aucun appel au shell, aucun téléchargement à l'exécution |
| Intégrité | paquets ONPhI signés ; vérification que les fichiers de la charte n'ont pas été modifiés |

### Une charte verrouillée

L'identité ONPhI est **unique et protégée**, par niveaux :

1. aucun autre thème, fond ou jeu d'icônes n'est livré (la charte existe en deux tons, clair et sombre) ;
2. des règles apt empêchent l'installation des paquets concurrents (Caja, picom, autre démon de notifications…) ;
3. des verrous dconf fixent le thème, les icônes et le fond pour tous les comptes ;
4. un gardien d'intégrité vérifie les fichiers ONPhI ;
5. *(version 2)* système en lecture seule.

---

## Sous le capot

| Élément | Choix |
| --- | --- |
| Base | Debian 13 « trixie », stable |
| Matériel visé | machines récentes, UEFI, Secure Boot |
| Bureau | session ONPhI : xfwm4, xfsettingsd, xfce4-power-manager, `onphi-bureau`, `onphi-barre` ; Titi ; plus aucun paquet MATE |
| Connexion | LightDM |
| Système de fichiers | btrfs avec instantanés (Timeshift) |
| Son | PipeWire / WirePlumber |
| Réseau | NetworkManager |
| Réglages par défaut | xfconf (`/etc/xdg/onphi`) et schéma `fr.onphi.*` propres à la distribution |
| Langue | français |

### Programmes propres à ONPhI

| Programme | Rôle |
| --- | --- |
| `onphi-bureau` | le bureau sans Caja : icônes, clic droit, glisser-déposer, clés USB |
| `onphi-notifications` | bulles, historique, panneau latéral, Ne pas déranger |
| `onphi-fenetres` | transparence réglable, aimantation en portions d'écran, fenêtres superposées |
| `onphi-sounds` | thème sonore Jungle et Doux, synthétisé |
| `onphi-ouverture` | animation d'ouverture de session |
| `onphi-economiseur` | économiseur d'écran animé, sombre (au bout de 5 minutes, ou tout de suite au verrouillage) |
| `onphi-session` | la session : lance et relance fenêtres, réglages, énergie, bureau, barres, démarrage automatique |
| `onphi-barre` | barres du haut et du bas : menus, lanceurs, recherche, son, horloge, Système, Éteindre ; fenêtres et bureaux |
| `onphi-reglages`, `onphi-quitter` | Réglages ONPhI (Apparence, Matériel, Réseau, Système) ; fenêtre Quitter |
| `onphi-apparence` | mode clair ou mode sombre pour tout le bureau (`clair`, `sombre`, `bascule`) |
| `onphi-veille` | économiseur et verrou d'écran (xss-lock, xsecurelock) |
| Boutons des bureaux | un bouton par bureau dans la barre, avec une petite roue quand une fenêtre de ce bureau installe ou calcule |
| lxpolkit | demande du mot de passe administrateur ; le son est le bouton de la barre |
| `onphi-menu` | menu Applications en français, par familles d'outils ; la rubrique Outils ONPhI ne montre que ce qui est installé |
| `onphi-recherche` | champ de recherche au centre de la barre : fichiers, contenu, Réf/Aide, IA locale |
| `onphi-empreintes` | empreintes digitales pour la connexion, sudo et le déverrouillage |
| `onphi-applis` | applications installées : chercher et désinstaller |
| `onphi-mise-a-jour` | sources apt, interrogation et mise à jour |
| `onphi-capture` | photo d'écran et vidéo ; Super+Impr bascule l'enregistrement |
| `onphi-sim` | carte SIM : code PIN, APN ; connexion mobile allumée par défaut si un modem est présent |
| `onphi-mobile` | radio WWAN et connexion automatique au démarrage |
| `onphi-pare-feu` | UFW actif dès l'installation, tout entrant refusé |
| `onphi-correcteur` | orthographe et grammaire françaises, en local |
| `onphi-courriel` | SpamAssassin local et quarantaine (spam, hameçonnage, pièces jointes) |
| `onphi-horloge` | heure locale et fuseaux ; la même liste dans l'horloge de la barre |
| `onphi-aide` | Réf/Aide, documentation locale |
| `onphi-sauvegarde` | sauvegarde complète et vérifiée (sommes SHA-256) du travail ONPhI |
| `onphi-iso` | fabrique l'image d'installation ONPhI |

---

## Installer ONPhI

L'installation se fait à partir de l'image officielle **Debian 13 netinst**, transformée par `onphi-iso` en disque d'installation ONPhI, sans toucher à ses chargeurs signés (Secure Boot fonctionne tel quel) :

1. l'entrée **« Installer ONPhI »** installe Debian 13 en français ; restent à choisir le nom du compte, les mots de passe et le partitionnement (chiffrement conseillé) ;
2. à la fin, l'installateur installe le méta-paquet **`onphi-desktop`** depuis les paquets `.deb` embarqués sur le disque (`deb [trusted=yes] file:/var/lib/onphi/debs`). Le bureau, le thème, GRUB, Plymouth, les sons, le menu, Réf/Aide et Conky sont en place dès le premier démarrage ;
3. les outils techniques et les éditeurs se demandent ensuite : `sudo install-tech-tools` puis `sudo post-install-tech-tools`.

Une connexion internet est nécessaire pour les paquets Debian. Les paquets ONPhI ne viennent que du disque. Il n'y a pas encore de dépôt apt signé ni d'image live (live-build, Calamares).

GitHub Actions fabrique une pré-version d'essai de ce disque à chaque envoi sur `main` qui touche autre chose que la documentation, et la publie sous le nom `iso-essai-<version>`. On peut aussi la lancer à la main.

---

## Feuille de route

| Phase | Contenu | État |
| --- | --- | --- |
| 0. Mise en ordre | dépôt git, historique de la maquette, plan | fait |
| 1. Laboratoire | machine virtuelle Debian 13 de test | fait |
| 2. Premiers paquets | thème, icônes, images, réglages par défaut | fait (source `onphi`, paquets locaux) |
| 3. Session ONPhI | démarrage, ouverture, économiseur, bureau, notifications, sons, menus, aide en paquets | fait (méta-paquet `onphi-desktop`) |
| 4. Dépôt signé | clé GPG hors ligne, dépôt apt | à venir (le disque utilise un dépôt `file:` de confiance, sans signature) |
| 5. Image d'installation | live-build + Calamares, LUKS, btrfs | à venir (le disque actuel est le netinst Debian, avec les `.deb` locaux ; GitHub Actions en publie une pré-version d'essai depuis `main`) |
| 6. Sécurité et verrouillage | durcissement et charte verrouillée | à venir |
| 7. Compléments | recherche, menu qui suit les paquets, empreintes, applications installées, mises à jour, capture (Super+Impr ; la touche Impr reste la photo), carte SIM, correcteur français, dessin au stylet, familles ingénierie, robotique, drones, forensique, OSINT et DevOps. Restent l'explorateur de documents et la suite de l'assistant (certificats, portefeuille) | en cours |
| Plus tard | système en lecture seule, surcouche portable pour Gentoo, documentation et dépôt en ligne | — |

### Questions encore ouvertes

- Quelles familles d'outils livrer par défaut, et lesquelles proposer à la demande : chaque outil ajouté alourdit le système et agrandit la surface d'attaque.
- Quels dépôts tiers admettre, et comment le signaler à l'utilisateur.
- Nom définitif (« ONPhI GNU/Linux » ou « ONPhI Linux ») et numéro de la première version.
- Langues : français seulement en version 1 ?

---

*ONPhI GNU/Linux — document de présentation, novembre 2026. Projet en cours de développement : le contenu décrit à la fois ce qui existe déjà dans la maquette et ce qui est prévu pour la version 1.*

*Icônes Font Awesome Free, licence CC BY 4.0.*
