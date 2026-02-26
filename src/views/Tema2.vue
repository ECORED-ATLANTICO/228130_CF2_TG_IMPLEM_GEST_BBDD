<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span 2
      h1 Restauración de bases de datos

    .row.justify-content-center.mb-5
      .col-lg-10
        .bloque-texto-g.color-acento-botones.p-3.p-sm-4.p-md-4
          .col-lg-4
            .bloque-texto-g__img(
              :style="{'background-image': `url(${require('@/assets/curso/temas/T2/img-1.png')})`}"
            )
          .col-lg-8
            .contenedor-dashed.p-3
              .bloque-texto-g1__texto.p-3
                p.mb-3 Como se ha mencionado, las bases de datos están expuestas a daños inesperados, esto hace necesario contar con planes para la recuperación de un error, una base de datos de SQL. Cuando esto sucede, es deber del administrador realizar un plan de contingencia haciendo la restauración, es decir, un conjunto de copias de seguridad de SQL en una secuencia lógica de restauración correcta y significativa.
                p SQL permite restaurar los datos de las copias de seguridad de toda una base de datos, un archivo de datos o una página de datos, tal y como se describe a continuación:


    h3.titulo-tercero(data-aos="fade-right") Restauración de bases de datos completa

    .row.mb-5.align-items-center.justify-content-center
      .col-6.col-md-2.col-lg-1.mb-3.mb-lg-0
        figure
          img(data-aos='fade-right')(src='@/assets/curso/temas/T2/img-2.svg', alt='')
      .col-md-10.col-lg-11
        p.mb-0 Se restaura y recupera toda la base de datos que permanece sin conexión, esta acción se ejecuta cuando más del 50% de los datos se han dañado o se presume que lo hicieron.

    h3.titulo-tercero(data-aos="fade-right") Restauración bases de datos SQL. MySQL

    p.mb-5 Para las copias de seguridad con MySQL, se debe crear una base de datos nueva para guardar la información de la copia del archivo de respaldo que se ha generado en un repositorio o carpeta. La generación de este archivo se puede definir, según la metodología de seguridad de bases de datos, que puede ser por meses, semanas o días. Se debe realizar de la siguiente manera:

    TabsC.color-acento-contenido.mb-5
      .py-3.py-md-4(titulo="Paso 1")
        .row.justify-content-around.align-items-center.p-4
          .col-lg-4.mb-4.mb-lg-0
            figure
              img(src='@/assets/curso/c1.svg', alt='En la imagen se muestra la sintaxis para la creación de bases de datos. ')
          .col-lg-6
            p Creación base de datos ejercicio 1.

      .py-3.py-md-4(titulo="Paso 2")
        .row.justify-content-around.align-items-center.p-4
          .col-lg-6.mb-4.mb-lg-0
            figure
              img(src='@/assets/curso/c2.svg', alt='En la imagen se muestra la sintaxis para la copia de seguridad de bases de datos. ')
          .col-lg-6
            p Copia de seguridad base de datos

    h3.titulo-tercero(data-aos="fade-right") Restauración de bases de datos NoSQL

    .row.justify-content-center.mb-5
      .col-lg-10
        .cajon.color-acento-contenido.p-4.mb-4(style="background-color: #fff4da")
          .row.justify-content-center
            .col-4.col-md-2.col-lg-1.mb-3.mb-lg-0: img(src='@/assets/curso/c3.svg', alt='')
            .col-lg-10
              h4 Actualización de MongoDB
              p “A partir de MongoDB 4.4, mongorestore ahora se lanza por separado del servidor MongoDB y utiliza su propio control de versiones, con una versión inicial de 100.0.0. Previamente, mongorestore se lanzó junto con el servidor MongoDB y utilizó versiones coincidentes”, (mongodb, 2022).
    p.mb-5 A continuación, se presenta el paso a paso, para realizar la restauración de una base de datos en MongoDB:

    .row.mb-5.md-5.justify-content-center.align-items-center
      .col-6.col-md-2.col-lg-1.mb-3.mb-lg-0
        figure
          img(data-aos='fade-right')(src='@/assets/curso/temas/T2/img-6.svg', alt='')

      .col-md-10.col-lg-11
        p.mb-0 En primer lugar, es necesario que exista un archivo con la copia de la base de datos; paso seguido, se realiza el borrado de la base de datos dañada, con la sintaxis db.dropDatabase(); después, se crea la base de datos en MongoDBCompass (Interfaz gráfica), dando clic en el botón ‘create databases’ y aparece entonces, un cuadro para agregar bases de datos y colección; luego, se selecciona la opción ‘Import Data’, seguido de “agregar datos desde archivo de backup .csv”, y de esta manera queda el registro de datos, en la nueva base de datos.


    .tarjeta.tarjeta--gris.p-4
      LineaTiempoC.color-primario
        .row.justify-content-around.align-items-center(titulo="Paso 1")
          .col-lg-6.mb-4.mb-lg-0
            p Ver bases de datos <i>MongoDBCompass</i>

          .col-lg-6
            figure
              img(src='@/assets/curso/temas/T2/img-7.png', alt='En la figura se muestran las base de datos de MongoDBCompass.')


        .row.justify-content-around.align-items-center(titulo="Paso 2")
          .col-lg-6.mb-4.mb-lg-0
            p Creación de bases de datos

          .col-lg-6
            figure
              img(src='@/assets/curso/temas/T2/img-8.png', alt='En la figura se muestran la creación de base de datos.')

        .row.justify-content-around.align-items-center(titulo="Paso 3")
          .col-lg-6.mb-4.mb-lg-0
            p Seguido, encuentra la ventana para nombrar bases de datos, en este caso se llamará ‘ejercicio1’

          .col-lg-6
            figure
              img(src='@/assets/curso/temas/T2/img-9.png', alt='En la figura se muestran la interfaz para nombrar la base de datos.')

        .row.justify-content-around.align-items-center(titulo="Paso 4")
          .col-lg-6.mb-4.mb-lg-0
            p Importar datos

          .col-lg-6
            figure
              img(src='@/assets/curso/temas/T2/img-10.png', alt='En la figura se muestran la opción de importar datos desde la base de datos.')

        .row.justify-content-around.align-items-center(titulo="Paso 5")
          .col-lg-6.mb-4.mb-lg-0
            p Agregar datos desde archivo

          .col-lg-6
            figure
              img(src='@/assets/curso/temas/T2/img-11.png', alt='En la figura se muestran la opción de agregar datos desde un archivo.')

        .row.justify-content-around.align-items-center(titulo="Paso 6")
          .col-lg-6.mb-4.mb-lg-0
            p Aparece la ventana de datos importados

          .col-lg-6
            figure
              img(src='@/assets/curso/temas/T2/img-12.png', alt='En la figura se muestran la pantalla con los datos que fueron importados.')


</template>

<script>
export default {
  name: 'Tema2',
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
