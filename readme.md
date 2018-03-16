# yoloSensor

This takes the darknet yolo 2 sensor, and sends it over osc to a [living-room-server][]

  /assert #yoloSensor found a wineglass at 0.73 0.23 0.01 0.05 1521216271

You can see what it sees with

  /select #yoloSensor found a $label at $x $y $width $height $timestamp

# install

You will need **yolo.weights** in the root directory

  curl -Os http://pjreddie.com/media/files/yolo.weights

You will need liblo to compile

  which brew && brew install liblo || sudo apt install liblo-dev

Compile with

  make

# running

  ./yoloSensor cfg/yolo9000.cfg cfg/coco.data -thresh 0.15

# credits

It is based off of [Darknet][]

[living-room-server]: https://github.com/jedahan/living-room-server
[Darknet]: http://pjreddie.com/darknet
