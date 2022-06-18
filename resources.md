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

12. შეგვიძლია ბექრაუნდი სადაც ტექსტია იქ მოვათავსოთ ვებკიტით:
    -webkit-background-clip: text; და შემდეგ ტექსტი გავხადოთ transparent რომ
    გამოჩნდეს ბექგრაუნდი.

13. დივშ თუ მოვაქცევთ ინლაინ ბლოკს, როგორც ტექსტი ისე ექცევა მას
    და text-align: center; - ით შეგვიძლია გავცენტროთ.
14. ჩვეულებრივ ბორდერსა და ელემენტს შორის ადგილს ვერ გამოვყოფთ,
    მაგრამ აუთლაინით და აუთლაინ ოფსეთით შეგვიძლია მაგის მიხწევა:
    outline: 1.5rem solid $color-primary; - ბორდერს გაუკეთებს
    outline-offset: 2rem; -- ბორდერსა და ელემენტს შორის ადგილს გააკეთებს
15. //composition:hover composition\_\_photo:not(:hover)რომელიც დაჰოვერებული
    არაა იმას აარჩევს.
16. <i> თეგი does not stands for icon, many are confused maybe.
    In prevous version of HTML, it was used to make text italic.
    It stands for italic, but now we no longer use it.

17. icon font is text და ჩვენ შეგვიძლია ბექრაუნდზე ისე დავქლიფოთ,
    რათა ფერები დავუყენოთ ხოლმე.

18. & > _ ასელექტებს დაირექთ შვილებს და & _ ასელექთებს ყველა შვილს.
19. card:hover card**side (&:hover &**side) როცა ქარდს ვაჰავერევთ ქარდ საიდს
    დაესეტოს სტილები.
20. მაგალითად რამე ქარდი რომ დავატრიალოთ, ვიყენებთ rotate ფროფერთის და სმუზ რომ იყოს,
    ფერსფექტივ ფროფერთი უნდა დავუყენოთ იმ ელემენტის მშობელს, რომელსაც ვატრიალებთ. ნორმალურად უფრო
    ნაისერ დატრიალება რომ ქონდეს და რაც უფრო დაბალია პერსპექტივის ველიუ, მით უდრო dramatic არის.
    150rem არისს ნორმალური და მოზილაშიც რომ იმუშავოს, მეორე ვებკითის ფროფერთიც უნდა დავუყენოთ:
    .card {
    perspective: 150rem;
    -moz-perspective: 150rem;
    &**side {
    transition: all 0.8s;
    }
    &:hover &**side {
    transform: rotateY(180deg);
    }
    }

21. When we use linear gradient, we should use background-image not background-color.
22. როცა სბოლუთს და რილეითივს ვიყენებთ, აბსოლუტზე როცა შვილს ვაყენებთ, ის ნორმალ ფლოუდან
    ვარდება და ამიტომ მშობლის ჰეითი ქოლაფსდ ხდება და ამიტომ ზომაც უნდა გავუწეროთ მშობელს
    ხელით, თუ რა ზომის გვინდა იყოს ის.
23. Great resource for pictures: https://unsplash.com/
24. ქლიპ პაზის გამოყენებისას ჯერ ვებკიტის ვერსიაც უნდა მივუთითოთ,
    რათა ყველა ბრაუზერში გაეშვას:
    -webkit-clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
    clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
25. ტექსტებზე გამოვიყენოთ რომ ბრეიქზე განსხვავებულ
    ბლოკებად ემუშვა სტილებს:
    -webkit-box-decoration-break: clone;
    box-decoration-break: clone;
26. ქლიფპეზის გამოყენების შემდეგ ოვერფლოუ აღარ ედება
    და ხელით უნდა გვაუწეროთ თუ გვიდნა რომ მომრგვალდეს:
    clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
    border-top-left-radius: 3px;
    border-top-right-radius: 3px;
    იმდენიმე ფიქსელი, რაც მშობელს უწერია ბორდერ რადიუსზე, ამ შემთხვევაში 3.
27. If we want to use -webkit-shape-outside, shape-outside properties element should
    have height, width and floated set. და ეს ფროფერთი გვეხმარება, რომ ელემენტსი ირგვლივ
    ვაფლოათოთ ელემენტები(ტექსტი თუნდაც).
