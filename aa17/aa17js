window.addEventListener("load", () => {
  loadProducts();
});

async function loadProducts() {
  try {
    const response = await fetch("aa16.json");

    if (!response.ok) {
      throw new Error("Error al cargar el archivo JSON");
    }

    const products = await response.json();
    renderProducts(products);

  } catch (error) {
    console.error("Hubo un problema:", error);
  }
}

function renderProducts(products) {
  const container = document.querySelector("#container");

  let htmlContent = "";

  products.forEach(product => {
    htmlContent += `
      <div class="product-card">
        <img src="${product.img}" alt="${product.name}">
        <div class="info">
          <h3>${product.name}</h3>
          <p class="price">$${product.price}</p>
        </div>
      </div>
    `;
  });

  container.innerHTML = htmlContent;
}
