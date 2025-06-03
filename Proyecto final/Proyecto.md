#  ChatGPT API en Python con Typer y Rich

Este es un ejemplo sencillo de cómo interactuar con la API de ChatGPT usando Python, `typer` para la interfaz de línea de comandos y `rich` para salida formateada.

## Requisitos

Instala las siguientes librerías con pip:

```bash
pip install openai
pip install "typer[all]"
pip install rich
```
##  Función `main()`: Configuración inicial y bienvenida

Esta función inicia la aplicación de consola. Aquí se configura la clave de la API, se imprime un mensaje de bienvenida estilizado y se muestra una tabla con comandos disponibles.
Código explicado

###  `main()`: Configuración inicial y bienvenida

```python
def main():
    openai.api_key = "TU_API_KEY creada en https://platform.openai.com"
```

* Aquí se asigna tu clave personal de la API de OpenAI. Esta es necesaria para autenticar tus peticiones.

```python
    print("💬 [bold green]ChatGPT API en Python[/bold green]")
```

* Muestra un mensaje de bienvenida en consola con formato en color gracias a `rich.print()`.

```python
    table = Table("Comando", "Descripción")
    table.add_row("exit", "Salir de la aplicación")
    table.add_row("new", "Crear una nueva conversación")
    print(table)
```

* Crea e imprime una tabla con dos comandos disponibles para el usuario: `exit` y `new`.

---

### 🔹 Contexto y bucle de conversación

```python
    context = {"role": "system",
               "content": "Eres un asistente muy útil."}
    messages = [context]
```

* Se inicializa la conversación con un mensaje de sistema que define el comportamiento del asistente.
* Este contexto se envía al modelo para que actúe como un ayudante útil.

```python
    while True:
        content = __prompt()
```

* Comienza un bucle infinito que mantendrá el chat funcionando hasta que el usuario lo detenga con `exit`.

```python
        if content == "new":
            print("🆕 Nueva conversación creada")
            messages = [context]
            content = __prompt()
```

* Si el usuario escribe `"new"`, el historial de la conversación se reinicia.

```python
        messages.append({"role": "user", "content": content})
```

* El mensaje del usuario se guarda en el historial (`messages`) con el rol `"user"`.

```python
        response = openai.ChatCompletion.create(
            model="gpt-3.5-turbo", messages=messages)
```

* Se realiza la llamada a la API de OpenAI usando el modelo `gpt-3.5-turbo` con todo el historial.

```python
        response_content = response.choices[0].message.content
```

* Se extrae el contenido de la respuesta generada por el asistente.

```python
        messages.append({"role": "assistant", "content": response_content})
```

* La respuesta también se guarda para mantener el contexto completo.

```python
        print(f"[bold green]> [/bold green] [green]{response_content}[/green]")
```

* Se imprime la respuesta del asistente en consola con formato de color.

---

### 🔹 Función auxiliar `__prompt()`

```python
def __prompt() -> str:
    prompt = typer.prompt("\n¿Sobre qué quieres hablar? ")
```

* Utiliza `typer.prompt()` para mostrar un campo interactivo en consola donde el usuario puede escribir.

```python
    if prompt == "exit":
        exit = typer.confirm("✋ ¿Estás seguro?")
        if exit:
            print("👋 ¡Hasta luego!")
            raise typer.Abort()
        return __prompt()
```

* Si el usuario escribe `"exit"`, se confirma si desea salir.
* Si acepta, la aplicación termina. Si no, se vuelve a pedir un nuevo prompt.

```python
    return prompt
```

* Retorna el texto escrito por el usuario para ser procesado en el bucle principal.

---

###  Ejecución del programa

```python
if __name__ == "__main__":
    typer.run(main)
```

* Inicia la ejecución de la función `main()` usando `typer`, que maneja la CLI de forma ordenada y legible.

---

# ¿Qué hace este proyecto?

* Lanza una app de terminal para chatear con ChatGPT.
* Usa `rich` para embellecer la consola.
* Usa `typer` para capturar y manejar comandos del usuario.
* Permite iniciar nuevas conversaciones o salir de forma elegante.



