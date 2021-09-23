````swift
import UIKit

/*Ahora, por fin, entiendo la programación orientada a objetos.
 Aquí hay un ejemplo del objeto tipo Person, y como creo otros objetos
 siguiendo el esquema base y usando funciones dentro de esos mismos objetos*/

struct Person {
    let firstName: String
    let lastName: String
    func sayHello() {
        print("Hello there! My name is \(firstName) \(lastName).")
    }
}

let Person1 = Person(firstName: "Belén", lastName: "Guisado")
let Person2 = Person(firstName: "Rubén", lastName: "Escribano")

Person1.sayHello()
Person2.sayHello()

struct Town {
  let name: String
  var citizens: [String]
  var resources: [String: Int]
  
  init(name: String, citizens: [String], resources: [String: Int]) {
    self.name = name
    self.citizens = citizens
    self.resources = resources
  }
  
  func fortify() {
    print("Defenses Increased!")
  }
  
  var newDelhi = Town(name: "New Delhi", citizens: ["Ángela Yu", "Jack Bauer"], resources: ["Coconuts": 100, "Wood": 100])
  newDelhi.citizens.append("Tom Hanks")
  print(newDelhi.citizens.count)
  newDelhi.fortify()  
}

/*Aquí hay ejemplos de control de flujo con operadores en Swift.
 Los principales operadores soportados en Swift son:
  == Los valores deben ser exactamente iguales.
  != Los valores NO deben ser iguales.
  >  El valor de la izquierda debe ser mayor que el de la derecha.
  >= El valor de la izquierda debe ser mayor o igual que el de la derecha.
  <  El valor de la izquierda debe ser menor que el de la derecha.
  <= El valor de la izquierda debe ser menor o igual que el de la derecha.
  && Equivale al condicional AND.
  || Equivale al condicional OR.
  !  Equivale al condicional NOT.
 */

let temperature = 70

if temperature >= 65 && temperature <= 75 {
    print("La temperatura está perfecta.")
} else if temperature < 65 {
    print("La temperatura está demasiado fría.")
} else {
    print("La temperatura está demasiado caliente.")
}

var isPluggedIn = true
var HasBatteryPower = false

if isPluggedIn || HasBatteryPower {
    print("Puedes usar el portatil.")
} else {
    print("Conecta el portatil a una fuente de alimentación")
}

/*Esto son ejemplos de switch-case statments, la diferencia con If/Else radica
 en que en este caso se busca un valor concreto para seguir con el algoritmo y no
 se usan operadores. obviamente los valores deben ser del mismo tipo.*/

let numberOfwheels = 2

switch numberOfwheels {
case 1:
    print("It's a Monocycle!")
case 2:
    print("It's a Bicycle!")
case 3:
    print("It's a Tricycle!")
case 4:
    print("It's a Quadcycle!")
default:
    print("That's a lot of wheels!")
}

let character = "z"

switch character {
case "a", "e", "i", "o", "u":
    print("¡Eso es una vocal!")
default:
    print("¡Eso es una consonante!")
}

var distance = 34

switch distance {
case 0...9:
    print("Estás muuuuy cerca de tu destino")
case 10...99:
    print("No estás excesivamente lejos")
case 100...999:
    print("Estás muuuuuy lejos de tu destino")
default:
    print("No creo que llegues nunca tan lejos")
}

/*Esto es un ejemplo de un código de control del flujo con operadores booleanos reducido.
 Al determinar el valor que se va a guardar en la variable largest se pregunta al sistema si a > b es true o false,
 en el caso de que sea true se almacena el valor a la izquierda de :, si es false se almacena el que está a la derecha.*/

var largest: Int

let a = 15
let b = 70

largest = a > b ? a:b

print ("""
Hola es que no
no se lo que tienes
tu que hacer aqui
""")

func sayHello (to: String, and: String) {
    print("Hola \(to) y \(and)")
}
sayHello(to: "Rubén", and: "Belén")

func multiply (First: Int, Second: Int) -> Int {
    let result = First * Second
    return result
}
multiply(First: 3, Second: 40)

func loveCalculator() {
    let loveScore = Int.random(in: 0...100)
    switch loveScore {
    case 0...40:
        print("No luck dude")
    case 41...80:
        print("you could get her in love with you if you try!")
    case 81...100:
        print("You love each other like Kanye loves himself!")
    default:
        print("Error, something bad happened!")
    }
}
loveCalculator()
````

Tags:
#code #swift #iOS
