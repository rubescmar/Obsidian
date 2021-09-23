````javascript
async function windowAlert(){
const prompt = new Alert()

prompt.message = "Enter Password"
const pass = prompt.addSecureTextField("Password", "Password")
const cancel = prompt.addDestructiveAction("Cancel")
const enter = prompt.addAction("Enter")

await prompt.presentAlert()

let val = prompt.textFieldValue(0)
console.log(val)
return val
}

var answer = await windowAlert()


 while (answer !== "1234") {
	
	const error = new Alert()

	error.message = "Wrong! Try 1234"

	error.addAction("Try again!")

	await error.presentAlert()
	
	answer = await windowAlert()
}


const correct = new Alert()

correct.message = "Correct!"

correct.addAction("Continue")

correct.presentAlert()
````

Tags:
#code #javascript #scriptable