# Composicion-bacteriana-de-rios pruebaaaaa
# Comparación de la composición bacteriana de dos ríos urbanos: Río Bogotá (Colombia) y Río Pinheiros (Brasil)

**Autores:** Ariana Delgadillo, Sergio Sánchez, Nataly Rodríguez
**Institución:** Universidad del Rosario

Este repositorio contiene los scripts, datos y documentación del análisis metagenómico
de comunidades bacterianas en dos ríos urbanos (Pinheiros y Bogotá), basado en secuencias
del gen 16S rRNA.

## Contenido del repositorio

- `scripts/`: Scripts en R para mirar la calidad de las secuencias, R desde cluster
para seguir con el pipeline de DADA2 hasta tener dos tablas de conteo para cada río,
luego desde R se hace análisis de diversidad alfa, beta y abundancia diferencial.
- `results/`: Gráficos los resultados de los análisis.

## Descripción del análisis

Los datos provienen de repositorios públicos:

`nota/`: Se tomarón solo seis pares de secuencias para cada río.
- Río Bogotá: [ENA - PRJEB22915](https://www.ebi.ac.uk/ena/browser/view/PRJEB22915)
- Río Pinheiros: [Zenodo Dataset](https://zenodo.org/records/1172783)

Los análisis incluyen:

1. **Calidad de secuencias** con paquetes de R `BiocManager` y `DAD2`.
2. **Procesamiento de secuencias** con DAD2 desde el cluster.
3. **Análisis de diversidad alfa, beta y comparación diferencial** con `phyloseq` y `vegan`:
   - Índices Shannon y Simpson
   - Wilcoxon
   - Bray-Curtis + PCoA
   - PERMANOVA (`adonis2`)

