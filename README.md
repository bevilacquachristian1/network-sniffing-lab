Network Sniffing Lab - HTTP e HTTPS

Obiettivo
Analizzare il traffico di rete per evidenziare le differenze tra protocollo HTTP e HTTPS utilizzando Wireshark e InetSim.


Tecnologie utilizzate
- Kali Linux
- Windows 10
- Wireshark
- InetSim


Configurazione
- Rete configurata manualmente:
  - Kali: 192.168.32.100
  - Windows: 192.168.32.101
- DNS e file `hosts` modificato per risolvere: 


 Analisi traffico

HTTP
- Protocollo: HTTP 
- Contenuto visibile:
- GET / HTTP/1.1
- Host: epicode.internal
- User-Agent, Accept, ecc.
- I dati sono in chiaro

Questo significa che chi sniffa la rete può leggere tutto.


 HTTPS
- Protocollo: TLS 1.3
- Contenuto:
- Client Hello
- Server Hello
- Application Data (criptata)

I dati NON sono leggibili → sono cifrati


 Differenza chiave

| HTTP | HTTPS |

| Dati in chiaro | Dati criptati |
| Leggibile con Wireshark | Non leggibile |
| Nessuna sicurezza | Sicuro |



 Conclusione
HTTPS protegge i dati grazie alla cifratura TLS, impedendo l’intercettazione e la lettura delle informazioni sensibili durante la trasmissione.


