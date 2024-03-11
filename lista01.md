Questões Objetivas

1. A
2. A
3. A
4. A
5. A
6. A

Questões Dissertativas

7. 

    class animal{
        constructor(nome, idade){
            this.idade = idade;
            this.nome = nome;
        }
        descrever(){
            console.log(`Esse é um ${this.nome} com ${this.idade} anos.`)
        }
    }
        const cachorro = new animal('cachorro', 10);
        cachorro.descrever();

        const gato = new animal('gato', 8);
        gato.descrever();

8. 

    class animal{
        constructor(nome, idade){
            this.idade = idade;
            this.nome = nome;
        }
        descrever(){
            console.log(`Esse é um ${this.nome} com ${this.idade} anos.`)
        }
    }

    class Gato extends animal{
        constructor(nome, idade, cor){
            super(nome, idade);
            this.cor = cor;
        }
        miar(){
            console.log('MIAAAAAAAAAAAAAAAAAAAAAAAU');
        }
    }
        
        const cachorro = new animal('cachorro', 10);
        cachorro.descrever();

        const gato = new Gato('gato', 8, 'preto');
        gato.descrever();
        gato.miar();

9. 
        
    class SomadordeNotas{
        constructor(total){
        this.total = 0;}

        AdicionarNota(nota){
            this.total += nota;
        }

        VerTotal(){
            console.log(`A soma total das notas é ${this.total}.`)
        }
    }

    const somador = new SomadordeNotas();

    somador.AdicionarNota(8);
    somador.AdicionarNota(7.5);
    somador.AdicionarNota(9.5);

    somador.VerTotal();

10. 

    class Funcionario{
        constructor(nome, idade, salariobase){ //Definindo os atributos 
            this.nome = nome;
            this.idade = idade;
            this.salariobase = salariobase;
        }

        calcularsalario(){
            console.log(`O salário base é ${this.salariobase}`); // Método de cálculo do salário do Funcionario 
        }
    }

    class Professor extends Funcionario{
        constructor(nome, idade, diciplina, horas){
            super(nome, idade); // Herdando os atributos da classe Funcionario e definindo novos 
            this.diciplina = diciplina;
            this.horas = horas;
        }
        calcularsalario(){ // Método de cálculo do salário do Professor
            this.salario = this.horas * 250; //Defini a hora trabalhada por hora como 250
            console.log(`O salário do ${this.nome}, professor de ${this.diciplina} é ${this.salario}`);
        }
    }

    let professor01 = new Professor('Paulo', 37, 'história', 40);
    professor01.calcularsalario();

    let professor02 = new Professor('Cléber', 67, 'matemática', 30);
    professor02.calcularsalario();


