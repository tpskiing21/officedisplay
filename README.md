<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Dashboard Controller</title>
  <style>html,body{height:100%;margin:0;background:#000;color:#fff;display:flex;align-items:center;justify-content:center;font:16px system-ui}</style>
</head>
<body>
  <div>Loading next view…</div>
  <script>
    // Configure your two targets:
    const A = "https://click-bond.us4.alta.avigilon.com/videoview/82907d0a-9e52-4591-a79a-50c7aa64f4217?site=cbaf39c8-6671-4555-bde0-fa10c49f4217";
    const B = "https://www.flightaware.com/live/flex_bigmap.rvt?type=me&time=1751476500&key=2fbfa3039cc7560ac6f63f8b0df1a18d9403cd88";

    // Toggle which one to show next
    const nextKey = "cb_dashboard_next";
    let next = localStorage.getItem(nextKey) || "A";
    const url = (next === "A") ? A : B;
    localStorage.setItem(nextKey, next === "A" ? "B" : "A");

    // Immediately go to the chosen URL
    location.replace(url);
  </script>
</body>
</html>
