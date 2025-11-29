# Configuración del Entorno de Desarrollo

Esta guía describe los pasos para configurar el entorno de desarrollo utilizando `uv`, un instalador y gestor de paquetes de Python rápido.

## 1. Instalación de `uv` [oficial-page↗](https://docs.astral.sh/uv/getting-started/installation/)

Para instalar `uv` en Linux o macOS, puedes usar el siguiente comando en tu terminal:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Para Windows, puedes usar PowerShell:

```powershell
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Después de la instalación, asegúrate de que la terminal se ha reiniciado o de que has recargado la configuración de tu shell para que el comando `uv` esté disponible.

## 2. Creación del Entorno Virtual (Opcional)

Una vez instalado `uv`, puedes crear un entorno virtual en la carpeta actual del proyecto.

1.  Crea el entorno virtual con alguna version de python. Esto creará una carpeta `.venv` en el directorio actual.
    ```bash
    uv init .
    uv python pin 3.13
    ```
2.  Añadir librerias
    ```bash
    uv add scikit-learn matplotlib pandas
    ```
## 3. Sincronización/Activar entorno
1. Sincronizar
    ```bash
      uv sync
    ```
2.  Activa el entorno virtual.
    - En Linux/macOS:
      ```bash
      source .venv/bin/activate
      ```
    - En Windows (Command Prompt):
      ```cmd
      .venv\Scripts\activate
      ```
    - En Windows (PowerShell):
      ```powershell
      .venv\Scripts\Activate.ps1
      ```
