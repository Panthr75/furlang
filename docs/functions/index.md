<h2>Example</h2>

<pre type="code-block"><code customStyle="true"><comment># function-example.fur</comment>
<keyword>protogen</keyword> <function-name>zeroArgFunction</function-name> <keyword>{</keyword><keyword>}</keyword>:
    <function-name>awoo</function-name> <keyword>{</keyword><string>"Zero arg function was called"</string><keyword>}</keyword>

<function-name>zeroArgFunction</function-name> <keyword>{}</keyword> <comment># Logs "Zero arg function was called" into the console</comment>
<function-name>zeroArgFunction</function-name> <keyword>{<string>"some string"</string>}</keyword> <comment># Throws an unexpected fur error</comment>
<keyword>frisky</keyword> <function-name>zeroArgFunction</function-name> <keyword>{<string>"some string"</string>}</keyword> <comment># Logs "Zero arg function was called" into the console</comment>

<comment><jsdoc-format-2>NOTE</jsdoc-format-2>: defining functions with the <keyword>sfw</keyword> keyword at the beginning disallows calling a function with the <keyword>frisky</keyword>. If a <keyword>sfw</keyword> function is called with the <keyword>frisky</keyword>, a NSFW Error is thrown.</comment>


<keyword>sfw</keyword> <keyword>protogen</keyword> <function-name>oneArgFunction</function-name> <keyword>{</keyword><variable>arg1</variable><keyword>}</keyword>:
    <function-name>awoo</function-name> <keyword>{</keyword><string>"One arg function was called: "</string> + <variable>arg1</variable><keyword>}</keyword>

<function-name>oneArgFunction</function-name> <keyword>{}</keyword> <comment># Throws an expected fur error</comment>
<function-name>oneArgFunction</function-name> <keyword>{<string>"some string"</string>}</keyword> <comment>Logs "One arg function was called: some string" into the console</comment>
<keyword>frisky</keyword> <function-name>oneArgFunction</function-name> <keyword>{<string>"some string"</string>}</keyword> <comment># Throws a NSFW Error</comment>

</code></pre>