28. როცა ელემენტი დაფლოატებულია(float:left) და ასე შემდეგ, ჯობია რომ მის მარჯინებში
    არ ჩავერიოთ და transform:translate() გამოვიყენოთ.
29. backface-visibility: hidden; - ანიმცაიების ბოლოში ფიქსავს,
    მაგალითად, ჰოვერზე ტრანსფორმის ბოლოში.
30. filter: blur(3px) brightness(80%);
    blur ბლარავს და ბრაიტნესზე 100 ზე ქვემოთ
    უფრო ადარქებს და 100 ზემოთ აბრაითნესებს.
31. coverr.co videos for websites
32. როცა ოფასითის ვაყენებთ ფერენთ ელემენტს და მის შვილებსაც ედებათ ოფასითი. მაგრამ ესე
    თუ არ გვინდა და მარტო მშობლის ბექრგაუნდი იყოს ოფასითი, მაშინ rgba() უნდა გამოვიყენოთ:
    background-color: rgba($color-white, 0.6);
33. object-fit: cover; მუშაობს როგორც background-size: cover; მაგრამ
    ობჯექთ ფით html ის ელემენტებზე მუშაობს და background-size კი ფოტოებზე.
34. background-size - ზე 100% იგივეა, რაც cover, მაგრამ უფრო x დაირექშენზე და
    მედია ქუერის დროს მოგვიწია მაინც ქავერზე დასმა, რადგან ვაი
    დაირექშენზე გააფუჭა დაპატარავებისას.
35. ელემენტები ფონტ ფემილის ავტომატურად აინჰერითებენ, მაგრამ ინფუთ ელემენტი არა.
36. ელემენტის დისფლეი ბლოკი(display:block) ზე თუ არაა დასეტილი,
    მაშინ block მოდელ ფროფერთებს(margin და ასე შემდეგ) ვერ გამოვიყენებთ.
37. &\_\_input:placeholder-shown {} as soon as placeholder is shown.
38. &**input:placeholder-shown &**label{} ასე ვასელექთებთ ლეიბელს, იმ შემთხვევაში,
    როცა ლებლი შვილი ელემენტი იქნებოდა ინფუთის, მაგრამ არ არის. ლეიბლი სიბლინგი, ერთ დონეზე არიან
    და ამ შემთხვევაში სიბლინგ სელექტორი + უნდა გამოვიყენოთ:
    &**input:placeholder-shown + &**label{} - adjecement sibling: it is a just sibling
    that comes immediately after the element that we select in the first place(ამ შემთხვევაში
    input). მაგრამ მათ შორის სხვა ელემენტიც რომ იყოს,
    მაინც შეგვეძლებოდა adjacement sibling selector - ის გამოყენება, მაგრამ მეორნაირის(~):
    &**input:placeholder-shown ~ &**label{}. ~ is general sibling selector. This works
    when there is a more levels in between.
39. ოფასითისით რომ ვაქრობთ, ვიუზე მაინც რჩება და visibility:hidden ით კი
    it is gone. მაგრამ ოფაისთის animating შეგვიძლია, მაგრამ ვიზიბილითის არა.
    ამიტომ ვიყენებთ ერთად.
40. რადიო ბათონების გასტილვა სიესესით არ შეგვიძ₾ია და ამიტომ ჩვენი რადიო ბათონების აგება გვიწევს
    და ჩვენს შემთხვევაში ლეიბლში სპანი ჩავსვით და ის გავსტილეთ და ინფუთ ელემენტი კი დავმალეთ.
    და რადგანაც ლეიბლი და ინფუთი დაქონექთებული გვაქვს, მასზე დაკლიკვისას(თან მასშია ჩასმული
    ჩვენი აგებული რედიო ბათონი) რედიო ბათონი მაინც ინიშნება - that is the trick.
41. display:inline-block; does not create line break.
42. after ში აუცილებელია რომ გვქონდეს კონტენტი, display:block, height და width.
43. ფორმაში a ენქორ ელემენტი არ გვინდა, რადგან ექშენი უნდა მოხდეს(დასაბმითება).
44. ბათონის ვიზითიდ და ლინკ სტეიტი არ აქვს ენქორ ელემენტისგან განსხვავებით.
45. უტილიტი კლასებში !important ების დაწერა ჩვეულებრივი პრაქტიკაა, რადგან
    ჩვენ გვინდა რომ ეს კლასები დაედოს, რაც არ უნდა იყოს.
