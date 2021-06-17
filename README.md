# kipusqa-simi.github.io
Proyect: Kipusqa Simi

## setup

1. Ir a https://estuary.mcmaster.ca - Collaborate - Ensemble: **kipusqa**, password: *quechua**
2. Correr las líneas de audio en la terminal:  
+`!insertaudioresource "https://jac307.github.io/kipusqa-simi.github.io/samples/muhu.wav?raw=true"  simi 0`
+`!insertaudioresource "https://jac307.github.io/kipusqa-simi.github.io/samples/paqarina.wav?raw=true"  simi 1`
+`!insertaudioresource "https://jac307.github.io/kipusqa-simi.github.io/samples/pisqu.wav?raw=true"  simi 2` 
3. Evaluar ##JSoLang yupana  
4. Evaluar ##JSoLang simi  
5. Correr en la terminal:  
+`!localview (grid 2 1 [[code 5 0],[code 7 0]])`


## yupana [visuales]

Syntaxis oración básica  
+ `Puriyñan` o `Puriy ñan`

| palabra    | Info                |
| ---------- | ------------------- |
| `Puriy`    | corre un video      |
| `ñan`      | link de video       |
| `ñawi`     | link de video       |
| `ñawi`     | link de video       |

Las transformaciones se agregan antes de la oración básica, entre cada comando nuevo debe ir:  `_`  
+ `Llimpi(1.2)_Puriyñan` o `Llimpi 1.2_Puriyñan` o `llimpi(1.2)_Puriyñan`  

| palabra      | Valores                 |
| ------------ | ----------------------- |
| `Llimpi`     | brillo(0++)             |
| `chaquy`     | vel(0++) durVide(0 a 1) |
| `Ayphu`      | opacidad(0 a 1)         |

Las palabras se pueden escribir con mayúsculas o minúsculas:  

+ `CHAQUY(15)(2)_Llimpi(1.2)_Puriyñan` o `chaquy(10)(2)_Llimpi(1.2)_Puriyñan`  

Reproducir dos o más videos  
Se debe separar cada oración con punto y coma `;`:  

+ `chaquy(10)(2)_Llimpi(1.2)_Puriyñan; Ayphu(0.5)_puriynina`


## simi [sonidos]

Syntaxis oración básica  
+ `Puriymuhu"` o `Puriy muhu"`

| palabra     | Info                |
| ----------- | ------------------- |
| `Puriy`     | corre un sonido     |
| `muhu"`     | link de audio       |
| `paqarina"` | link de audio       |
| `pisqu"`    | link de audio       |

Transformaciones que deben ir antes de la oración básica:  
+ `mayupuriypaqarina"` o `mayu puriypaqarina"` o `Mayupuriypaqarina"`  

| palabra      | Info                                       |
| ------------ | ------------------------------------------ |
| `mayu`       | cambia la duracion del ciclo a 2 segundos  |

Transformaciones que deben ir después de la oración básica:  
+ `mayupuriypaqarinakuna"` o `puriypaqarinakuna"`

| palabra      | Valores                              | Info
| ------------ | ------------------------------------ |
| `kuna`       | sin valor                            | Debe escribirse antes del símbolo `"`. Multiplica el audio x2                           |
| `chaquy`     | vel(-1 a 1)                          | Debe escribirse después del símbolo `"`. Invierte la reproducción con números negativos |
| `Llimpi`     | nota (números positivos o negativos) | Debe escribirse después del símbolo `"`. Cambia el color del sonido                     |

Las palabras se pueden escribir con mayúsculas o minúsculas:  

+ `puriypaqarinakuna"chaquy(-0.5)Llimpi(6)` o `puriypaqarinakuna"CHAQUY(-0.5)llimpi(6)`  

Reproducir dos o más sonidos  
Añandir `simi[]` y poner los sonidos adentro de los corchetes `[]`, separados con comas `,`:  

+ `simi[puriypaqarinakuna"CHAQUY(-0.5)llimpi(6), puriypisqu"]`


## Info Extra:
Para volver a la vista por defecto se puede refrescar la páguina del browser o correr la siguiente línea en la terminal:
+`!localview !( grid 2 3 [[code 1 0],[code 3 0],[code 5 0],[code 7 0],[code 9 0],[code 11 0]] )`

