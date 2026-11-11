## LAB # 24

### A.1 · Ficha del equipo

La ficha original registra un portátil con Windows y 16 GB de RAM. La marca y el modelo quedaron sin registrar. El equipo actual es un HP Victus 15-fa1xxx con 32 GB de RAM.

| Configuración | Modelo registrado | Parámetros | Memoria estimada a 4 bits | ¿Cabe en el equipo original? |
| --- | --- | ---: | ---: | --- |
| L1 | Qwen2.5-1.5B-Instruct | 1.5B | 0.75 GB (0.90–0.98 GB con margen) | Sí, según la estimación |
| L2 | Qwen2.5-7B-Instruct | 7B | 3.50 GB (4.20–4.55 GB con margen) | Sí, según la estimación |
| N | ChatGPT gratuito | Sin registro | Procesamiento remoto | No aplica |

Cada mil millones de parámetros a 4 bits ocupan aproximadamente 0.5 GB de pesos. El contexto y la aplicación requieren memoria adicional. Los nombres locales se tomaron del informe original y quedan por cotejar con la app.

**Predicción registrada.** L1 sería el más rápido entre los modelos locales y L2 daría mejores respuestas. La ficha no registra el motivo.

**Condiciones anotadas.** L1 y L2 en QV.AC sin internet y N en ChatGPT gratuito con internet. Batería o corriente y otras aplicaciones abiertas quedaron sin registrar.

### A.2 · Instrucciones

1. Resume en 3 viñetas, en español, este aviso: "La cooperativa Agro Cuchumatanes Prueba informa que la entrega de semillas de maíz se mueve del lunes 3 al jueves 6 por la lluvia. Traigan su tarjeta de socio. Quien no pueda llegar puede mandar a un familiar con una nota firmada. El fertilizante se entrega el mismo día, solo a socios al día con su cuota."
2. Un modelo tiene 8 mil millones de parámetros y está cuantizado a 4 bits. ¿Cuántos GB de memoria necesita, aproximadamente, sin contar el margen? Explica la cuenta en dos líneas.
3. Escribe un mensaje corto de WhatsApp (máximo 60 palabras), amable y en español de Guatemala, para avisarle a un cliente ficticio de Remesas Volcán Prueba que su envío está listo para recoger en agencia y que debe llevar su documento de identificación.

**Clave para el juez.** 8 × 4 ÷ 8 = 4 GB sin margen. Otra cifra limita la nota a 2.


### A.3 · Mediciones y calidad por respuesta

| Configuración | Instrucción | Primera palabra (s) | Total (s) | Tokens/s | Calidad (1–5) | Razón según A.4 | Condiciones o incidencias |
| --- | ---: | --- | --- | --- | --- | --- | --- |
| L1 | 1 | No se pudo¹ | No se pudo¹ | Sin registro | Sin calificar | Requiere la respuesta completa y la rúbrica A.4. | Sin registro |
| L1 | 2 | No se pudo¹ | No se pudo¹ | Sin registro | Sin calificar | Verificar con la clave de 4 GB. | Sin registro |
| L1 | 3 | No se pudo¹ | No se pudo¹ | Sin registro | Sin calificar | Requiere la respuesta completa y la rúbrica A.4. | Sin registro |
| L2 | 1 | No se pudo¹ | No se pudo¹ | Sin registro | Sin calificar | Requiere la respuesta completa y la rúbrica A.4. | Sin registro |
| L2 | 2 | No se pudo¹ | No se pudo¹ | Sin registro | Sin calificar | Verificar con la clave de 4 GB. | Sin registro |
| L2 | 3 | No se pudo¹ | No se pudo¹ | Sin registro | Sin calificar | Requiere la respuesta completa y la rúbrica A.4. | Sin registro |
| N | 1 | No se pudo¹ | No se pudo¹ | Sin registro | Sin calificar | Requiere la respuesta completa y la rúbrica A.4. | Sin registro |
| N | 2 | No se pudo¹ | No se pudo¹ | Sin registro | Sin calificar | Verificar con la clave de 4 GB. | Sin registro |
| N | 3 | No se pudo¹ | No se pudo¹ | Sin registro | Sin calificar | Requiere la respuesta completa y la rúbrica A.4. | Sin registro |

¹ No se pudo recuperar un registro de cronómetro por instrucción. Para completar la tabla, registrar los tiempos y copiar los tokens/s si la app los muestra. Si la app carece de esa métrica, escribir «no muestra». Calificar cada respuesta completa con A.4 sin mirar los tiempos.

### A.4 · Rúbrica de calidad

| Nota | Criterio |
| ---: | --- |
| 5 | Correcta, completa, clara y en buen español. Se puede usar tal cual. |
| 4 | Correcta con un detalle menor. Basta un retoque. |
| 3 | Útil pero incompleta o con un error visible. Requiere corrección. |
| 2 | Errores importantes, datos inventados o incumplimiento de la instrucción. |
| 1 | Incorrecta, sin sentido, en otro idioma o sin respuesta. |

En la instrucción 1, comprobar que haya tres viñetas y que incluyan el jueves 6, la tarjeta de socio, la opción de enviar a un familiar con nota firmada y el fertilizante solo para socios al día. En la 2, comprobar los 4 GB y la cuenta en dos líneas. En la 3, comprobar el límite de 60 palabras, el tono amable, el español de Guatemala, el aviso de recogida en agencia y el documento de identificación, sin datos inventados.


### Reflexión

- **(a)** Queda pendiente determinar qué configuración ganó en velocidad y calidad, por cuánto y si se cumplió la predicción. Faltan los tiempos y las notas por instrucción.
- **(b)** L1 podría bastar para clasificar solicitudes generales de la venture por tema. Para tomar decisiones financieras que requieren verificar cifras y supuestos, usaría revisión humana.
- **(c)** Sin internet, las instrucciones se procesan en el equipo. En la nube, el proveedor recibe las instrucciones para generar la respuesta.
