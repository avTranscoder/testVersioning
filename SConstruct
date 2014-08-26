import glob, re
import os
import sys

env = Environment()

# C++ environment
env.Append(
    CPPPATH = [
        "#src",
    ],
    CXXFLAGS = [
        '-Wall',
        '-fPIC',
    ],
    LIBPATH = [
        "#src",
    ],
)

avTestVersioningVersion = "0.0.1"

staticTestVersioning = env.StaticLibrary(
    'sTestVersioning',
    Glob( 'src/*.cpp' )
)

sharedTestVersioning = env.SharedLibrary(
    'testVersioning',
    Glob( 'AvTranscoder/*.cpp' ),
    SHLIBVERSION = avTestVersioningVersion,
)

Export( { 'sTestVersioning' : staticTestVersioning } )
Export( { 'testVersioning'  : sharedTestVersioning } )

# env.Alias( "install", env.Install( "lib", staticTestVersioning ) )
# env.Alias( "install", env.InstallVersionedLib( "lib" , sharedTestVersioning ) )
