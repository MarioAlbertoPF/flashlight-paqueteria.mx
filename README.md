# flashlight-paqueteria.mx
<script>

let baseDatos = {
  "FL123456MX": {
    estado: "En tránsito 🚚",
    ubicacion: "CDMX",
    entrega: "24 horas"
  },
  "FL654321MX": {
    estado: "Entregado ✅",
    ubicacion: "Toluca",
    entrega: "Completado"
  }
};

function buscarPaquete(){
  let guia = document.getElementById("trackingInput").value.toUpperCase()
  let resultado = document.getElementById("resultado")

  if(baseDatos[guia]){
    let data = baseDatos[guia]
    resultado.style.display="block"
    resultado.innerHTML = `
      <b>Guía:</b> ${guia}<br><br>
      <b>Estado:</b> ${data.estado}<br>
      <b>Ubicación:</b> ${data.ubicacion}<br>
      <b>Entrega:</b> ${data.entrega}
    `
  } else {
    resultado.style.display="block"
    resultado.innerHTML="Guía no encontrada ❌"
  }
}

</script>
