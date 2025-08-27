
<!doctype html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Camera + FlightAware</title>
    <style>
      html,body{height:100%;margin:0}
      .wrap{display:flex;height:100vh;width:100vw}
      .left,.right{height:100%;border:0}
      .left{flex:6}   /* Avigilon wider */
      .right{flex:4}  /* FlightAware narrower */
      @media (max-aspect-ratio: 4/5){ /* if portrait-ish screen, stack */
        .wrap{flex-direction:column}
        .left,.right{width:100%}
        .left{height:60vh}
        .right{height:40vh}
      }
    </style>
  </head>
  <body>
    <!-- Avigilon -->
    <iframe class="left"
      src="https://click-bond.us4.alta.avigilon.com/videoview/82907d0a-9e52-4591-a79a-50c7aa64f193?site=cbaf39c8-6671-4555-bde0-fa10c49f4217"
      allow="autoplay; fullscreen"></iframe>

    <!-- FlightAware -->
    <iframe class="right"
      src="https://www.flightaware.com/live/flex_bigmap.rvt?type=me&time=1751476500&key=2fbfa3039cc7560ac6f63f8b0df1a18d9403cd88"
      allow="autoplay; fullscreen"></iframe>
  </body>
</html>
