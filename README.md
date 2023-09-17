"const inputTxt = document.querySelector("input");
      const btn = document.querySelector(".FizzBuzz");

      function FizzBuzz() {
        const numberValue = parseInt(inputTxt.value);
        for (let i = 0; i <= numberValue; i++) {
          if (inputTxt.value === "0") {
            console.error("0 no es multiplo de ningun numero");
          } else if (i === 0) {
            console.log(0);
          } else if (i % 3 === 0 && i % 5 === 0) {
            console.log("FizzBuzz");
          } else if (i % 3 === 0) {
            console.log("Fizz");
          } else if (i % 5 === 0) {
            console.log("Buzz");
          } else if (inputTxt.value === " ") {
            console.log("tiene q poner un valor");
          } else {
            console.log(i);
          }
        }
      }

      function validación(num) {
        if (num === undefined) throw new Error("Valor indefinido");
        if (num < 0) throw new Error("no se puede usar numeros negativos");
        if (num > 3000)
          throw new Error("Numero muy alto tiene que ser menor que 3000");
        return FizzBuzz();
      }
      btn.onclick = () => {
        validación(parseFloat(inputTxt.value));
      };"