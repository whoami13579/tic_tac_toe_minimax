cmake_minimum_required(VERSION 3.26)
project(tic_tac_toe_minimax)
set(CMAKE_CXX_STANDARD 17)
# include_directories(${SFML_INCLUDE_DIRS})
include_directories(./sfml/2.6.1/include/)
add_executable(tic_tac_toe_minimax main.cpp
        Texture.cpp
        Texture.h
        Piece.cpp
        Piece.h
        Board.cpp
        Board.h
        Game.cpp
        Game.h
        MiniMax.cpp
        MiniMax.h
)
find_package(SFML 2.6 COMPONENTS system window graphics audio network REQUIRED)
target_link_libraries(tic_tac_toe_minimax sfml-system sfml-window sfml-graphics sfml-audio sfml-network)
