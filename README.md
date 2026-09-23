#Atividade 1

***TypeScript***
```typescript

class Pessoa {
    nome: string;
    idade: number;

    constructor(nome: string, idade: number) {
        this.nome = nome;
        this.idade = idade;
    }
}

const pessoa1 = new Pessoa("Ana Silva", 28);
console.log(pessoa1.nome);
console.log(pessoa1.idade);

```
#Atividade 2

***TypeScript***
```typescript
class Produto {
    nome: string;
    preco: number;
    estoque: number;

    constructor(nome: string, preco: number, estoque: number) {
        this.nome = nome;
        this.preco = preco;
        this.estoque = estoque;
    }

    exibirDados(): void {
        console.log(this.nome, this.preco, this.estoque);
    }
}

const produto1 = new Produto("Notebook", 3500.00, 10);
const produto2 = new Produto("Mouse", 89.90, 45);
produto1.exibirDados();
produto2.exibirDados();

```
#Atividade 3

***TypeScript***
```typescript

class Aluno {
    nome: string;
    nota: number;

    constructor(nome: string, nota: number) {
        this.nome = nome;
        this.nota = nota;
    }

    aprovado(): boolean {
        return this.nota >= 6;
    }
}

const aluno1 = new Aluno("Carlos", 7.5);
const aluno2 = new Aluno("Mariana", 5.0);

console.log(`--- STATUS DOS ALUNOS ---`);
console.log(`Aluno: ${aluno1.nome.padEnd(8)} | Nota: ${aluno1.nota.toFixed(1)} | Aprovado? ${aluno1.aprovado() ? "Sim ✅" : "Não ❌"}`);
console.log(`Aluno: ${aluno2.nome.padEnd(8)} | Nota: ${aluno2.nota.toFixed(1)} | Aprovado? ${aluno2.aprovado() ? "Sim ✅" : "Não ❌"}\n`);
```
#Atividade 4

***TypeScript***
```typescript
class Retangulo {
    largura: number;
    altura: number;

    constructor(largura: number, altura: number) {
        this.largura = largura;
        this.altura = altura;
    }

    calcularPerimetro(): number {
        return 2 * (this.largura + this.altura);
    }
}

const meuRetangulo = new Retangulo(5, 10);
console.log(`--- CÁLCULO DE PERÍMETRO ---`);
console.log(`Dimensões: ${meuRetangulo.largura}x${meuRetangulo.altura}`);
console.log(`Perímetro total: ${meuRetangulo.calcularPerimetro()} metros\n`);
```
#Atividade 5

***TypeScript***
```typescript
class ContaBancaria {
    #saldo: number;

    constructor(saldoInicial: number = 0) {
        this.#saldo = saldoInicial;
    }

    depositar(valor: number): void {
        if (valor > 0) {
            this.#saldo += valor;
            console.log(`Depósito de R$ ${valor.toFixed(2)} realizado.`);
        }
    }

    consultarSaldo(): number {
        return this.#saldo;
    }
}

const conta = new ContaBancaria(1000);
console.log(`--- EXTRATO BANCÁRIO ---`);
console.log(`Saldo Inicial: R$ ${conta.consultarSaldo().toFixed(2)}`);
conta.depositar(500);
console.log(`Saldo Atual:   R$ ${conta.consultarSaldo().toFixed(2)}`);


