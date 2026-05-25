FROM ubuntu:latest

RUN apt update && apt upgrade -y

RUN apt install -y git cmake libsdl2-dev

RUN apt update && apt upgrade -y

RUN git clone https://github.com/Marchosias140/ioq3-experiments.git

WORKDIR /ioq3-experiments

RUN cmake -S . -B build -DCMAKE_BUILD_TYPE=Release

RUN cmake --build build

WORKDIR /ioq3-experiments/build

# Cmake flags

#  BUILD_SERVER            - build the 'ioq3ded' server binary
#  BUILD_CLIENT            - build the 'ioquake3' client binary
#  BUILD_RENDERER_OPENGL1  - build the opengl1 client / renderer library
#  BUILD_RENDERER_OPENGL2  - build the opengl2 client / renderer library
#  BUILD_GAME_LIBRARIES    - build the game shared libraries
#  BUILD_GAME_QVMS         - build the game qvms
#  BUILD_STANDALONE        - build binaries suited for stand-alone games

#  USE_RENDERER_DLOPEN     - build and use the renderer in a library
#  USE_OPENAL              - use OpenAL where available
#  USE_OPENAL_DLOPEN       - link with OpenAL at runtime
#  USE_HTTP                - enable http download support
#  USE_CODEC_VORBIS        - enable Ogg Vorbis support
#  USE_CODEC_OPUS          - enable Ogg Opus support
#  USE_MUMBLE              - enable Mumble support
#  USE_VOIP                - enable built-in VoIP support
#  USE_FREETYPE            - enable FreeType support for rendering fonts

#  USE_INTERNAL_LIBS       - build internal libraries instead of dynamically
#                            linking against system libraries; this just sets
#                            the default for USE_INTERNAL_ZLIB etc.
#  USE_INTERNAL_SDL        - link against internal SDL (if available)
#  USE_INTERNAL_ZLIB       - build and link against internal zlib
#  USE_INTERNAL_JPEG       - build and link against internal JPEG library
#  USE_INTERNAL_OGG        - build and link against internal ogg library
#  USE_INTERNAL_VORBIS     - build and link against internal Vorbis library
#  USE_INTERNAL_OPUS       - build and link against internal opus/opusfile libraries

#  EMSCRIPTEN_PRELOAD_FILE - set to 1 to package 'baseq3' (BASEGAME) directory
#                            containing pk3s and loose files as a single
#                            .data file that is loaded instead of listing
#                            individual files in client-config.json

#  CMAKE_BUILD_TYPE        - on single config CMake, set to Debug or Release

