<template>
  <div class="curso-main-container referencias">
    <BannerInterno
      icono="fas fa-book"
      titulo="Referencias bibliográficas"
    ></BannerInterno>
    <div class="container tarjeta tarjeta--blanca p-4 p-md-5 mb-5">
      <div v-for="ref in orderedData" :key="ref.link" class="referencias__item">
        <span v-html="ref.referencia"></span
        ><a v-if="ref.link" class="ms-1" :href="ref.link" target="_blank"
          ><span v-html="ref.link"></span
          ><i class="ms-1 fas fa-external-link-alt"></i
        ></a>
        <hr class="my-3" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Referencias',
  data: () => ({
    referencias: [
      {
        referencia:
          'Agrosavia.co. (n.d.). [Documento PDF]. Recuperado el 16 de junio de 2025, de',
        link:
          'https://repository.agrosavia.co/bitstream/handle/20.500.12324/38661/Ver_Documento_38661.pdf?sequence=4&isAllowed=y',
      },
      {
        referencia:
          'AI in Business (IA en la empresa) [@Al_Busines]. (n.d.). Supervisión automática de maquinaria: Mantenimiento predictivo y eficiencia energética. [Video]. Youtube. Recuperado el 16 de junio de 2025, de',
        link: 'https://www.youtube.com/watch?v=qVhRbyPsh7Q',
      },
      {
        referencia:
          'Amazon Web Services [@amazonwebservices]. (s/f). Introducción a AWS IoT. [Video]. Youtube. Recuperado el 16 de junio de 2025, de',
        link: 'https://www.youtube.com/watch?v=ywne0g-9ZWY',
      },
      {
        referencia:
          'Baker, M. (2020). Cloud Platforms for IoT: An Overview. IoT World Today.',
        link: 'https://www.iotworldtoday.com/',
      },
      {
        referencia:
          'Digi-Key Electronics. (2019). Power Saving Techniques for IoT Devices. Digi-Key.',
        link: 'https://www.digikey.com/',
      },
      {
        referencia:
          'Domotics, I. [@INNOVADOMOTICS]. (n.d.). ESP32 - Introducción y Aplicaciones - Guía Completa. [Video]. Youtube. Recuperado el 16 de junio de 2025, de',
        link: 'https://www.youtube.com/watch?v=gbntchCgXSs',
      },
      {
        referencia:
          'Edu.ec. (n.d.). [Documento PDF]. Recuperado el 15 de junio de 2025, de',
        link:
          'https://dspace.ups.edu.ec/bitstream/123456789/19349/1/UPS-CT008847.pdf',
      },
      {
        referencia:
          'Go, I. to [@instrumentacion_industrial]. (n.d.). Términos del control de procesos. [Video]. Youtube. Recuperado el 15 de junio de 2025, de',
        link: 'https://www.youtube.com/watch?v=LUi0HEXKnjo',
      },
      {
        referencia:
          'Google Cloud. (2021). Getting Started with Google Cloud IoT Core. Google Cloud.',
        link: 'https://cloud.google.com/iot-core/docs/quickstart',
      },
      {
        referencia:
          'IoT protocols: A comprehensive guide. (2024, septiembre 9). A1 Digital; #creator.',
        link:
          'https://www.a1.digital/knowledge-hub/iot-protocols-a-comprehensive-guide/',
      },
      {
        referencia:
          'Isc, E. [@EDUCATRONICOSISC]. (n.d.). ¿Qué es el IOT? - Definición, Topología, Características y Aplicaciones. [Video]. Youtube. Recuperado el 13 de junio de 2025, de',
        link:
          'https://www.youtube.com/watch?v=gzM15itxUzU&list=PLts8p0-b9wstwo9hkW2z1Z1pr5R_1OguW',
      },
      {
        referencia:
          'Isc, E. [@EDUCATRONICOSISC]. (n.d.). LoRa y LoRaWAN - El futuro del IOT. [Video]. Youtube. Recuperado el 15 de junio de 2025, de ',
        link: 'https://www.youtube.com/watch?v=TE5__LDPtaw&t=24s',
      },
      {
        referencia:
          'Lo Ra y GPRS, C. E. (n.d.). Análisis de sistemas IoT en entorno agrícola. [Documento PDF]. Uoc.edu. Recuperado el 16 de junio de 2025, de',
        link:
          'https://openaccess.uoc.edu/server/api/core/bitstreams/5942ab0a-6557-4dc3-b345-78e2f5a29244/content',
      },
      {
        referencia:
          'MathWorks. (2021). Visualizing IoT Data with ThingSpeak. MathWorks.',
        link: 'https://www.mathworks.com/help/thingspeak',
      },
      {
        referencia:
          'Mathworks.com. (n.d.). Recuperado el 15 de junio de 2025, de',
        link: 'https://www.mathworks.com/help/thingspeak/getting-started.html',
      },
      {
        referencia:
          'Microsoft.com. (n.d.). Recuperado el 14 de junio de 2025, de',
        link:
          'https://azure.microsoft.com/es-es/solutions/iot/iot-technology-protocols',
      },
      {
        referencia:
          'Ortiz Arciniega, J. L., Valencia Barahona, F. X., Bosmediano Cárdenas, C. P., Bastidas Jácome, A. D., Aguirre Chagna, V. H., & Jácome Ayala, P. J. (2025). ESP32: Manual Básico para Estudiantes. [Documento PDF]. Alumni Editora.',
        link: 'https://doi.org/10.70625/alumned/9',
      },
      {
        referencia:
          'SparkFun. (2021). DHT11 and DHT22 Sensors Explained. SparkFun.',
        link: 'https://learn.sparkfun.com/tutorials/ ',
      },
      {
        referencia:
          'Vista de Agricultura de Precisión: La integración de las TIC en la producción Agrícola. (n.d.). [Documento PDF]. Edu.co. Recuperado el 16 de junio de 2025, de',
        link:
          'https://revistascientificas.cuc.edu.co/CESTA/article/view/3978/4013 ',
      },
      {
        referencia:
          'Weg.net. (n.d.). [Documento PDF]. Recuperado el 15 de junio de 2025, de',
        link:
          'https://static.weg.net/medias/downloadcenter/hf4/h7d/WEG-sensores-industriales-50094674-es.pdf',
      },
      {
        referencia:
          'Wokwi - World’s most advanced ESP32 Simulator. (s/f). Wokwi.com. Recuperado el 14 de junio de 2025, de',
        link: 'https://wokwi.com/ ',
      },
      {
        referencia: 'Tme.eu. (n.d.). Recuperado el 16 de junio de 2025, de',
        link:
          'https://www.tme.eu/es/news/library-articles/page/53063/no-solo-wi-fi-estandares-de-comunicacion-inalambrica-en-iot/ ',
      },
    ],
  }),
  computed: {
    orderedData() {
      return [...this.referencias].sort((a, b) => {
        const afl = this.quitarAcentos(a.referencia.split(' ')[0].toLowerCase())
        const bfl = this.quitarAcentos(b.referencia.split(' ')[0].toLowerCase())
        if (afl < bfl) return -1
        if (afl > bfl) return 1
        return 0
      })
    },
  },
  methods: {
    quitarAcentos(str) {
      return str.normalize('NFD').replace(/[\u0300-\u036f]/g, '')
    },
  },
}
</script>

<style lang="sass">
.referencias
  &__item
    &:last-child
      hr
        display: none
    a
      color: $blue
      text-decoration: underline
      overflow-wrap: break-word
</style>
