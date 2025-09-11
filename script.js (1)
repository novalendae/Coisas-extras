document.addEventListener("DOMContentLoaded", async () => {
  const container = document.getElementById("links-container");
  const jsonURL = "https://raw.githubusercontent.com/novalendae/Links-dos-apps-e-sites/main/arquivos.json";
  
  try {
    const response = await fetch(jsonURL);
    const links = await response.json();
    
    links.forEach(link => {
      const card = document.createElement("div");
      card.className = "link-card";
      
      card.innerHTML = `
        <img src="${link.img}" alt="${link.titulo}" class="link-img">
        <h2>${link.titulo}</h2>
        <p>${link.descricao}</p>
        <a href="${link.url}" target="_blank">Acessar</a>
      `;
      
      container.appendChild(card);
    });
  } catch (error) {
    console.error("Erro ao carregar links:", error);
  }
});