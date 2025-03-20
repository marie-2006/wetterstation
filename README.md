## Wetterstation

Eine Wetterstation mit Arduino + BME208 und  LC-Display

```

   ---------------------------------
  |                                 |
  |                                 |
  |        4x20 LC-Display          |
  |                                 |
  |                                 |
  | D7 D6 D5 D4         Bl En RW RS |
   ---------------------------------
    |  |  |  |          |  |  |  |
    |  |  |  |          |  |  |  |
    |  |  |  |          |  |  |  |
    |  |  |  |          |  |  |  |
    |  |  |  |          |  |  |  |
    |  |  |  |          |  |  |  |
   ---------------------------------                    -------------------------
  | D7 D6 D5 D4         D3 D2 D1 D0 |             SDA  |                         |
  |                             SDA | -----+---------- | Port Bx                 |
  |           Port-Expander         |      |      SCL  |         Arduino         |
  |                             SCL | -----|---+-------| Port Bx                 |
  |                                 |      |   |       |                         |
   ---------------------------------       |   |        -------------------------
                                           |   |
                                           |   |
                                           |   |
   ---------------------------------       |   |
  |                                 |      |   |
  |                             SDA | -----+   |
  |            Tiny RTC             |      |   |
  |                             SCL | -----|---+
  |                                 |      |   |
   ---------------------------------       |   |
                                           |   |
                                           |   |
                                           |   |
   ---------------------------------       |   |
  |                                 |      |   |
  |                             SDA | -----    |
  |              BME280             |          |
  |                             SCL | ---------
  |                                 |
   ---------------------------------

   
```

**Anzeigen von Uhrzeit** - Die Uhrzeit wird beim Start aus dem Tiny-RTC Modul ausgelesen und dann im Controller weitergerechnet.
   
