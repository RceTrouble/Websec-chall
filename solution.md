1. Looking at the source code, we can see an interesting code : `<script src="https://get.mavo.io/mavo.js"></script>`
2. Mavo is a JS framework, used for writing websites without a single JS code.. great!
3. If we search for a simple phrase "mavo xss", an article by portswigger is discovered : <a href="https://portswigger.net/research/abusing-javascript-frameworks-to-bypass-xss-mitigations">here</a>
4. In the article, we can see that we can use a thing called "MavoScript", which is extended JS.
5. So we now have a nice payload to use... but where?
6. FUZZING IS DA WAY - Yes, you need to fuzz a parameter, kinda tricky, but trust me, fuzzing for hidden parameters can be a goldmine. :)
7. You can use any tool for fuzzin params, This tool is good : <a href="https://github.com/0xsapra/fuzzparam">fuzzparam</a> (credits to 0xsapra)
8. `q` parameter is reflected. 
9. `site.com/?q=[self.alert(1)]`
