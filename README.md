# README.md

## Descrição
Este é um programa simples escrito em C++ que realiza uma busca linear em um vetor para encontrar um valor específico (`target`). Se o valor for encontrado, ele retorna o índice do valor no vetor. Caso contrário, retorna `-1`. O índice encontrado é então impresso no console.

## Explicação do Código
1. **Include e Namespace:**
   - `#include<bits/stdc++.h>`: Inclui todas as bibliotecas padrão do C++.
   - `using namespace std`: Usa o namespace padrão para evitar prefixos como `std::`.

2. **Função `busca`:**
   - Recebe um vetor `lista` e um valor `target` como parâmetros.
   - Itera sobre cada elemento do vetor.
   - Se encontrar o valor `target`, retorna seu índice.
   - Se não encontrar o valor, retorna `-1`.

3. **Função `main`:**
   - Define o valor `target` como `10`.
   - Cria um vetor `lista` com os valores de `1` a `10`.
   - Chama a função `busca` para encontrar o índice do `target` no vetor `lista`.
   - Verifica se o índice retornado é `-1` (não encontrado).
   - Imprime o índice se o valor for encontrado, caso contrário, imprime uma linha em branco.

### Código Completo

```cpp
#include<bits/stdc++.h>
using namespace std;

int busca(vector<int> lista, int target){
    for(int i = 0; i < lista.size(); i++){
        if(lista[i] == target){
            return i;
        }
    }
    return -1;
}

int main()
{
    int target = 10;
    
    vector<int> lista = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    
    int indice = busca(lista, target);
    
    if(indice == -1){
        cout << endl;
    }else{
        cout << indice << endl;
    }

    return 0;
}
```
