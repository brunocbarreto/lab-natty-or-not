# Podcast: Podcast - Descomplicando APIs em C# em 10 Minutos 🎙️

## 📒 Descrição
Este podcast de 10 minutos oferece um passeio rápido, mas profundo, pelas APIs utilizando a linguagem C#.

## 🤖 Tecnologias Utilizadas
- IA Generativa **[ChatGPT](https://chat.openai.com)** para roteirização e geração do conteúdo;
- IA Generativa **[ElevenLabs](https://www.elevenlabs.io)** para a sintetização de voz;
- Software **[Descript](https://www.descript.com)** para edição e montagem do podcast.

## 🧐 Processo de Criação
"ChatGPT" foi utilizado para desenvolver o roteiro e gerar o conteúdo do podcast. "ElevenLabs" ajudou a criar uma voz sintética envolvente para a narração , enquanto o "Descript" foi essencial para a edição final, garantindo um fluxo suave e profissional.

## 🚀 Resultados
O episódio é uma introdução acessível e estimulante ao campo das IAs Generativas, ideal para quem busca uma compreensão rápida do assunto.

[LINK PARA A PARTE 1 DO PODCAST AQUI](https://share.descript.com/view/pax5QjAG3x8){target="_blank"}

~~~c#
using Microsoft.AspNetCore.Mvc;
using System.Collections.Generic;

[Route("api/[controller]")]
[ApiController]
public class ProductsController : ControllerBase
{
    private static readonly List<string> Products = new List<string>
    {
        "Product1", "Product2", "Product3"
    };

    // GET: api/products
    [HttpGet]
    public ActionResult<IEnumerable<string>> Get()
    {
        return Products;
    }

    // POST: api/products
    [HttpPost]
    public ActionResult AddProduct([FromBody] string product)
    {
        Products.Add(product);
        return Ok();
    }

    // PUT: api/products/1
    [HttpPut("{id}")]
    public ActionResult UpdateProduct(int id, [FromBody] string product)
    {
        if (id >= Products.Count)
        {
            return NotFound();
        }
        Products[id] = product;
        return Ok();
    }

    // DELETE: api/products/1
    [HttpDelete("{id}")]
    public ActionResult DeleteProduct(int id)
    {
        if (id >= Products.Count)
        {
            return NotFound();
        }
        Products.RemoveAt(id);
        return Ok();
    }
}
~~~

[LINK PARA A PARTE 2 DO PODCAST AQUI](https://share.descript.com/view/26LXvaUaXvH){target="_blank"}

## 💭 Reflexão
O projeto destacou a versatilidade das IAs Generativas na criação de conteúdo auditivo, abrindo novos caminhos para a produção de mídia digital.
