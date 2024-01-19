# Documentação do Código

**Versão:** 1.0

## Classe: Nest

Esta classe é uma versão estendida da classe `dictonary` incorporada.

**Data de Criação:** 15-11-2020

**Data de Alteração:** 05-10-2021

**Autor:** Sibra-Soft - Alex van den Berg

### Atributos Privados

- `mCol`: Uma instância da classe `Collection`.

### Métodos e Propriedades

1. **Clear**: Este método limpa a coleção.

2. **Exists(sItem As String, sKey As String)**: Este método verifica se um item ou chave existe na coleção. Se ambos os parâmetros forem passados, um erro é acionado, pois apenas um dos dois pode ser procurado por vez.

3. **Add(Item As Variant, sKey As String, Before As Variant, After As Variant)**: Este método adiciona um novo item à coleção. Se o item for um objeto, ele será adicionado como tal, caso contrário, seu valor será adicionado. Se uma chave for fornecida, o item será adicionado com essa chave. O item pode ser adicionado antes ou depois de um item específico, se especificado.

4. **Item(vntIndexKey As Variant) As Variant**: Esta propriedade retorna o item na posição `vntIndexKey`.

5. **ItemKey(vntIndexKey As Variant) As String**: Esta propriedade retorna a chave do item na posição `vntIndexKey`.

6. **Count As Long**: Esta propriedade retorna o número de elementos na coleção.

7. **Remove(vntIndexKey As Variant)**: Este método remove o item na posição `vntIndexKey` da coleção.

8. **Class_Initialize**: Este método é chamado quando a classe é instanciada. Ele inicializa a coleção.

9. **Class_Terminate**: Este método é chamado quando a classe é destruída. Ele limpa a coleção.

### Erros

- Erro 9: Você deve especificar um nome de item ou chave para encontrar.
- Erro 10: Você só pode encontrar uma das duas opções.