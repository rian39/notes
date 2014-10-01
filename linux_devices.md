Alessandro Rubini & Jonathan Corbet, Linux Device Drivers, 2nd Edition
O'Reilly & Associates, 2nd Edition June 2001

In a Unix system, several concurrent processes attend to different tasks. Each process asks for system resources, be it computing power, memory, network connectivity, or some other resource. The kernel is the big chunk of executable code in charge of handling all such requests. (4)
Almost every system operation eventually maps to a physical device. (5)

So far, we've talked about the Linux kernel from the perspective of writing device drivers. Once you begin playing with the kernel, however, you may find that you want to "understand it all." In fact, you may find yourself passing whole days navigating through the source code and grepping your way through the source tree to uncover the relationships among the different parts of the kernel.  (http://www.xml.com/ldd/chapter/book/ch16.html)
