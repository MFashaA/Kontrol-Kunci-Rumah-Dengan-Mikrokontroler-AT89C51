# Kontrol-Kunci-Rumah-Dengan-Mikrokontroler-AT89C51

ORG 00H
MOV P0,#00000001B
baca_tombol : MOV A,P0
RRC A
JC lanjut
SETB P2.0
SETB P2.1
SETB P2.2
SETB P2.3
SETB P2.4
SETB P2.5
SETB P2.6
SETB P2.7

SJMP baca_tombol
lanjut : RRC A         
JC baca_tombol
CLR P2.0
CLR P2.1
CLR P2.2
CLR P2.3
CLR P2.4
CLR P2.5
CLR P2.6
CLR P2.7

SJMP baca_tombol
END
