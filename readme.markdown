Why does `git status` show that all of my files are modified?
--
StoryTeller is built by Windows users, so all of the text files have CRLF line endings. These line endings are stored as-is in git (which means we all have autocrlf turned off).
If you have autocrlf enabled, when you retrieve files from git, it will modify all of your files. Your best bet is to turn off autocrlf, and re-create your clone of StoryTeller.

1. Delete your local clone of the StoryTeller repository
1. Type: `git config --global core.autocrlf false`
1. Type: `git config --system core.autocrlf false`
1. Clone the StoryTeller repository again

Where is CommonAssemblyInfo.cs?
--

CommonAssemblyInfo.cs is generated by the build. The build script requires Ruby with rake installed.

1. open a command prompt to the root folder and type `rake` to execute rakefile.rb

If you do not have ruby:

1. You need to manually create a source\CommonAssemblyInfo.cs file 

  * type: `echo // > source\CommonAssemblyInfo.cs`
1. open source\StoryTeller.sln with Visual Studio and Build the solution