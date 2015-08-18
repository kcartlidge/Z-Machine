# Z-Machine
A Version 3 C# implementation of the Zork Interpreter Program (ZIP) by Infocom

The Z-machine was created on a coffee table in Pittsburgh in 1979. It is an imaginary computer whose programs are adventure games, and is well-adapted to its task, implementing complex games remarkably compactly. They were still perhaps 100K long, too large for the memory of the home computers of their day, and the Z-machine seems to have made the first usage of virtual memory on a microcomputer. Further ahead of its time was the ability to efficiently save and restore the entire execution state. The design's cardinal principle is that any game is 100% portable to different computers: that is, any legal program exactly determines its behaviour. This portability is largely made possible by a willingness to constrain maximum as well as minimum levels of performance (for instance, dynamic memory allocation is impossible).

The Z-Machine Standards Document was first released in 1997 based on an internal document called the "Z-Language Interpreter Program", a virtualized machine that would allow any user to program their machine to run games written in Z-Language, an object based language that relied on locations in memory for access once a file was read into memory. By having a virtual Z-Machine read through memory as if it was reading from its own ROM, it would execute calls and jumps in a predictable way. The first game to be executed successfully in the Z-Language was Zork I: The Great Underground, which I have in the main folder, stored as a .DAT file. The entire game is written in a single byte-array which contains the logic flow, the save state controllers, and the text, encoded in an ASCII-like form called "ZSCII", which was necessary to preserve the uniformity of character size in memory. The game file will be modified during execution, which allows it to be self-contained much like a game cartridge.

Files like Zork I are generally called "story files". Approximately 130 story files exist, and Infocom released a compiler in 1993 so that these programs could be generally executable without the use of a prorprietary Z-Machine Interpreter like the one I have created. The compiler allowed anyone to create their own story files, and since 1993 many many more games have been written in the Z-Language. Z-Machines went through several iterations as technology improved, adding colour, sound, images, and the ability to use game controllers (such as mice) instead of standard text input. Still, there are two primary implementations of the Z-Machine, version 3, which has full support for text and save states, and version 6, which also supports visuals, sound, and use of a mouse. The first byte of any story file will give the Version number. Though my version 3 interpreter does not support these additional features, it allows for expansion, and I encourage anyone who wants to know more about how machine processes or data storage and retrieval works to give it a shot.

I included the primary documentation files I used as reference, and more information is available here: http://inform-fiction.org/zmachine/standards/index.html
