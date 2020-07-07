
# Padronização de Gateways Linkapi


## <a name='table-of-contents'>Índice</a>


## <a name='table-of-contents'>Nomenclaturas</a>
  1. [Arquivos](#names)
  1. [Variáveis](#variables)
  1. [Funções](#functions)
  1. [Construtores e Classes](#constructors)


## <a name='names'>Arquivos (custom-middlewares, data-transformations e functions).</a>

Idioma | Inglês
------------- | -------------
Objetivo  | Ser simples e objetivo, deixar explícito o que fará cada arquivo.
Padrões  | Nomenclaturas devem ser minúsculas, em caso de 2 ou mais utilizar kebab-case separando as palavras por “-” 

  - Exemplos:
  
  
![](https://i.ibb.co/FBfC2wd/Files.png)

  - Não utilizar:

![](https://i.ibb.co/m9c6k6w/bad-files.png)


**[⬆ voltar ao topo](#table-of-contents)**


## <a name='variables'>Variáveis.</a>

Idioma | Inglês
------------- | 
**Objetivo**  |Ser simples e objetivo, deixar explícito o que armazenará cada variável ou constante. 
**Padrões**  | As variáveis devem ser declaradas em minúsculo, em caso 2 ou mais palavras utilizar camelCase.   

  - Exemplos:

 ```javascript
    // ruim   
	const "Products"
	const"produtos"
	const "invoicedorders" 
	const "paid-orders"

    // bom
	const "products"
	const "customers"
	const "orders"
	const "yesterday"
	const "today"
	const "invoicedOrders"
	const "paidOrders”
    ```
**[⬆ voltar ao topo](#table-of-contents)**

## <a name='functions'>Funções</a>

Idioma | Inglês
------------- | -------------
**Objetivo**  | Ser simples e objetivo, deixar explícito o que fará a função.
**Padrões**  | As funções devem ser declaradas em minúsculo, em caso 2 ou mais palavras utilizar camelCase.   

  - Exemplos:

    ```javascript
    // ruim   
async function getCredentials(param) {
		// implementações
	}
	
	// ruim
	const getcredentials = async((param) => {
		// implementações
	});

    // bom
	const getCredentials = async((param) => {
		// implementações
	});
    ```
**- Observações: ** Sempre utilizar o mesmo nome declarado na variavel como parâmetro da função. 

```javascript
	// ruim
	const sub = "test"
	const tenant = "test"
	
	const getCredentials  = async((a, b) => {
		// implementações
	});
	await getCredentials(sub, tenant)

    // bom
	const getCredentials = async((sub, tenant) => {
		// implementações
	});
	await getCredentials(sub, tenant)

```

**[⬆ voltar ao topo](#table-of-contents)**

## <a name='constructors'>Construtores e Classes</a>

Idioma | Inglês
------------- | -------------
**Objetivo**  |Ser simples e objetivo, deixar explícito o que fará cada construtor.
**Padrões**  | Deve-se utilizar PascalCase quando nomear os construtores.   

  - Exemplos:

    ```javascript
    // ruim
function user(options) {
          this.name = options.name;
}
	
	const bad = new user({
          name: 'hernandes'
});

    // bom
function User(options) {
           this.name = options.name;
}		
const good = new User({
           name: 'hernandes'
});
    ```

**[⬆ voltar ao topo](#table-of-contents)**

