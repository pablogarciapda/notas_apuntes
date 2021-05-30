# notas_apuntes

una duda que me aparece de uso de brackets o de parentesis. get: () => store.getters['boardModule/getCardsByColumn'](props.column.id),
      set: (payload) => store.dispatch('boardModule/updateCards', payload)   Porque en el getters se usa brackets? y no parentesis o corchetes
      
frontSparrow — 28/05/2021
@pablo, en javascript a los objetos se puede acceder a sus propiedad de dos formas:
   const obj = {
        name: 'Test',
        age: {
            x: 100,
            y: 1000,
        }
    };
    console.log(obj.name, obj.age.x);           // usando el punto: Test 100
    console.log(obj['name'], obj['age']['x']);  // usando los corchetes, que puede llevar a equivocación con un array asociativo: Test 100

    // Array asociativo
    const car = new Array();
    car['colour'] = 'red';
    car['model'] = 'ferrari';

    console.log(car, car['colour']); // [colour: 'red', model: 'ferrari'] red
en el getters estas accediendo a un objeto, por eso store.getters[propiedad]() --> Los parentesis ejecutan ese getters
store.dispatch() --> ejecutas esa acción


…or create a new repository on the command line
echo "# notas_apuntes" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/pablogarciapda/notas_apuntes.git
git push -u origin main

…or push an existing repository from the command line
git remote add origin https://github.com/pablogarciapda/notas_apuntes.git
git branch -M main
git push -u origin main
