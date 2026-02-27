# reto_practico_de


## SQL

Las queries están escritas en SQLite. Se aplican correcciones de calidad sobre los datos de origen: normalización de nombres, eliminación de caracteres especiales y parsing de strings con `INSTR` y `SUBSTR`.

## PySpark

Ejecutar en Google Colab o Databricks. Los archivos de salida se guardan en `/tmp/`.

```bash
pip install pyspark
```

Los DataFrames siguen nomenclatura medallion: `_raw` para datos crudos, `_silver` para datos limpios y tipados, `_gold` para el resultado final.

## Archivos de salida

| Archivo | Formato | Ruta |
|---|---|---|
| Nuevo_Ranking | JSON | /tmp/Nuevo_Ranking.json |
| centros_reunion | Parquet | /tmp/centros_reunion.parquet |
| centros_reunion | JSON | /tmp/centros_reunion.json |
| centros_reunion | CSV (sep=\|) | /tmp/centros_reunion.csv |
