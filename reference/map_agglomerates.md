# Mapa de indicadores por aglomerado

Mapa de indicadores por aglomerado

## Uso

``` r
map_agglomerates(
  .data,
  agglomerates,
  indicator,
  alpha = 0.75,
  palette = "viridis"
)
```

## Argumentos

- .data:

  Dataframe con los datos

- agglomerates:

  Variable con los codigos de aglomerados

- indicator:

  Variable con los indicadores

- alpha:

  Opacidad de los puntos

- palette:

  Paleta de colores a utilizar, incluye "viridis", "magma", "inferno",
  or "plasma". Para mas opciones, ver
  [colorNumeric](https://rstudio.github.io/leaflet/reference/colorNumeric.html)

## Valor

Devuelve un mapa de indicadores por aglomerado

## Ejemplos

``` r

toybase_individual_2016_04 %>%
  dplyr::group_by(AGLOMERADO) %>%
  dplyr::summarise(tasa_actividad = sum(PONDERA[ESTADO == 1]) / sum(PONDERA)) %>%
  map_agglomerates(
    agglomerates = AGLOMERADO,
    indicator = tasa_actividad
  )
#> Assuming "lon" and "lat" are longitude and latitude, respectively

{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"https://openstreetmap.org/copyright/\">OpenStreetMap<\/a>,  <a href=\"https://opendatacommons.org/licenses/odbl/\">ODbL<\/a>"}]},{"method":"addCircleMarkers","args":[[-34.94983157727109,-38.70475630702338,-32.91629723864629,-31.63823807734137,-31.76294822831131,-27.46373244873876,-27.45634083530054,-45.84503608516329,-32.86247067715458,-27.46918004799461,-31.3246342911516,-31.37992163203392,-26.09262818618212,-38.95143032201835,-27.77774039034913,-24.15756829693703,-51.63380538209513,-28.4019981097551,-24.79227669867552,-29.59511953563488,-33.27757073346354,-31.5264583779038,-26.80235268771995,-36.60973588441878,-54.29931374358322,-34.61450141350594,-34.58313880520514,-38.00425315570097,-33.10002766722715,-33.31949892887774,-43.24303483097826,-40.80425188430407],[-57.97301561179525,-62.26569125171952,-60.77094469254985,-60.63886791069051,-60.48101335129581,-55.90496297118494,-58.98669352080694,-67.51521083497538,-68.86390639294065,-58.76855518131105,-64.23297420082234,-58.03414704024036,-58.11173143351487,-68.18560143522865,-64.26390635019806,-65.40493923390571,-69.25608249158297,-65.78947389486224,-65.41831560921236,-66.68401097803616,-66.31496244824928,-68.52609501091392,-65.24038688473635,-64.29912263291693,-68.01766639334508,-58.44639444094842,-58.58878339007717,-57.59645059094734,-64.3202598811874,-60.27633743620682,-65.23918297985782,-62.98835973400427],10,null,null,{"interactive":true,"className":"","stroke":false,"color":"#03F","weight":5,"opacity":0.5,"fill":true,"fillColor":["#482576","#57C766","#2EB37C","#277F8E","#20A386","#3D4E8A","#238A8D","#1F968B","#33B679","#31688E","#7FD34E","#B2DD2D","#39558C","#2CB17E","#440154","#2C718E","#31B57B","#38598C","#218F8D","#26AD81","#24AA83","#2C738E","#2C718E","#228D8D","#26818E","#FDE725","#35B779","#77D153","#1F988B","#39BA76","#31688E","#424186"],"fillOpacity":0.75},null,null,null,null,["<p>Gran La Plata<p><\/p>tasa_actividad: 0.26<\/p>","<p>Bahia Blanca - Cerri<p><\/p>tasa_actividad: 0.48<\/p>","<p>Gran Rosario<p><\/p>tasa_actividad: 0.45<\/p>","<p>Gran Santa Fe<p><\/p>tasa_actividad: 0.37<\/p>","<p>Gran Paraná<p><\/p>tasa_actividad: 0.42<\/p>","<p>Posadas<p><\/p>tasa_actividad: 0.3<\/p>","<p>Gran Resistencia<p><\/p>tasa_actividad: 0.39<\/p>","<p>Comodoro Rivadavia - Rada Tilly<p><\/p>tasa_actividad: 0.4<\/p>","<p>Gran Mendoza<p><\/p>tasa_actividad: 0.45<\/p>","<p>Corrientes<p><\/p>tasa_actividad: 0.34<\/p>","<p>Gran Córdoba<p><\/p>tasa_actividad: 0.5<\/p>","<p>Concordia<p><\/p>tasa_actividad: 0.53<\/p>","<p>Formosa<p><\/p>tasa_actividad: 0.31<\/p>","<p>Neuquén - Plottier<p><\/p>tasa_actividad: 0.44<\/p>","<p>Santiago del Estero - La Banda<p><\/p>tasa_actividad: 0.22<\/p>","<p>Jujuy - Palpalá<p><\/p>tasa_actividad: 0.35<\/p>","<p>Rio Gallegos<p><\/p>tasa_actividad: 0.45<\/p>","<p>Gran Catamarca<p><\/p>tasa_actividad: 0.32<\/p>","<p>Salta<p><\/p>tasa_actividad: 0.39<\/p>","<p>La Rioja<p><\/p>tasa_actividad: 0.44<\/p>","<p>San Luis - El Chorrillo<p><\/p>tasa_actividad: 0.43<\/p>","<p>Gran San Juan<p><\/p>tasa_actividad: 0.35<\/p>","<p>Gran Tucumán - Tafi Viejo<p><\/p>tasa_actividad: 0.35<\/p>","<p>Santa Rosa - Toay<p><\/p>tasa_actividad: 0.39<\/p>","<p>Ushuaia - Rio Grande<p><\/p>tasa_actividad: 0.37<\/p>","<p>CABA<p><\/p>tasa_actividad: 0.57<\/p>","<p>Partidos del GBA<p><\/p>tasa_actividad: 0.45<\/p>","<p>Mar del Plata - Batán<p><\/p>tasa_actividad: 0.5<\/p>","<p>Rio Cuarto<p><\/p>tasa_actividad: 0.41<\/p>","<p>San Nicolas - Villa Constitiución<p><\/p>tasa_actividad: 0.46<\/p>","<p>Rawson - Trelew<p><\/p>tasa_actividad: 0.34<\/p>","<p>Viedma - Carmen de Patagones<p><\/p>tasa_actividad: 0.29<\/p>"],{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]},{"method":"addLegend","args":[{"colors":["#440154 , #481D6F 7.697208218503%, #3E4A89 22.2468091193318%, #2D718E 36.7964100201607%, #20938C 51.3460109209895%, #32B67A 65.8956118218183%, #7CD250 80.4452127226472%, #DDE318 94.994813623476%, #FDE725 "],"labels":["0.25","0.30","0.35","0.40","0.45","0.50","0.55"],"na_color":null,"na_label":"NA","opacity":1,"position":"bottomright","type":"numeric","title":"tasa_actividad","extra":{"p_1":0.07697208218502996,"p_n":0.9499481362347599},"layerId":null,"className":"info legend","group":null}]}],"limits":{"lat":[-54.29931374358322,-24.15756829693703],"lng":[-69.25608249158297,-55.90496297118494]}},"evals":[],"jsHooks":[]}
```
