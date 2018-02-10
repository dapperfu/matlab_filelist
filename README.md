```
matlab_filelist
===============
%FILE_LIST Create list of files
%   [FILES,TOTAL_FILES,FILES_STRUCT] = FILE_LIST(TOPLEVEL,FILE_EXTENSION,DEPTH,FILENAME_SEARCH,FILENAME_EXACT) will
%   recurse through subdirectories of TOPLEVEL to a depth of DEPTH looking
%   for files that have the same extension as FILE_EXTENSION and matching
%   FILENAME_SEARCH. FILENAME_EXACT will match the filename exactly.
%
%   FILE_EXTENSION searches for the given the extension. Can be specified
%   with or without wildcards. '*.m' '.m' & 'm' are all equivalent. However
%   for wildcard searches '*' and '.*' are different. '*' will search for
%   all files (including those without extensions). '.*' will return all
%   extensions 
%
%   FILE_LIST(TOPLEVEL,FILE_EXTENSION) will search all subdirectories (to a
%   depth of infinity)
%
%   FILE_LIST(TOPLEVEL) will search for all files in a folder and sub
%   folders
%
%   TOPLEVEL and FILE_EXTENSION can also be cell arrays of multiple top
%   level directories or file extensions.
%
%   FILENAME_EXACT defaults to false. (For backwards compatability).
%
%   FILE_LIST is a cell array of all the file found
%   TOTAL_FILES is the total number of files found
%
%   The absolute path is always returned using GetFullPath.
%
%   Example:
%   [files,total]=file_list(pwd)
%   [files,total]=file_list(pwd,{'m','*mat','*.txt'})
%   [files,total]=file_list({'C:'},'.txt')
%   [files,total]=file_list({'C:'},{'m','mat'})
%   [files,total]=file_list({'C:'},'',inf,'NTUSER')
%
%   [files,total]=file_list(pwd,'*.mat',1);
%   for i=1:total
%       data=load(files{i});
%       % Do stuff with file
%   end
```
