# Contador Binario con Flip-Flops JK: `00`->`10`->`10`

**Diagrama esquemático**

![image](https://github.com/user-attachments/assets/b9b501ad-5679-484e-a722-3b6baec08cd8)

**Simulación en Thinkercad**

![Contador de 00-01-10](https://github.com/user-attachments/assets/6ea3cf1a-6e6f-427b-b48b-403c4c3e2663)

*Enlace a la simulación:* [https://www.tinkercad.com/things/8zLiOy1rFmA-contador-de-00-01-10](https://www.tinkercad.com/things/8zLiOy1rFmA-contador-de-00-01-10)

**Tabla de verdad**

| SW | E1 | E0 | ES1 | ES0 |
|----|----|----|----|----|
| 0  | 0  | 0  | 0  | 0  |
| 0  | 0  | 1  | 0  | 0  |
| 0  | 1  | 0  | 0  | 0  |
| 0  | 1  | 1  | 0  | 0  |
| 1  | 0  | 0  | 0  | 1  |
| 1  | 0  | 1  | 1  | 0  |
| 1  | 1  | 0  | 0  | 0  |
| 1  | 1  | 1  | 0  | 0  |

## Estados para los flip-flops JK

| SW | E1 | E0 | ES1 | ES0 | J1 | K1 | J0 | K0 |
|----|----|----|----|----|----|----|----|----|
| 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  |
| 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| 0  | 1  | 1  | 0  | 0  | 0  | 0  | 0  | 0  |
| 1  | 0  | 0  | 0  | 1  | 0  | x  | 1  | x  |
| 1  | 0  | 1  | 1  | 0  | 1  | x  | x  | 1  |
| 1  | 1  | 0  | 0  | 0  | x  | 1  | 0  | x  |
| 1  | 1  | 1  | 0  | 0  | x  | x  | x  | x  |

**Mapas de Karnaugh**

### **J1**

| SW \ E1E0 | 00 | 01 | 11 | 10 |
|-----------|----|----|----|----|
| 0         |  0 |  0 |  0 |  0 |
| 1         |  0 |  1 |  x |  x |

SW E1 E0 + SW E1’ E0 

SW E0 (E1+E1’) 

SW E0 

### **K1**

| SW \ E1E0 | 00 | 01 | 11 | 10 |
|-----------|----|----|----|----|
| 0         |  0 |  0 |  0 |  0 |
| 1         |  1 |  1 |  x |  x |

SW E1 E0’ + SW E1 E0 + SW E1’ E0’ + SW E1’ E0 

SW E1 (E0’+E0) + SW E1’ (E0’+E0) 

SW (E1+E1’) 

SW 

### **J0**

| SW \ E1E0 | 00 | 01 | 11 | 10 |
|-----------|----|----|----|----|
| 0         |  0 |  0 |  0 |  0 |
| 1         |  1 |  x |  x |  0 |

SW E1 E0' + SW E1’ E0' 

SW E0’ (E1+E1’) 

SW E0’ 


### **K0**

| SW \ E1E0 | 00 | 01 | 11 | 10 |
|-----------|----|----|----|----|
| 0         |  0 |  0 |  0 |  0 |
| 1         |  1 |  1 |  x |  x |

SW E1 E0’ + SW E1 E0 + SW E1’ E0’ + SW E1’ E0 

SW E1 (E0’+E0) + SW E1’ (E0’+E0) 

SW (E1+E1’) 

SW 


