---
title: "Comandos Linux: cd"
date: 2025-01-19
draft: false
tags:
  - comandos linux
---
El comando cd nos permite cambiar el directorio de trabajo en el que nos encontramos.

Podemos usarlo con rutas relativas:

cd ./Escritorio

cd ./mi-proyecto

Pero tambien absolutas:

cd /etc/ssh

cd /var/log

Además, podemos ir más arriba en el arbol del directorio en el que nos encontramos:

```
cd test

cd

cd

cd
```

Además, en caso de que queramos volver al directorio anterior, podemos usar el comando cd -:

\`\`\`bash

_user@~_ pwd

_/home/user_

_user@~_ cd /tmp

_user@/tmp_ pwd

_/tmp_

_user@/tmp_ cd -

_user@~_ pwd

_/home/user_

\`\`\`