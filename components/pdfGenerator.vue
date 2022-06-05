<template>
  <div>
    <my-btn text="Generar PDF" color="secondary" :action="writePdf" />
  </div>
</template>

<script>
// import fs from 'fs'
// import JsPDF from 'jspdf'
// import 'jspdf-autotable'
import { degrees, PDFDocument, rgb, StandardFonts } from 'pdf-lib'
import download from 'downloadjs'
import MyBtn from './buttons/myBtn.vue'
export default {
  components: { MyBtn },
  props: {
    giftBookText: {
      type: String,
      default: 'Hola coca cola',
    },
  },
  data() {
    return {
      pdf: null,
    }
  },
  methods: {
    async writePdf() {
      // This code belongs to jsPDF plugin
      // const doc = new JsPDF({
      //   orientation: 'p',
      //   unit: 'mm',
      //   format: 'a4',
      // })
      // const text = this.giftBookText
      // const page = {
      //   width: 190,
      //   leftM: 25,
      //   rightM: 25,
      //   topM: 30,
      //   bottomM: 20,
      // }
      // doc.setFont('helvetica', 'italic')
      // doc.setFontSize(16)
      // const lines = doc.splitTextToSize(
      //   text,
      //   page.width - page.leftM - page.rightM
      // )
      // doc.addPage()
      // doc.text(page.leftM, page.topM, lines)
      // doc.save('testing-doc.pdf')

      try {
        const url = 'https://pdf-lib.js.org/assets/with_update_sections.pdf'
        const currentPdf = await fetch(url).then((res) => res.arrayBuffer())
        const pdfDoc = await PDFDocument.load(currentPdf)
        const helveticaFont = await pdfDoc.embedFont(StandardFonts.Helvetica)

        // const pages = pdfDoc.getPages()
        const newPage = pdfDoc.addPage()
        const { width, height } = newPage.getSize()
        const message = this.giftBookText

        newPage.drawText(message, {
          x: width / 2 - 100,
          y: height / 2 + 300,
          size: 16,
          font: helveticaFont,
          color: rgb(0, 0, 0.5),
          rotate: degrees(0),
        })
        const pdfBytes = await pdfDoc.save()
        download(
          pdfBytes,
          'pdf-lib_modification_example.pdf',
          'application/pdf'
        )
      } catch (error) {
        throw new Error(error)
      }

      // eslint-disable-next-line no-undef
    },
  },
}
</script>
