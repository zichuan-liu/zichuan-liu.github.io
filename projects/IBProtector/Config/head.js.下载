var scripts = document.getElementsByTagName('script');
var myScript = scripts[scripts.length - 1];

var queryString = myScript.src.replace(/^[^\?]+\??/, '');

var params = parseQuery(queryString);

function parseQuery(query) {
    var Params = {};
    if (!query) return Params; // return empty object
    var Pairs = query.split(/[;&]/);
    for (var i = 0; i < Pairs.length; i++) {
        var KeyVal = Pairs[i].split('=');
        if (!KeyVal || KeyVal.length != 2) continue;
        var key = unescape(KeyVal[0]);
        var val = unescape(KeyVal[1]);
        val = val.replace(/\+/g, ' ');
        Params[key] = val;
    }
    return Params;
}

document.write('\
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>\
    <meta name=viewport content="width=device-width, initial-scale=1">\
    <link rel="shortcut icon" href="'+params["prefix"]+'images/favicon.ico">\
');

function append_image(id, width, i) {
    var elem = document.createElement('img');
    elem.src = 'images/'.concat(i).concat('.png');
    elem.width = width;
    elem.style.padding = "20px 20px 20px 20px";
    console.log(elem);

    var div = document.getElementById(id)
    div.appendChild(elem)
    console.log(div);
}

function append_all() {
    var id = 'attention_maps'
    var width = 240;

    for (let i = 0; i < 1000; i++) {
        append_image(id, width, i);
    }
}