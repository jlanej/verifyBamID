cmake_minimum_required(VERSION 3.13)
project(src)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)
include_directories(base)
include_directories(genmat)
include_directories(../../libStatGen/general/)
include_directories(../../libStatGen/samtools/)
include_directories(../../libStatGen/bam/)

add_executable(src
        base/basictypes.h
        base/build_config.h
        base/port.h
        base/string_piece.h
        base/string_tokenizer.h
        genmat/GenMatrix.h
        BamPileBases.cpp
        BamPileBases.h
        Logger.h
        Main.cpp
        MathGenMin.cpp
        MathGenMin.h
        MathGold.cpp
        MathGold.h
        VcfFile.cpp
        VcfFile.h
        VerifyBamID.cpp
        VerifyBamID.h
        VerifyBamIDArgs.h)
