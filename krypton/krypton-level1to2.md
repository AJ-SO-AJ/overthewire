# Level 1 -> 2
Simple rotation cipher. To decrypt we need to rotate. Typical rotation is 13, so we will use the tr command for that.

The file krypton2 has:

- YRIRY GJB CNFFJBEQ EBGGRA
- Solution: cat krypton2 | tr 'A-Za-z' 'N-ZA-Mn-za-m'
