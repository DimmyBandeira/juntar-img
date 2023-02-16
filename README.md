# ImgAlign

Um aplicativo da web para unir, unir ou alinhar imagens sobrepostas. Pode ser usado para criar panoramas ou para alinhar imagens, por exemplo, formulários que não foram digitalizados corretamente.

Recursos: Projeção de superfície, detecção de recursos, correspondência de recursos, ajuste de pacote, correção de onda, transferência de cor, detecção de costura e combinação multibanda.

Os algoritmos principais são retirados do OpenCV (módulos Feature2D e Stitching principalmente) e foram ajustados onde necessário. Uma versão personalizada do OpenCV foi então compilada para wasm. Para garantir uma interface do usuário sem bloqueio, todas as funções relacionadas ao OpenCV são executadas por meio de um webworker.

Prós e contras: como a união de imagens pode consumir muita memória e CPU, existem algumas limitações na quantidade ou tamanho das imagens que podem ser unidas, especialmente em dispositivos móveis. No lado positivo, a funcionalidade básica de costura está disponível em quase todos os dispositivos que podem executar um navegador. Não há necessidade de baixar um software de costura profissional. O aplicativo também é totalmente funcional offline.

## Built With

* [Vue](https://vuejs.org/) - The web framework used
* [Vuex](https://vuex.vuejs.org/) - Vue store
* [Vuetify](https://vuetifyjs.com) - Vue Material Design Component Framework
* [OpenCV](https://opencv.org/) - Open Source Computer Vision Library
* [WebAssembly](https://webassembly.org/) - Binary instruction format for a stack-based virtual machine

## Getting Started

### Prerequisites

* [NPM/Node](https://www.npmjs.com/get-npm) - NPM and Node.js

### Build instructions

* npm run build / npm run serve

Optionally opencv can be built:
* Install <a href="https://kripken.github.io/emscripten-site/docs/getting_started/downloads.html">emsdk</a> and make it available on the command line.
* Install python and make it available on the command line.
* Run build_opencv.sh, this will create an opencv wasm version and copies it to the public folder of the spa. 

## Deployment

## Contributing

## Versioning

## Authors

## License

MIT if not otherwise noted in the source files.
Be aware that Surf and Sift are patented algorithms (at least in some regions of the world).

## Acknowledgments

## Images and Screenshots

<p align="center">
  <img width="100%" src="./images/collections/Table_Collection.jpg">
</p>
<p align="center">
  <img width="100%" src="./images/collections/wz_collection.jpg">
</p>
<p align="center">
  <img width="100%" src="./images/collections/balcony_collection.jpg">
</p>
<p align="center">
  <img width="100%" src="./images/collections/collectionME.jpg">
</p>
<p align="center">
  <img width="100%" src="./screenshots/Multistitcher.jpg">
</p>
<p align="center">
  <img width="100%" src="./screenshots/matcher5.jpg">
</p>
<!-- <p align="center">
  <img width="460" src="./screenshots/matcher2.jpg">
</p>
<p align="center">
  <img width="460" src="./screenshots/matcher3.jpg">
</p>
<p align="center">
  <img width="460" src="./screenshots/comparer1.jpg">
</p> -->



