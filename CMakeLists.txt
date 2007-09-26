PROJECT(LDRD2006 NONE)

INCLUDE(UseLATEX.cmake)

LATEX_COPY_GLOBBED_FILES(${CMAKE_CURRENT_SOURCE_DIR}/SANDreport/*.cls .)
LATEX_COPY_GLOBBED_FILES(${CMAKE_CURRENT_SOURCE_DIR}/SANDreport/*.sty .)
LATEX_COPY_GLOBBED_FILES(${CMAKE_CURRENT_SOURCE_DIR}/SANDreport/*.eps .)
LATEX_COPY_GLOBBED_FILES(${CMAKE_CURRENT_SOURCE_DIR}/SANDreport/*.pdf .)

SET(images
  images/GSpaceExampleGraph.pdf
  images/GSpaceExampleBFS.pdf
  images/GSpaceExamplePlot.pdf
  images/GSpaceExampleFeatures.pdf
  images/GSpaceExampleRotated.pdf
  images/GSpaceEnron.png
  images/GSpaceVBForceDirected.pdf
  images/GSpaceVBVertexBundles.pdf
  images/GSpaceBundlingOriginal.png
  images/GSpaceBundlingBreakout.png
  images/GSpaceBundleMap.pdf
  images/GSpaceBundlingInsets.png
  images/GSpaceComparison.png
  images/EdgeAccEnronNoBlend.png
  images/EdgeAccEnronPixelBlend.png
  images/EdgeAccEnronEdgeFrequency.png
  )

ADD_LATEX_DOCUMENT(LDRD2006.tex
  BIBFILES LDRD2006.bib
  IMAGES ${images}
  USE_INDEX
  )
