# agslua

[![Build Status](https://dev.azure.com/ericoporto/agslua/_apis/build/status/ericoporto.agslua?branchName=master)](https://dev.azure.com/ericoporto/agslua/_build/latest?definitionId=10&branchName=master)

## Complications

- The editor plugin is ILMerged with ZLib.NET and Scintilla.NET, as a post-compile action
	- ILMerge: http://www.microsoft.com/download/en/details.aspx?displaylang=en&id=17630
	- ZLib.NET: http://www.componentace.com/zlib_.NET.htm
- Several of the runtime plugin files are generated, rather than handwritten, by a Lua script that uses information about the object types, function signatures etc. to create a whole lot of repetitive boilerplate code
- The runtime plugin needs a DLL lib for Lua 5.1, a static lib for ZLib, the Windows SDK for <WINDOWS.H>
- The runtime plugin uses a little Lua helper library I made called llh (included)
