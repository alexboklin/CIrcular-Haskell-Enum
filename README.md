This is a realization of Haskell Enum that wraps around (i.e., does now stop as its maxBound and minBound). 

For example, given that False is minBound for Bool and True is maxBound for Bool, here's what we can do:

<pre><code>
GHCi> instance SafeEnum Bool
GHCi> spred False
True
GHCi> ssucc True
False
</code></pre>

Similarly, given that '\NUL' is minBound for Char and '\1114111' is maxBound for Char, we can do the following:

<pre><code>
GHCi> instance SafeEnum Char
GHCi> spred '\NUL'
'\1114111'
GHCi> ssucc '\1114111'
'\NUL'
</code></pre>
