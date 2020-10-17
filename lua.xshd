<?xml version="1.0"?>

<SyntaxDefinition name="Lua" extensions=".lua" xmlns="http://icsharpcode.net/sharpdevelop/syntaxdefinition/2008">
  <Color name="Comment" foreground="#ff999999" exampleText="-- comment" />
  <Color name="String" foreground="#F2DC63" />
  <Color name="Punctuation" foreground="#DA577C" />
  <Color name="MethodCall" foreground="#76CE89" fontWeight="bold" />
  <Color name="NumberLiteral" foreground="#948AE3" />
  <Color name="NilKeyword" fontWeight="bold" />
  <Color name="Keywords" fontWeight="bold" foreground="#DA577C" />
  <Color name="GotoKeywords" foreground="#F45F89" />
  <Color name="Visibility" fontWeight="bold" foreground="#FC618D" />
  <Color name="TrueFalse" fontWeight="bold" foreground="#9086DC" />

  <RuleSet name="CommentMarkerSet">
    <Keywords fontWeight="bold" foreground="#fff2777a">
      <Word>TODO</Word>
      <Word>FIXME</Word>
    </Keywords>
    <Keywords fontWeight="bold" foreground="#fff2777a">
      <Word>HACK</Word>
      <Word>UNDONE</Word>
    </Keywords>
  </RuleSet>

  <RuleSet>
    <Span color="Comment" ruleSet="CommentMarkerSet" multiline="true">
      <Begin>--\[[=]*\[</Begin>
      <End>\][=]*]</End>
    </Span>

    <Span color="Comment" ruleSet="CommentMarkerSet">
      <Begin>--</Begin>
    </Span>

    <Span color="String">
      <Begin>"</Begin>
      <End>"</End>
      <RuleSet>
        <Span begin="\\" end="." />
      </RuleSet>
    </Span>

    <Span color="String">
      <Begin>'</Begin>
      <End>'</End>
      <RuleSet>
        <Span begin="\\" end="." />
      </RuleSet>
    </Span>

    <Span color="String" multiline="true">
      <Begin color="String">\[=*\[</Begin>
      <End color="String">\]=*\]</End>
    </Span>

    <Keywords color="TrueFalse">
      <Word>true</Word>
      <Word>false</Word>
    </Keywords>

    <Keywords color="Keywords">
      <Word>and</Word>
      <Word>break</Word>
      <Word>do</Word>
      <Word>else</Word>
      <Word>elseif</Word>
      <Word>end</Word>
      <Word>false</Word>
      <Word>for</Word>
      <Word>function</Word>
      <Word>if</Word>
      <Word>in</Word>
      <Word>local</Word>
      <Word>not</Word>
      <Word>or</Word>
      <Word>repeat</Word>
      <Word>return</Word>
      <Word>then</Word>
      <Word>true</Word>
      <Word>until</Word>
      <Word>while</Word>
    </Keywords>

    <Keywords color="GotoKeywords">
      <Word>break</Word>
      <Word>return</Word>
    </Keywords>

    <Keywords color="Visibility">
      <Word>local</Word>
      <Word>self</Word>
    </Keywords>

    <Keywords color="NilKeyword">
      <Word>nil</Word>
    </Keywords>

    <Rule color="MethodCall">
      \b
      [\d\w_]+  # an identifier
      (?=\s*\() # followed by (
    </Rule>
    <Rule color="MethodCall">
      \b
      [\d\w_]+  # an identifier
      (?=\s*\") # followed by "
    </Rule>
    <Rule color="MethodCall">
      \b
      [\d\w_]+  # an identifier
      (?=\s*\') # followed by '
    </Rule>
    <Rule color="MethodCall">
      \b
      [\d\w_]+  # an identifier
      (?=\s*\{) # followed by {
    </Rule>

    <Rule color="NumberLiteral">
      \b
      0[xX][0-9a-fA-F]+  # hex number
      |
      ( \b\d+(\.[0-9]+)?   #number with optional floating point
      | \.[0-9]+           #or just starting with floating point
      )
      ([eE][+-]?[0-9]+)?   # optional exponent
    </Rule>

    <Rule color="Punctuation">
      [?,.;()\[\]{}+\-/%*&lt;&gt;^+~!|&amp;#=]+
    </Rule>
  </RuleSet>
</SyntaxDefinition>
