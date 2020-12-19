# FFMPEG

Provides a recent and extensive ffmpeg build, for consistent deployment across platforms.

    docker run --rm -it dgrnwd/ffmpeg


From a movie via url - note that https is working fine:

docker run --rm -it \
    -w /f \
    -v "$(pwd)":/f \
     dgrnwd/ffmpeg \
    -i https://www.learningcontainer.com/wp-content/uploads/2020/05/sample-mp4-file.mp4 \
    out.mp4


using an alias in zshrc:

dffmpeg(){
    docker run --rm -it -w /f -v "$(PWD)":/f dgrnwd/ffmpeg "$@"
    }
