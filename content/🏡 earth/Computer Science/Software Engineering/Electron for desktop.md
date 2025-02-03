#concept-pamphlet 

In Electron, each window displays a web page that can be loaded either from a  `________` or a  `________`.
[[SR/memory/N9ZXpWke.md|?]]
local HTML file, remote web address.


What is a preload script in Electron?
[[SR/memory/vH73kwJQ.md|?]]
It is a script that bridges Electron's different processes together. These processes include:
- Electron's main process which is a Node.js environment with full OS access. Includes Electron and Node.js built-in modules.
- Renderer processes to run web pages. They do not include Node.js by default for security reasons.


What is inter-process communication (IPC) in Electron?
[[SR/memory/VfNKH9kG.md|?]]
IPC consists of modules that help communicate between Electron's main and renderer processes. Messages are sent between the web page and the main process. 

