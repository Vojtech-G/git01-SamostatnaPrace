# Git a Vagrant – první Linux server

![Moje virtuální Linuxová laboratoř](./Images/muj-linux-server.png)

Úvodní samostatná práce z předmětu Operační systémy (OSY) pro 3. I na SPOŠ Dvůr Králové nad Labem.

Vyberte si Linuxovou distribuci a pomocí Vagrantu si připravte vlastní virtuální server. Jeho konfiguraci uložte do svého repozitáře na GitHubu, abyste prostředí mohli znovu vytvořit i na jiném počítači.

## Moje řešení

**Distribuce a verze:** Debian GNU/Linux 13 (trixie)

**Použitý Vagrant box:** bento/debian-13

**Adresář serveru:** srv01

**Výsledek spuštění a přihlášení:**
Server se úspěšně spustil příkazem `vagrant up` – při prvním spuštění se stáhl box `bento/debian-13`.
`vagrant status` ukazuje server jako running, přihlášení `vagrant ssh` funguje.
Distribuce ověřena příkazem `cat /etc/os-release`.

**Případné problémy a jejich řešení:**
První spuštění trvalo déle kvůli stažení boxu. Jinak bez problémů.

**Kontrolní kód a záznam ze serveru:**

**Kontrolní kód:** `SPOS-3I-3672a224b021166378eb61cc2e0b2c236bc47b8cf186d5794a7d9e6e2018436b`

```text
Úloha: git-vagrant / SPOŠ / 3. I / v1
Distribuce: Debian GNU/Linux 13 (trixie)
Hostname: debian13
Kernel: 6.12.48+deb13-amd64
Virtualizace: oracle
Čas UTC: 2026-09-25T06:23:48Z
Náhodné ID: 354bf045-5081-48fa-9957-46e1fb209b89
```

**Bonus – AI obrázek a použitý prompt:**
Obrázek: `Images/muj-linux-server.png`
Nástroj: perchance.org AI text-to-image generator
Prompt: *"A futuristic home lab with virtual Linux servers running on Vagrant boxes, Git branches and terminal windows floating in the background, dark cyberpunk style"*

## Očekávaná struktura

```text
.
├── README.md
├── .gitignore
├── overeni-serveru.sh
├── LICENSE
├── Vagrant
├── Images/
│   └── muj-linux-server.png
└── srv01/
    └── Vagrantfile
```

Adresář `srv01/.vagrant/` vznikne pouze lokálně při práci s Vagrantem a nebude součástí odevzdaného repozitáře.

## Kontrola před odevzdáním

- [x] Mám vlastní adresář serveru a v něm správně pojmenovaný Vagrantfile.
- [x] Vybral/a jsem Linuxovou distribuci ze vzorů ročníkového projektu.
- [x] Server se spustí a mohu se do něj přihlásit pomocí `vagrant ssh`.
- [x] .gitignore vylučuje `.vagrant/` a žádné soubory z něj nejsou sledované Gitem.
- [x] Na serveru jsem spustil/a ověřovací skript a vložil/a kód i celý záznam do části Moje řešení.
- [x] Doplnil/a jsem část Moje řešení a odeslal/a změny do svého GitHub repozitáře `git01-...`.