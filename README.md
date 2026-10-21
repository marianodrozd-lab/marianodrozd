# Reactivar productos Lecuine con tarifas CyC

Proyecto para reactivar en PrestaShop (lecuine.com) productos descatalogados o
desactivados que vuelven a estar disponibles en la tarifa del distribuidor CyC.

## Flujo por producto

1. **Brief**: recopilar datos oficiales del fabricante (medidas, referencia,
   EAN, garantía, materiales) y cruzarlos con la tarifa CyC. El EAN del
   producto en PrestaShop debe coincidir con el de la tarifa.
2. **Ficha**: redactar la ficha en castellano a partir del brief
   (agente `redactor-fichas`).
3. **Fotos**: solo fotos oficiales del fabricante. No se usan fotos de
   tiendas. Si no hay web oficial accesible, pedirlas a CyC o al fabricante.
4. **Subida**: subir ficha y fotos a PrestaShop **sin publicar**. Los
   productos permanecen desactivados hasta revisión final.

## Estructura

```
briefs/      un archivo por producto: <id>-<marca>-<modelo>.md
fichas/      ficha en castellano lista para PrestaShop, mismo nombre
fotos/       fotos oficiales por producto, carpeta <id>/
tarifas/     tarifa CyC de referencia (no subir datos sensibles)
ESTADO-fichas-wusthof-cyc.md   estado de la tanda en curso
```

## Convenciones

- El nombre del producto en PrestaShop describe el producto real. Ejemplo:
  la 626 es un set santoku 18 cm + cuchillo de oficio 15 cm, no un
  "fileteador".
- Las medidas de hoja se expresan en cm, redondeando desde pulgadas cuando
  la fuente oficial es KAI USA (2,5" = 6,5 cm).
- Todo dato no confirmado por fuente oficial se marca como **sin confirmar**
  en el brief y no se afirma en la ficha.
