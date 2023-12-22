[Uploading assets…]()<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Encriptador</title>
    <link rel="icon" href="https://cdn-icons-png.flaticon.com/512/2494/2494628.png"/>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Rubik+Doodle+Shadow&display=swap"/>
    <link rel="stylesheet" href="styles.css"/>
</head>
<body>
    <fieldset class="mi-fieldset">
        
           <div class="container">
                <h1>Codigo Morse </h1>
               <label for="inputText">Mensaje:</label>
               <textarea id="inputText" placeholder="Insertar tu texto" rows="4"></textarea>
               <div class="buttons">
                   <button onclick="encriptar()">Encriptar</button>
                   <button onclick="desencriptar()">Desencriptar</button>
               </div>
               <label for="outputText">Resultado:</label>
               <textarea id="outputText" placeholder="Mensaje secreto" rows="4" readonly></textarea>
           </div>   

            <details>
                <summary>ABC(morse)</summary> 
                <img src="https://i.pinimg.com/originals/6b/22/de/6b22de5cadeb85444d1039ec98d12f89.png" width="500" height="350"/>
          </details>
          <button name="boton-1" type="button">
          <img src="https://i.pinimg.com/originals/da/a1/d1/daa1d179d4f90c09258a68a1b7cc0410.gif" width="105">
        </button>
        </fieldset>
    
    <script src="script.js"></script>
</body>
</html>


# Quienes son los principales usuarios del producto 
Las personas en general que quieren comunicarse con un codigo mas complejo e innovador 

# cuales son los objetivos de estos usuarios en relacion con tu producto
el principal obetivo seria que puedan tener mas privacidad al comunicarse con las personas

# como crees que el producto que estas creando esta resolviendosus problemas
este producto soluciona un problema , ya que  el proyecto es facil de usar 



const codigoMorse = {
    'A': '.-', 'B': '-...', 'C': '-.-.', 'D': '-..', 'E': '.', 'F': '..-.', 'G': '--.', 'H': '....', 'I': '..', 'J': '.---',
    'K': '-.-', 'L': '.-..', 'M': '--', 'N': '-.','Ñ':'--.--','O': '---', 'P': '.--.', 'Q': '--.-', 'R': '.-.', 'S': '...', 'T': '-',
    'U': '..-', 'V': '...-', 'W': '.--', 'X': '-..-', 'Y': '-.--', 'Z': '--..',
    '0': '-----', '1': '.----', '2': '..---', '3': '...--', '4': '....-', '5': '.....', '6': '-....', '7': '--...', '8': '---..', '9': '----.',
    '.': '.-.-.-', ',': '--..--', '?': '..--..', '\'': '.----.', '!': '-.-.--', '/': '-..-.', '(': '-.--.', ')': '-.--.-', '&': '.-...',
    ':': '---...', ';': '-.-.-.', '=': '-...-', '+': '.-.-.', '-': '-....-', '_': '..--.-', '"': '.-..-.', '$': '...-..-', '@': '.--.-.'
};

const reversorCodigoMorse = {};
for (let char in codigoMorse) {
    reversorCodigoMorse[codigoMorse[char]] = char;
}

function encriptar() {
    const inputText = document.getElementById('inputText').value.toUpperCase();
    let resultado = '';

    for (let i = 0; i < inputText.length; i++) {
        const char = inputText[i];
        if (char === ' ') {
            resultado += ' ';
        } else if (codigoMorse[char]) {
            resultado += codigoMorse[char] + ' ';
        }
    }

    document.getElementById('outputText').value = resultado.trim();
}

function desencriptar() {
    const inputText = document.getElementById('inputText').value.split(' ');
    let resultado = '';

    for (let i = 0; i < inputText.length; i++) {
        const codigo = inputText[i];
        if (reversorCodigoMorse[codigo]) {
            resultado += reversorCodigoMorse[codigo];
        } else {
            resultado += ' ';
        }
    }
    document.getElementById('outputText').value = resultado;
}


body {
    font-family: 'Arial', sans-serif;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    margin: 0;
    background-image: url('eta.jpg');
    background-size: cover; 
    background-position: center; 
    background-repeat: no-repeat; 
}

.mi-fieldset {
    background-color: rgb(217, 147, 241);
}

.container {
    text-align: center;
}


textarea {
    width: 100%;
}

.buttons {
    margin-top: 10px;
}

button {
    margin: 5px;
    padding: 8px;
    cursor: pointer;
}

![eta](https://github.com/anamile-haru/codigo/assets/152450034/8a3166fb-be4f-4d14-9fa8-26505e90aef3)
