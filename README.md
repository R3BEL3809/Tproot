# Tproot (DockerLabs)

**IP:** 172.122.0.2

**Dificultad:** Muy Fácil

**Vector:** vsFTPd 2.3.4 backdoor -> root directo

---

## INFO 

### Descubrir el host

```bash
nmap -sS -p- -sV -O --open --min-rate 5000 -n -oN scan 172.17.0.2
```

image

| PUERTO | SERVICIO |
| ------ | -------- |
| 21     | FTP      |
| 80     | HTTP     |

### Enumeración web

Acceso al puerto 80: Es un apache2 sin contenido. 

Fuzzing de directorios sin resultados:

```
dirb http://172.17.0.2

gobuster dir -u http://172.17.0.2 -w /usr/share/wordlists/seclists/Discovery/Web-Content/raft-medium-directories.txt -x php,html,xml,txt

gobuster dir -u http://172.17.0.2 -w /usr/share/wordlists/seclists/Discovery/Web-Content/DirBuster-2007_directory-list-2.3-medium.txt -x php,html,xml,txt,py

```

