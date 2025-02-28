#Saludos en Go
Este paquete proporciona una forma simple de obtener saludos personalizados en Go.

#Istalación
Ejecuta el siguiente comando para instalar el paquete:
```bash
go get -u github.com/Verito24/greetings

#Uso
Aqui tienes un ejemplo de como usar el paquete desde tu código:

package main

import (
	"fmt"
	"log"
	"github.com/Verito24/greetings"
)

func main() {
	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	names := []string{"Pedro", "Juan", "Diego"}
	messages, err := greetings.Hellos(names)
	if err != nil {
		log.Fatal(err)

	}
	
	fmt.Println(messages)
}
