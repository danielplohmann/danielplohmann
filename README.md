Hi! I'm Daniel and I do [research](https://net.cs.uni-bonn.de/wg/cs/staff/daniel-plohmann/) around (malware) reverse engineering and analysis automation.

The root and motivation for most of my projects is [Malpedia](https://malpedia.caad.fkie.fraunhofer.de/), a a resource for rapid identification and actionable context when investigating malware.
It was launched in December 2017 by [Steffen Enders](https://github.com/steffenenders) and me and is maintained by us ever since.

[SMDA](https://github.com/danielplohmann/smda) is a minimalistic recursive disassembler, which internally uses [capstone](https://github.com/capstone-engine/capstone). 
It was created to study and improve heuristics for function entry point detection, especially in memory-mapped buffers and shellcode.

[MCRIT](https://github.com/danielplohmann/mcrit) is the MinHash-based Code Relationship & Investigation Toolkit, a binary code similarity analysis framework.
It uses [SMDA](https://github.com/danielplohmann/smda) as its built-in disassembler, and [picblocks](https://github.com/danielplohmann/picblocks) for the hashing of basic blocks. 
For easy deployment, it comes as [docker-mcrit](https://github.com/danielplohmann/docker-mcrit), including its web UI [mcritweb](https://github.com/fkie-cad/mcritweb).

To filter out library code during analysis, we created [mcrit-data](https://github.com/danielplohmann/mcrit-data), a collection of reference library code for various compilers (MSVC, MinGW, Go, Nim, ...) and commonly found 3rd party libraries.
For this, the support tool [lib2smda](https://github.com/danielplohmann/lib2smda) was created, which can be used to convert LIB/OBJ files into SMDA reports, which can then be imported into MCRIT.
[Empty MSVC](https://github.com/danielplohmann/empty_msvc) was a pre-cursor to this, which is a collection of "empty main()" Visual Studio projects, compiled with various options - which can also serve well as ground truth for commonly found compiler/library code.

During my [research](https://cyberjournal.cecyf.fr/index.php/cybin/article/view/20/15) on dynamic Windows API imports in malware, I wrote [ApiScout](https://github.com/danielplohmann/apiscout). 
It's a method/tool to reliably recover such dynamic imports and make them usable in other tools.
We also showed that the entirety of Windows API imports used by a malware family can be used effectively for its identification.

In 2012, I created [IDAscope](https://github.com/danielplohmann/idascope), an IDA Pro plugin that provides various convenience functionality during reversing. 
It was one of the first plugins which extensive rich use of PySide/PyQt in IDA and served as a template for many others.

Over the years, I occassionally wrote some [blog posts](https://danielplohmann.github.io/), which cover many of the above projects or aspects of them in detail. 

If you want to support my work, I would be happy if you'd [buy me a coffee](https://www.buymeacoffee.com/pnxpnx). 
