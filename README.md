# marmitaria
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Modelo de Banco de Dados - Marmitaria</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background-color: #f8f9fa;
    }
    h1 {
      color: #333;
    }
    table {
      border-collapse: collapse;
      width: 100%;
      margin-bottom: 40px;
      background-color: #fff;
    }
    caption {
      caption-side: top;
      font-size: 1.2em;
      font-weight: bold;
      margin-bottom: 8px;
      color: #444;
    }
    th, td {
      border: 1px solid #ccc;
      padding: 10px;
      text-align: left;
    }
    th {
      background-color: #e9ecef;
    }
    tr:nth-child(even) {
      background-color: #f2f2f2;
    }
  </style>
</head>
<body>
  <h1>Modelo de Banco de Dados - Sistema da Marmitaria</h1>

  <!-- Tabela: produtos -->
  <table>
    <caption>produtos</caption>
    <thead>
      <tr>
        <th>Campo</th>
        <th>Tipo</th>
        <th>Descrição</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>id</td>
        <td>INT (PK, AUTO_INCREMENT)</td>
        <td>Identificador único do produto</td>
      </tr>
      <tr>
        <td>nome</td>
        <td>VARCHAR(100)</td>
        <td>Nome do produto</td>
      </tr>
      <tr>
        <td>preco</td>
        <td>DECIMAL(10,2)</td>
        <td>Preço do produto</td>
      </tr>
    </tbody>
  </table>

  <!-- Tabela: pedidos -->
  <table>
    <caption>pedidos</caption>
    <thead>
      <tr>
        <th>Campo</th>
        <th>Tipo</th>
        <th>Descrição</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>id</td>
        <td>INT (PK, AUTO_INCREMENT)</td>
        <td>Identificador único do pedido</td>
      </tr>
      <tr>
        <td>cliente</td>
        <td>VARCHAR(100)</td>
        <td>Nome do cliente</td>
      </tr>
      <tr>
        <td>data_pedido</td>
        <td>DATE</td>
        <td>Data em que o pedido foi feito</td>
      </tr>
    </tbody>
  </table>

  <!-- Tabela: itens_pedido -->
  <table>
    <caption>itens_pedido</caption>
    <thead>
      <tr>
        <th>Campo</th>
        <th>Tipo</th>
        <th>Descrição</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>id</td>
        <td>INT (PK, AUTO_INCREMENT)</td>
        <td>Identificador único do item do pedido</td>
      </tr>
      <tr>
        <td>pedido_id</td>
        <td>INT (FK → pedidos.id)</td>
        <td>Referência ao pedido</td>
      </tr>
      <tr>
        <td>produto_id</td>
        <td>INT (FK → produtos.id)</td>
        <td>Referência ao produto</td>
      </tr>
      <tr>
        <td>quantidade</td>
        <td>INT</td>
        <td>Quantidade do produto no pedido</td>
      </tr>
    </tbody>
  </table>
</body>
</html>