46. inline ელემენტები ისე იქცევიან, როგორც ტექსტი.
47. inline-block მთლიან სიგრძეს არ იკავებს, არამედ იმდენს იკავებს, რამდენიც კონტენტს ჭირდება.
48. position:fixed ანალოგიურად მუშობს, როგორც აბსოლუტ, მაგრამ ფიქსავს.
49. cubic-bezier sites: https://cubic-bezier.com/ https://easings.net/
50. transform-origin:left defines where transformation should happen.
51. linear gradient ერთი მხრიდან იწყებს ფერის ცვლილებას და radial-gradient კი
    შუიდან იწყებს და გარშემო დაირექშენზე გადადის და ცვლის ფერს.
52. hyphens რომ გამოვიყენოთ გვჭირდება html ტეგში ენა გვქონდეს დასეტილი:
    <html lang="en">.
53. display:none ით we can not do animate anymore, instead we can use opacity:0
    and visibility:hidden; ოფასითი არაა საკმარისი, რადგან მაგით კი გავაქრობთ,
    მაგრამ ელემენტი ისევ ვიუზე იქნება და ამიტომ ვიზიბილითის გაწერაც გვჭირდება.
54. მაგალითად მიქსინში თუ გვიწერია ტრანსფორმი, და მერე მოგვიანებით კლასში ტრანსფორმზე
    რამის დამატება თუ გვინდა, მაშინ რაც მიქსინში გვიწერია ეგეც უნდა გადმოვაკოპიროთ და
    ახალიც დავამატოთ.
55. mobile first - min-width, desktop first - max-width.
56. Rem and em in the media queries are not affected by
    a root font-size settings. This means that one rem or one em
    in a media query is always just equal to the font-size
    which is coming from the browser and that is by default 16px. მაგრამ იუზერმა ხელით რომ შეცვალოს 20 ფიქსელზე, ეს იუნითებიც
    20 ფიქსელი იქნებიან, no matter what we have in our base font definition.
    ასევე, მედიქ ეურიში უნდა გამოვიყენოთ ემი, რადგან რემი ზოგ ბრაუზერში
    ამ დროს უცნაურად იქცევა და ყველაზე ოპტიმალური ოფშენი ემი არის.
57. მედია ქუერების ორდერი მნიშვნელოვანი, თავიდან ყველაზე დიდი ვიუპორტი და
    ბოლოში ყველაზე პატარა ვიუპორტი უნდა იყოს - ეს desktop-first approach - ზე
    არის, რადგან max-width ებს ვიყენებთ და mobile-first approach - რომ იყოს,
    იქ რადგანაც min-width ებს ვიყენებთ, მაშინ მედია ქვერების განლაგება პირიქით იქნებოდა: ჯერ პატარა ვიუპორტები და მერე უფრო დიდები ბოლოში.
58. (min-resolution: 192dpi) and (min-width: 37.5em), (min-width: 125em)
    და მძიმით or - ს ნიშნავს.
    https://caniuse.com/
59. ფრეფიქსიან(webkit) ფროფერთის ვწერთ ყოველთვის ჯერ პირველს და მერე ორიგინალს.
60. backdrop-filter: blur(10px) მსგავსი ეფექტი filter:blur(3px) ით მივაღწიეთ, მაგრამ
    ბექდროპი ელემენტის ბექრაუნდზე დავსვით და ფილტერი კი თვითონ ელემენტზე.
61. მარტო ეკრანის ზომით ვერ გავარკვევთ მედია ქვერებში თაჩდ დევაისი არის თუარა, ჰოვერებთან
    როცა გვაქვს საქმე და ამიტმ დამატებით რაღაცას ვიყენებთ მედია ქვერში:
    @media only screen and (max-width: 56.25em), only screen and (hover: none).
    (hover:none) დაეეფლაიებს სტილებს, თუ დევაისის დაჩდ არის და ჰოვერინგი ნაკლებად შეუძლია.
    (hover: hover) კი (hover:none) - ის საპირისპიროა.
