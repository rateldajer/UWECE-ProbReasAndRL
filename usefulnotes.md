## Useful notes

### Search and Replace
#### Structure
% s/\\subsection{\(.*\)}/## \1/g
% s/\\begin{enumerate}//g
% s/  \\item/-/g
#### References
'<,'>s/\$\(\$.\{-}\$\)\$/`\1`/g
% s/\\ccv/\\cite/g
% s/\\cite{\(.\{-}\)}/{\% include sidenote.html note="ref:\1" \%}/g    
