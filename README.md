let nomeHeroi = ["Capitão América", "Batman", "Mulher Maravilha", "Superman", "Morte", "Jesus"];
let xpHeroi = [3950, 5030, 6000, 7500, 9999, 1000000];


// Função para calcular o nível com base na experiência
function calcularNivel(xp) {
  // Objeto que mapeia os intervalos de experiência para os níveis correspondentes
  const niveis = {
    Ferro: { min: 0, max: 1000 },
    Bronze: { min: 1001, max: 2000 },
    Prata: { min: 2001, max: 5000 },
    Ouro: { min: 5001, max: 7000 },
    Platina: { min: 7001, max: 8000 },
    Ascendente: { min: 8001, max: 9000 },
    Imortal: { min: 9001, max: 10000 },
    Radiante: { min: 10001, max: Infinity }, // Infinity representa um valor maior que 10000
  };


  // Itera sobre os níveis e verifica em qual intervalo de experiência o valor se encaixa
  for (let nivel in niveis) {
    if (xp >= niveis[nivel].min && xp <= niveis[nivel].max) {
      return nivel; // Retorna o nome do nível encontrado
    }
  }
}


// Laço de repetição para processar cada herói
for (let i = 0; i < nomeHeroi.length; i++) {
  let nome = nomeHeroi[i];
  let xp = xpHeroi[i];
  let nivel = calcularNivel(xp); // Calcula o nível do herói com base na experiência


  // Imprime o resultado no console
  console.log(`O Herói de nome ${nome} está no nível ${nivel}`);
}# dESAFIO-fELIP-O
