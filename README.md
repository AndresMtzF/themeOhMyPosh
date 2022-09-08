# Theme OhMyPosh
Tema personalizado para Oh My Posh

## Guía de Instalación

Éste es el proceso que yo seguí, funcinaría en la mayoría de los casos. Para más información, consultar [OhMyPosh](https://ohmyposh.dev/) para más aclaraciones o consulta de temas.

### Primeros pasos

Es necesario tener instalada la ultima version de powershell y la podemos obtener desde la tienda: [Powershell](https://www.microsoft.com/store/productId/9MZ1SNWT0N5D)

Así como la terminal de Windows: [Terminal](https://www.microsoft.com/store/productId/9N0DX20HK701)

Y por último utilizar una de las fuentes compatibles, cualquier de las populares [NerdFonts](https://www.nerdfonts.com/). Cualquier Nerdfont debe ser compatible.

### NEXT

Configurar la terminal

1. Establecer el perfil predeterminado en la terminal de Powershell

2. Establecer el tipo de fuente en la terminal

### Instalación

Abrir Powershell prompt y ejecutar el siguiente comando

```
winget install JanDeDobbeleer.OhMyPosh -s winget
```

### Actualización

Abrir Powershell prompt y ejecutar el siguiente comando

```
winget upgrade JanDeDobbeleer.OhMyPosh -s winget
```

### Cambiar el prompt

Si no sabes que shell estás ocupando, puedes ejecutar el siguiente comando. 

```
oh-my-posh get shell
```

Salida:

<samp>pwsh</samp>

Es necesario editar el perfil, en este caso de powershell. Podemos encontrar su ubicación en la variable `$PROFILE`
Para editar: 

```
code $PROFILE
```

Si no usas VSC puede reemplazar `code` por `notepad` o el editor que uses.

Si, tras ejecutar el comando, se recibe un error, hay que asegurarse de crear el perfil primero. 

```
New-Item -Path $PROFILE -Type File -Force
```

Agregar la linea siguien al archivo

```
oh-my-posh init pwsh | Invoke-Expression
```

Una vez agregado, recargar el perfil para visualizar los cambios

`. $PROFILE`

### Cambiar Tema

Oh My Posh, inicia con el tema por defecto. Para cambiar la configurar un tema diferente en el `$PROFILE`.

```
oh-my-posh init pwsh --config 'C:/Users/Posh/custum-bubbles.omp.json' | Invoke-Expression
```

Una vez alterada la configuración, recargar el perfil

`. $PROFILE`

### Temas

Oh My Posh incluye una serie de temas, para visualiarlos:

```
Get-PoshThemes
```

Una vez elegido, podemos reemplazar el tema como se menciona anteriormente.

## Theme

![ohmyposh theme](/custum-bubbles.png)
