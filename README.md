# go-staticmaps
Render static map images with go using OpenStreetMap tiles.


## Installation

    go get -u github.com/flopp/go-staticmaps/...

## Usage
    
    Usage:
      create-static-map [OPTIONS]
    
    Creates a static map
    
    Application Options:
          --width=PIXELS       Width of the generated static map image (default: 512)
          --height=PIXELS      Height of the generated static map image (default: 512)
      -o, --output=FILENAME    Output file name (default: map.png)
      -t, --type=MAPTYPE       Select the map type; list possible map types with '--type list'
      -c, --center=LATLNG      Center coordinates (lat,lng) of the static map
      -z, --zoom=ZOOMLEVEL     Zoom factor
      -m, --marker=MARKER      Add a marker to the static map
      -p, --path=PATH          Add a path to the static map
    
    Help Options:
      -h, --help               Show this help message

### Create a map of the Berlin Marathon

    go run cmd/create-static-map.go --width 800 --height 600 --marker "color:green|52.5153,13.3564" --marker "color:red|52.5160,13.3711" --output "berlin.png" --path "color:blue|weight:2|52.5153,13.3564|52.5146,13.3519|52.5143,13.3511|52.5139,13.3502|52.5139,13.3496|52.5143,13.3484|52.5129,13.3280|52.5128,13.3234|52.5128,13.3230|52.5138,13.3226|52.5146,13.3225|52.5170,13.3244|52.5220,13.3286|52.5223,13.3285|52.5238,13.3297|52.5246,13.3346|52.5223,13.3675|52.5221,13.3685|52.5209,13.3739|52.5217,13.3754|52.5221,13.3764|52.5272,13.3872|52.5294,13.3976|52.5283,13.4114|52.5274,13.4145|52.5249,13.4201|52.5226,13.4176|52.5222,13.4169|52.5206,13.4216|52.5189,13.4277|52.5189,13.4282|52.5188,13.4288|52.5182,13.4289|52.5180,13.4282|52.5142,13.4252|52.5131,13.4238|52.5098,13.4212|52.5110,13.4165|52.5037,13.4104|52.5034,13.4105|52.4992,13.4179|52.4989,13.4178|52.4988,13.4183|52.4955,13.4204|52.4880,13.4251|52.4865,13.4241|52.4874,13.4209|52.4895,13.4065|52.4938,13.3836|52.4935,13.3672|52.4942,13.3626|52.4914,13.3622|52.4910,13.3607|52.4905,13.3602|52.4890,13.3451|52.4857,13.3452|52.4831,13.3451|52.4815,13.3449|52.4787,13.3440|52.4724,13.3361|52.4710,13.3295|52.4715,13.3291|52.4712,13.3283|52.4716,13.3194|52.4706,13.3175|52.4674,13.3088|52.4681,13.3077|52.4677,13.3063|52.4691,13.2979|52.4707,13.2898|52.4707,13.2893|52.4768,13.2811|52.4801,13.2863|52.4802,13.2861|52.4885,13.3021|52.4884,13.3055|52.4905,13.3142|52.4927,13.3111|52.4971,13.3116|52.4995,13.3128|52.5007,13.3132|52.5026,13.3253|52.5045,13.3347|52.5022,13.3420|52.5020,13.3432|52.5001,13.3515|52.4999,13.3539|52.4980,13.3621|52.4998,13.3628|52.5040,13.3664|52.5053,13.3678|52.5084,13.3695|52.5096,13.3763|52.5096,13.3781|52.5107,13.3928|52.5110,13.3968|52.5123,13.3934|52.5159,13.3929|52.5170,13.3907|52.5160,13.3711"

![https://raw.githubusercontent.com/flopp/go-staticmaps/master/examples/berlin-marathon.png]

## License
Copyright 2016 Florian Pigorsch. All rights reserved.

Use of this source code is governed by a MIT-style license that can be found in the LICENSE file.
