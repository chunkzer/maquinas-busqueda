# Máquinas de búsqueda

En este repositorio se explorarán algoritmos de *ranking* utilizados en motores de búsqueda como parte de la asignatura *Tópicos avanzados en inteligencia artificial*.

## Instrucciones para correr Foofle

### Generar un índice con el crawler

Abrir `ipython` en el directorio `collective-intelligence`

```
In [1]: import searchengine

In [2]: urls = [url, ...]

In [3]: crawler = searchengine.crawler("index.db")

In [4]: crawler.db_create_tables()

In [5]: crawler.crawl(urls, depth=D)

In [6]: crawler.calculate_pagerank(I)

In [7]: exit
```

Uno tiene que determinar los valores de:

- `[url, ...]` : Lista con URLs (las URLs son cadenas de caracteres)
- `D` : Es un entero positivo que indica la profundidad de la búsqueda (sugiero que primero lo hagan con 1 o con 2, ya que con las pruebas que yo hice, una profundidad de 3 tardó mas de una noche en correr).
- `I` : Iteraciones del cálculo del Pagerank, con 20 tarda algo de tiempo pero mucho menos que hacer `crawl`, pudieran probar con valores mas grandes para aproximar mejor el valor de pagerank.

Para iniciar el servidor, abren una terminal en la carpeta `website` y ejecutan

```
python -m server
```

Después pueden abrir en algún browser la dirección `localhost:3456`.

Ahora solo falta disfrutar los resultados de `Foofle search` (seguramente son algo macanas los resultados, falta ponderar los scores).
