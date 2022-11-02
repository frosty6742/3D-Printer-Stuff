
###Temp tower layer height generator for Slic3r
'
;Add the following to before each layer change setting:
;M104 S{220 - (a * int(((layer_z - b)/ c)))}
;a == temperature step per level 
;b == the layer height for platform or brim 
;c == the thickness in z of each temp tower level 

;Examples ; https://www.thingiverse.com/thing:2493504/files  
; at 0.2mm layer height, these have 6.8mm thickness per level and have a 0.8mm intro platform for better bed adhesion:
;PLA - 180-220: M104 S{220 - (5 * int(((layer_z - 0.8)/ 6.8)))} 
;PETG/ABS - 220-260 M104 S{260 - (5 * int(((layer_z - 0.8)/ 6.8)))}

