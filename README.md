# FIFA-FC-Nostalgic-Revival
const http = require('http');
const port = process.env.PORT || 3000; 

const server = http.createServer((req, res) => {
  console.log(`Petición recibida en: ${req.url}`);
  res.setHeader('Access-Control-Allow-Origin', '*');
  res.setHeader('Access-Control-Allow-Methods', 'GET, POST, OPTIONS');
  res.setHeader('Content-Type', 'application/json');
  res.statusCode = 200;
  res.end(JSON.stringify({ status: "success", message: "Conectado al FIFA/FC Nostalgic Revival" }));
});

server.listen(port, '0.0.0.0', () => {
  console.log(`Servidor en línea`);
});

