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

