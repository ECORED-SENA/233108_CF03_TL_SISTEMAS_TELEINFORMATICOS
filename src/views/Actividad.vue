<template lang="pug">
  .curso-main-container.pb-3
    BannerInterno(icono="far fa-question-circle" titulo="Actividad didáctica")
    .container.tarjeta.tarjeta--blanca.p-4.p-md-5
      // Para cuestionario usar: <ActividadController :cuestionario="cuestionario"/>
      // Para parrafo usar: <ActividadController :parrafo="parrafo"/>
      #Actividad                
      <ActividadController :cuestionario="cuestionario"/>

</template>

<script>
import ActividadController from '@ecored-sena/boulder-kit/plugin/components/actividad/ActividadController.vue'

export default {
  name: 'ActividadDidactica',
  components: {
    ActividadController,
  },
  data: () => ({
    cuestionario: {
      tema: 'Gestión de equipos de cómputo',
      titulo: 'Cuestionario',
      introduccion:
        '<b>Objetivo:</b> apropiarse de los conceptos más importantes asociados a la gestión de equipos de cómputo con el fin de aplicarlos en el mantenimiento y limpieza de los mismos.',
      barajarPreguntas: false,
      titulo_aprobado: '¡BUEN TRABAJO!',
      titulo_reprobado: 'VUELVA A INTENTARLO',
      preguntas: [
        {
          id: 1,
          texto:
            '¿Cuál es el componente electrónico encargado de transformar la corriente de la red eléctrica con una tensión de 200V o 125V, a una corriente con una tensión de 5 a 12 voltios?',
          imagen: '@/assets/actividad/imagen1.png',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Placa base.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'BIOS .',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Fuente de alimentación.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Antivirus.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto:
            'Lo sentimos, su respuesta no es la correcta. <em>Board</em> del <em>software</em> EAGLE.',
        },
        {
          id: 2,
          texto: '¿Cuál es el cerebro del computador?',
          imagen: '@/assets/actividad/imagen2.png',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Fuente de alimentación.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Procesador.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Batería.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'USB.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 3,
          texto:
            '¿Cuál elemento o elementos de limpieza se utilizan para limpiar los diferentes componentes de la computadora sin dejar raspaduras ni residuos?',
          imagen: '@/assets/actividad/imagen3.png',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Paño suave.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Aire comprimido.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Toalla de manos.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'a y b son correctas.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 4,
          texto:
            '¿Cuáles son las acciones de mantenimiento de un equipo informático?',
          imagen: '@/assets/actividad/imagen4.png',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Ingresar modo seguro.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Eliminar archivos temporales.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Desconectar el P.C.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'a y b son correctas.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 5,
          texto:
            'Una de estas acciones no hace parte de las herramientas a tener cuando se trabaja en una computadora, ¿cuál es?',
          imagen: '@/assets/actividad/imagen1.png',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Muñequera antiestática o esd, herramientas informáticas imprescindibles, herramientas informáticas imprescindibles.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Destornillador, destornillador phillips y destornillador torx o broca, linterna, bolsas antiestáticas vacías.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Tener mascotas al lado del P.C para trabajar más tranquilo y comer en el sitio de trabajo para optimizar el tiempo.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto:
                'Paño sin pelusa, soldador de bajo voltaje, mecha y carrete, cortacables y pelacables, pinzas o recogedor de piezas, pistola de temperatura.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 6,
          texto:
            '¿Cuáles son procesos de mantenimiento del software informático?',
          imagen: '@/assets/actividad/imagen2.png',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Siempre apague, apague el sistema antes de realizar cualquier mantenimiento de la computadora.  ',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Use una aspiradora para eliminar la suciedad, el polvo, los alimentos y el cabello de los teclados. Se recomienda usar una muñequera antiestática para reducir la transferencia de electricidad estática del cuerpo a la computadora.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'a y son correctas. ',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Ninguna situación presentada tiene relación.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 7,
          texto:
            '¿Cuáles de estos manuales podemos encontrar en una organización?',
          imagen: '@/assets/actividad/imagen3.png',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Manuales de instalación, operación y mantenimiento.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Manuales de acondicionamiento.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Manuales de desempeño.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Manuales de preciosa y costos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 8,
          texto: '¿Qué se incluye en un manual de operación y mantenimiento?',
          imagen: '@/assets/actividad/imagen4.png',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Todas las anteriores.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Información general: audiencia, terminología, alcance de un manual, etc.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Características operativas de la maquinaria',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Especificaciones técnicas del equipo',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
      ],
      mensaje_final_aprobado: '¡Excelente! Ha superado la actividad.',
      mensaje_final_reprobado:
        'Le recomendamos volver a revisar el componente formativo e intentar nuevamente la actividad didáctica.',
    },
  }),
}
</script>
