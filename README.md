Supervisor Sample
=================

Ejemplo de supervisión con `supervisord`.

## Instalación

```bash
pip install supervisord
```

## Ejecución sin supervisión

```bash
./programa.rb
```

## Ejecución con supervisión

```bash
supervisord -c supervisord.conf
```

Luego, verificar los siguientes archivos:

```bash
tail -F supervisord.log
tail -F programa.log
```

Alternativamente, verificarlo accediendo con el navegador desde `http://localhost:9001/`.

Observar qué sucede si se ejecuta:

```bash
while true; do ps ax | pgrep -of programa; sleep 1; done
```

Observar también que sucede si se ejecuta:

```bash
pkill -of programa.rb
```