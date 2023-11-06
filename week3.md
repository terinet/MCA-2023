[week2](week2.md)
[week4](week4.md)

https://terinet.github.io/MCA-2023/verovio.html

differences between MusicXML and MEI that I noticed:

1)MusicXML uses separate sections for metadata like the title, composer, and instrumentation. MEI consolidates this data in its <meiHead>, with more detailed sections and references for authorities, making it appear more complex due to its multi-level information display

2)MusicXML and MEI both use the <clef> tag to represent the clef element, specifying details like type, line, and other attributes. However, MusicXML distinguishes the clef type and placement line using the attributes <sign> and <line>

3)In MusicXML the key is represented through a <key> element, which is placed within the 'attributes' parent element. In contrast, MEI records this information within an element known as <keySig>, which offers a more extensive array of child elements and can be housed by various attributes. 
