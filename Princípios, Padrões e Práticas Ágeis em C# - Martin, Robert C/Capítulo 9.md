# Princípio do Aberto/Fechado (OCP)

O **Princípio do Aberto/Fechado (OCP)** afirma que **entidades de software (classes, módulos, funções, etc.) devem ser abertas para ampliação, mas fechadas para modificação**.
Isso significa que, diante de mudanças, devemos **adicionar código novo**, sem precisar alterar o código antigo que já funciona.

---

## Problema que o OCP resolve
- Quando uma única mudança gera modificações em vários módulos dependentes, temos **rigidez no design**.  
- O OCP orienta que o sistema seja refatorado para evitar esse efeito em cascata.  

---

## Características de módulos que seguem o OCP
1. **Abertos para ampliação** → permitem novos comportamentos.  
2. **Fechados para modificação** → o código existente permanece intacto.  

Isso parece contraditório, mas é possível graças à **abstração**.  
- Em C# ou em qualquer outra linguagem de programação orientada a objetos, é possível criar **abstrações fixas** que permitem diferentes implementações futuras.  
- Assim, um módulo pode depender de uma interface ou classe abstrata, sendo protegido contra mudanças internas das implementações concretas.  

---

## Como se preparar para mudanças
- No passado, usava-se o conceito de “**inserir ganchos**” para prever mudanças, mas isso frequentemente gerava complexidade desnecessária.  
- A abordagem correta é **não prever tudo**:  
  - “**Engane-me uma vez**”: o código nasce simples, e ao aparecer uma mudança, refatoramos criando abstrações que previnem futuras alterações do mesmo tipo.  

---

## Estimulando mudanças
Para identificar cedo quais alterações são prováveis, é importante:  
- **Escrever testes primeiro** → garante que o sistema seja testável e preparado para mudanças.  
- **Usar ciclos curtos de desenvolvimento** → dias em vez de semanas.  
- **Construir funcionalidades antes da infraestrutura** → mostrar cedo o valor ao cliente.  
- **Priorizar as funcionalidades mais importantes**.  
- **Entregar cedo e frequentemente** → receber feedback real e rápido dos usuários.  

---

## Conclusão
- O OCP é **central na orientação a objetos**, pois garante **flexibilidade, reutilização e manutenção** do software.  
- Entretanto:  
  - Usar uma linguagem orientada a objetos não garante, por si só, o respeito ao OCP.  
  - **Exagerar em abstrações é tão ruim quanto não usá-las.**  
  - O ideal é aplicar abstração apenas em **áreas do sistema que mudam com frequência**.  

---

## Minha Opinião
Gostei da ideia de não complicar o código logo no início, mas sim aprender com as mudanças e criar abstrações somente quando necessário. Isso deixa o software mais limpo e fácil de manter.
