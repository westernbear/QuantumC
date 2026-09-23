# Lexical Structures

The character set must be ASCII.
(principle of maximal munch)

## Alphabet

$$ \begin{align*}
    \texttt{<alphabet>}
    &\Coloneqq \texttt{"A"} \mid \texttt{"B"}
\end{align*} $$

## Whitespace

## Comments

## Identifiers

## Keywords

### Type Specifiers

$$ \begin{align*}
    \texttt{<type\_specifier>}
    &\Coloneqq \texttt{<classical\_type>} \mid \texttt{<quantum\_type>} \\
    
    \texttt{<classical\_type>}
    &\Coloneqq \texttt{"void"} \mid \texttt{"char"} \mid \texttt{"int"} \mid \texttt{"float"} \mid \texttt{"double"} \mid \\
    &\phantom{\Coloneqq} \texttt{"int8\_t"} \mid \texttt{"int16\_t"} \mid \texttt{"int32\_t"} \mid \texttt{"int64\_t"} \mid \\
    &\phantom{\Coloneqq} \texttt{"uint8\_t"} \mid \texttt{"uint16\_t"} \mid \texttt{"uint32\_t"} \mid \texttt{"uint64\_t"} \\

    \texttt{<quantum\_type>}
    &\Coloneqq \texttt{"qubit"} \mid \\
    &\phantom{\Coloneqq} \texttt{"int8\_q"} \mid \texttt{"int16\_q"} \mid \texttt{"int32\_q"} \mid \texttt{"int64\_q"}
\end{align*} $$

## Literals

## Operators
