# Seguimiento_1_Bioinfo
Este tipo de archivos, constan de 9 campos obligatorios que son:
1. sequid: Este nos va a servir para identificar la secuencia a la que pertence la anotacion. (Puede ser un cromosoma, genoma, etc.)
2. source: Origen de la anotación. (Esta puede ser una base de datos, software, pipeline, etc. Si no cuenta con eso se agrega un ".")
3. type: Tipo de caracteristica genética de la anotación. (gen, wxon, CDS mRNA, etc.)
4. start: Posición inicial donde comienza la secuencia. (Que normalmente es 1, no 0)
5. end: Posición final de la secuencia.
6. score: Valor que representa el nivel de confianza o significancia. (Si el modelo no cuenta con el se escribe un ".")
7. strand: Hebra donde se encuentra la caracteristica, ya sea, hebra directa 5´-> 3´ (+), commplementaria 3´-> 5´(-), o desconocido (.).
8. phase: Solo se usa en secuencia codificante (CDS) e indica el marco de lectura (puede ser 0, 1, 2 o "."). Esto varía dependiendo de cuantas bases faltan para el primer codon codificante. 
9. attributes: Brinda propiedades adicionales como ID, Parent, Name, etc.

Ej: 

chr2   .   gene   1000   7000   .   +   .   ID=gene0001;Name=SOUL 


chr2   .   mRNA   1800   7000   .   +   .   ID=mRNA0001;Parent=gene0001;Name=SOUL-001


chr2   .   exon   4000   7000   .   +   .   ID=exon0001;Parent=transcript0001


chr2   .   CDS    5000   5500   .   +   0   ID=cds0001;Parent=transcript0001


- sequid: "chr2" (El gen está en el cromosoma 2)


- source: "." (No se registra de donde surgió la anotación)


- type: "gene" (Es una feature tipo gen)


- start: "1000" (Empieza en la base 1000)


- end: "7000" (termina en la base 7000)


- score: "." (No se proporciona un score)


- strand: "+" (El gen es de hebra directa)


- phase: "." (Solo aplica para el CDS) (Y para el ultimo caso que es CDS, el "0" significa que desde el 1er nucleotido empieza el primer codon codificante)


- attributes: "ID=gene0001;Name=SOUL" (Proporciona ID único del gen y el nombre)


El organismo asignado es "Cairina moschata domestica" este es una variedad domesticada del pato mudo (Cairina moschata), es una especeie de ave acuática originaria de América tropical. Es criada principalmente por usar su carne como alimento e incluso en algunas regiones es considerada como ave ornamental. Su genoma fue secuenciado principalmente para estudios genéticos enfocados en la evolución aviar y mejoramiento animal.


1. ¿Cuantos features contiene el archivo? : 944022
2. ¿Cuantas regiones de la secuencia (cromosomas) contiene el archivo?: 2941 
3. ¿Cuántos genes están listados en el organismo? 15898
4. ¿Cuál es el top 10 de tipo de features (columna 3) más anotados en el genoma?
   Top 10
   1. exon: 395833
   2. CDS: 381077
   3. biological_region: 80277
   4. mRNA: 29016
   5. five_prime_UTR: 18942
   6. gene: 15898
   7. three_prime_UTR: 15713
   8. region: 2941
   9. lnc_RNA: 2152
   10. ncRNA_gene: 1651



