# parse_du_draw

online tool => https://dustinchen26.github.io/parse_ulbler_draw_upload

## Example
```
Please paste the whole du_stats_XXX.txt content below, then it will parse the DL/UL Tput, BLER, MCS.
formula 1: DL-BLER = DL-RETX / (DL-RETX + DL-TX)
formula 2: UL-BLER = UL-CRC-FAIL / (UL-CRC-SUCC + UL-CRC-FAIL)

【Input】
#############################################################################################
                       GNB DU Statistics  Fri Dec  8 11:26:26 2023
#############################################################################################

---------------------------------------------------------------------------------------------
                       UE Instantaneous Statistics
---------------------------------------------------------------------------------------------
UE-ID     BEAM-ID   CSIRS-PORT   PCELL-ID  DL-PKT-RX   DL-TPT    UL-PKT-TX UL-TPT    DL-LC-1   DL-LC-2   DL-LC-3   DL-LC-4   UL-LC-1   UL-LC-2   UL-LC-3   UL-LC-4   DL-PADDING  UL-PADDING  DL-PRB    UL-PRB    NUM-SR    NUM-BSR-TMR    SCELL-ACT-CE   TA-CE     NUM-TA-TMR   TA        
17037     0         0            1         10          0.0003    5055      1.5981    0.0005    0.0000    0.0000    0.0000    1.6016    0.0000    0.0000    0.0000    0.0002      9.3894      2         58        0         0              0              0         0            0         
17049     0         0            1         5117        1.6011    174       0.0100    1.6316    0.0000    0.0000    0.0000    0.0100    0.0000    0.0000    0.0000    0.0237      0.1011      36        22        387       0              0              0         0            0         

---------------------------------------------------------------------------------------------
                       UE MAC-Scheduler Instantaneous Statistics
---------------------------------------------------------------------------------------------
UE-ID   CELL-ID   ON-SUL   DL-TX   DL-RETX   ACK-TB[0] NACK-TB[0]  BLER-TB[0]  DTX-TB[0] ACK-TB[1] NACK-TB[1]  BLER-TB[1]  DTX-TB[1] DL-MCS  DL-RI-PER   DL-CQI-PER     UL-RX   UL-RETX  UL-CRC-SUCC   UL-CRC-FAIL   UL-CRC-DTX   UL-CQI  UL-MCS  UL-RI   NUM-BSR   SHR-BSR ST-BSR  LNG-BSR LT-BSR  NUM-CSI   NUM-SRS   
17037   1         0        10      0         10        0           0           0         0         0           0           0         9       1           8              17994   0        17994         0             0            10      9       0       17339     1074    0       16265   0       0         0         
17049   1         0        2676    46        2676      46          1           0         0         0           0           0         8       1           8              465     0        464           0             0            10      9       0       464       384     0       80      0       0         0         

【Output】
GNB DU Statistics  Fri Dec  8 11:26:26 2023
GNB DU Statistics
UE-ID=17037   DL-TPT=0.0003    UL-TPT=1.5981  
UE-ID=17049   DL-TPT=1.6011    UL-TPT=0.0100  
UE-ID=17037   DL-TX=10      DL-RETX=0       DL-BLER=0.0000  DL-MCS=9       UL-CRC-SUCC=17994   UL-CRC-FAIL=0       UL-BLER=0.0000  UL-MCS=9       
UE-ID=17049   DL-TX=2676    DL-RETX=46      DL-BLER=0.0169  DL-MCS=8       UL-CRC-SUCC=464     UL-CRC-FAIL=0       UL-BLER=0.0000  UL-MCS=9   
```