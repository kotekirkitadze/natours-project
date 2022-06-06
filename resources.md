1.  პროცენტი სხვადასხვანაირად მუშაობს
    ფონტზე და length ზე:
    ფონტზე: ყოველთვის იღებს რეფერენსად მშობლის ფონტ საიზს.
    ხოლო length ის დროს, ყოველდთვის იღებს ფერენტის
    width - ს რეფერენსად. \*/

2.  ფონტის პროცენტულობა მშბლიდან მოდის, და სიგრძის:
    პადინგების და მარჯინების მშბლიდან \*/

3.  რემი და ემი ფონტ ბეისდ იუნითებია:
    ემი მშობლიდან ან თავისი ელემენტის ფონტ საიზს იღებს
    რეფერენსად. რემი კიდევ რუთის ფონთ საიზს იღებს
    რეფერენსად.

4.  მაგრამ ემის გამოყენებისას სიგრძისას, ქარენთ ელემენტის
    ფონტს საიზს აიღებს რეფერენსად.
    for font in em reference is parent emelent, but
    for length, reference is current element's font-size. _/
    /_ მაგრამ რემი ერთნაირად მუშაობს ფონტზეც და ლენგზეც,
    რადგან რეფერენსს რუთიდან იღებს \*/

/_
vh და vh are based on browser's viewport
_/

5. inheritance
   properties related to texts are inherited, like
   font-size, font-family, color...

margin, padding and ... - are note inhereted

we can force inheritance by keyword inherit.
Also, we can use initial keyword to
reset a property to its initial value.

6.  in regular css in rgba color like hexadecimal do not work like that:
    $color-black: #000;
    rgba($color-black, 0.2);
    but in sass it works

7.  no underscore in scss for partials imports and also no .scss in imports
8.  to make image flexible we use percentage
    (and max-width in a certain situations) instead of
    pixels, because images behaves differently //than text.

9.  max-width is good to fill the place with 100% available space, if viewport is smaller than specified width

10. to use variables in calc function, we need this kind of
    syntax: calc((100% - (2 \* #{$gutter-horizontal}));

11. we can select element by attribuet in css:
    [alt="Logo"] {}
    aslos, we can do not only by equal but also like take
    all elements that classes starts with: col-
    like that: [class^="col-"] {}.
    This one: [class*="col-"]{} takse all emenets which contains col-.
    This one: [class$="col-"]{} takes which ends with col-.
