<template lang="pug">
.curso-main-container.pb-3
  BannerInterno(icono="fas fa-sitemap" titulo="Síntesis")
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5

    p El siguiente mapa integra los criterios y especificidades de los conocimientos expuestos en el presente componente formativo:

    .row.justify-content-center
      .col-lg-10.mb-5
        figure
          img(src="@/assets/curso/temas/sintesis.png", alt="En la gestión de BD SQL encontramos: 1. Planificación: considerar la estructura de BD origen. 2. Contador de registro: conteo de los registros existentes. 3. Mapeador de tipo de datos: mapeo de campor la nueva BD. 4. Restricciones y triggers: deshabilitar trigers y restricciones para migración. 5.Codificación de caracteres: codificar caracteres a la nueva base de datos. 6. Pruebas: aplicadas para tener la certeza que no existen ausencia de datos. 7. Implementación: poner en marcha la migración. 8. Monitoreo: observación constante en el proceso de migración.")
      .col-auto
        a.anexo.mb-4(:href="obtenerLink('/downloads/Sintesis.pdf')" target="_blank")
          .anexo__icono
            img(src="@/assets/template/icono-pdf.svg")
          .anexo__texto
            p Anexo. Síntesis

</template>

<script>
export default {
  name: 'Sintesis',
  data: () => ({
    // variables de vue
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
}
</script>

<style lang="sass"></style>
