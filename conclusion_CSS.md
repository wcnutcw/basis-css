
อ้างอิงไปที่ไฟล์ css
    <link rel="stylesheet" href="ชื่อไฟล์">  ใส่ในส่วนของ <head>

    การตกแต่งwebใส่ไว้ในไฟล์ CSS แล้วค่อยใส่ในไฟล์ html



เขียน comment ใน <style>... </style> หรือ ในส่วน css ที่ไว้ใช้กำหนดstyleหรือการตกแต่ง
   ใช้ /**/  หรือ ctrl+/


unit ใน CSS แบบ absolute(แบบตายตัว)
    px : pixel
    pt : point  (1pt = 1/72 inches)
    cm : centimete
    mm : millimete
    in : inches(นิ้ว) (1in = 96px =2.54cm)
    pc : picas (1pc = 12pt)


unit ใน CSS แบบ Relative(แบบอัตราส่วน) : ออกแบบหน้า web แล้วสามารถแสดงผลในอุปกรณ์ต่างๆที่มีขนาดแตกต่างกันได้ เช่น มือถือ (Responsive web design)

    % : เป็นการกำหนดขนาดเป็น % (ใช้กับความกว้างหรือสูง)
    em : อ้างอิงขนาดกับ element parent(ตัวที่ใกล้ที่สุด) ที่ใกล้ที่สุด คือ จำนวนเท่าของขนาดปัจจุบัน
        เช่น ถ้าตอนนี้ใช้10px แล้วกำหนดขนาดเป็น 2em หมายถึง 2เท่าของขนาดปัจจุบัน คือ 20px
    rem : กำหนดขนาดโดยอ้างอิง root element(ตัวที่อยู่นอกสุดในส่วนของ head) ปกติ font-size จะอยู่ที่ 16px ( 1rem = 16px  : remปรับตามweb browserในส่วนของ<head> : แนะนำให้ใช้เพราะยืดหยุ่นปรับตามขนาดอุปกรณ์ได้) 
    vw :1%หรือ1/100 ของ viewport width
        - width ของ browser viewport เท่ากับ 750px ค่า 1vw=7.5px
    vh : 1%หรือ1/100 ของ viewport height
        - height ของ browser viewport เท่ากับ 900px ค่า 1vh=9px
    vmin,vmax : กำหนดค่าต่ำสุด และค่าสูงสุดของ viewport


Universal Selector : กำหนด style sheet มีผลต่อทุกtag โดยใช้ *
    *{
        attribute : value;
    }


font-family : กำหนดชนิด font เดียวหรือหลายfont
    font1;
    หรือ
    font1,font2,font3;

    *กำหนดfontได้มากกว่า 1 ชนิด ในกรณีBrowserไม่รองรับfontชนิดแรก ก็จะไป font ตัวที่2แทนไปเรื่อยๆ

    font : https://www.cssfontstack.com/

    google font: https://fonts.google.com/


font-size : กำหนดขนาดข้อความ
    แบบคงที่ : xx-small , x-small , medium . large , x-large , xx-large
    แบบตัวเลข : 10px , 20px


กำหนดความหนาข้อความ 
    font-weight ได้2แบบ
        แบบค่าคงที่ : lighter , bold(ตัวหนา) , bolder(ตัวหนากว่า)
         แบบตัวเลข : 100,200,...,800,900

    font-style : กำหนดตัวเอียง โดยค่าที่กำหนดคือ italic , oblique(4องศา)


กำหนดสีใน css 
    color 4 แบบ
        ชื่อสี
        RGB : (red , green , blue)
            rgba ( red , green , blue , alpha->ค่าความโปร่งใส (0 ถึง 1))
        Hexadecimal เช่น #FFF
        HSL : (hue(ความเข้มของสี) , saturation(ความคมชัดของสี) , lightness(ความสว่างของสี))

        * ดูในเน็ตได้ 
        * color picker

การกำหนดลักษณะข้อความ
    text-decoration กำหนดได้ 4 แบบ    
        none : ค่าว่าง 
        underline : ขีดเส้นใต้
        overline : ขีดเส้นเหนือข้อความ
        line - through : ขีดเส้นทับข้อความ

การจัดแนวข้อความ
    text-align กำหนดได้ 4 แบบ
        - left , right , center (ชิดด้านซ้าย ขวา และกึ่งกลางตามลำดับ)
        - justify (การกระจายข้อความให้ทุกบรรทัดมีความกว้างเท่ากัน)


กำหนดความกว้างและความสูง
    width ใช้กำหนดความกว้างของวัตถุที่ต้องการ
    height ใช้กำหนดความสูงของวัตถุที่ต้องการ
        auto คือ browser จะกำหนดให้เอง
        length คือ ความกว้างแบบหน่วยวัด เช่น px cm 
        % คือ ความกว้างแบบ % (ยืดหยุ่นตามขนาดหน้าจอได้)

ความกว้างและความสูงด้วย max,min
    width-min : ใช้กำหนดความกว้างต่ำสุด
    width-max : ใช้กำหนดความกว้างสูงสุด
    height-min : ใช้กำหนดความสูงต่ำสุด
    height-max : ใช้กำหนดความสูงสูงสุด

    หน่วยที่รองรับ
        none ไม่กำหนด default
        length คือ กำหนดแบบหน่วยวัด เช่น px cm เป็นต้น
        % คือ กำหนดแบบ % (แบบยืดหยุ่น)

การกำหนดเส้นขอบ : Border 
    border : <รูปแบบเส้น><ขนาด><สี>

    รูปแบบเส้น ประกอบด้วย solid(เส้นทึบ) dotted(แบบจุด) dashed(เส้นประ)

    ขนาด คือ ความกว้างของเส้นกำหนดเป็นตัวเลขตามหน่วย
    สี กำหนดรูปแบบเหมือน font เลย เช่น ชื่อสี,rgb,hex

    border-radius : ความโค้ง

การกำหนดรูปแบบเส้นขอบ (style)
    border-style : <รูปแบบเส้น>
        รูปแบบเส้น ประกอบด้วย solid(เส้นทึบ) dotted(แบบจุด) dashed(เส้นประ)
    
    border-xxx-style : <รูปแบบเส้น>
        xxx คือ ทิศทางของรูปแบบเส้นขอบ

การกำหนดสีเส้นขอบ    : border คือ  กำหนดเส้นขอบ
    border-color : <สี> 
        ประกอบด้วย rgb , ชื่อสี , hex

    border-xxx-color : <สี>
        xxx คือ ทิศทางของรูปแบบเส้นขอบ


การกำหนดขนาดเส้นขอบ (width)
    Border คือ การกำหนดเส้นขอบ 
        border-width : <ขนาด>
        border-xxx-width : <ขนาด>
            xxx คือ ทิศทางของรูปแบบเส้นขอบ

        <ขนาด>
            แบบระบุค่าคงที่ :
                medium - ขอบปานกลาง
                thin - ขอบบาง
                thick - ขอบหนา
                initial - ค่าเริ่มต้น
                inherit - อ้างอิงตาม parent element
            แบบตัวเลขได้ ตามด้วยหน่วย เช่น 10px , 10pt เป็นต้น

การกำหนดความโค้งของเส้นขอบ (radius)
    border-radius : <ค่าความโค้ง>

    border-xxx-radius: <ค่าความโค้ง>
        xxx คือ ทิศทางรูปแบบเส้นขอบ


Box Model : การจัดวางตำแหน่งหน้า web 
   การกำหนดพื้นที่รอบ Element
        Margin : กำหนดระยะห่างจากเส้นขอบหรือพื้นที่ภายนอก (ช่องว่างข้างนอก)
        Padding : กำหนดพื้นที่ระยะห่างภายในของ Element (ช่องว่างข้างใน)
        Border : กำหนดเส้นขอบ
            กำหนดทิศทางได้ ได้แก่ top bottom riht left 

        margin : ค่าที่กำหนด  เช่น margin : 10px (ทุกทิศทางมีขนาด 10px)
            margin : auto (ให้webคำนวณให้)

            การกำหนดพื้นที่รอบ element
                4แบบ
                    เช่น margin : 10px 5px 15px 20px  (เริ่มจากข้างบนแล้วหมุนตามเข็ม)
                        top margin = 10px
                        right margin = 5px
                        bottom margin = 15px
                        left margin = 20px
                    
                Padding : กำหนดพื้นที่ระยะห่างภายในของเส้นขอบกับ content
                    มีโครงสร้างเหมือนกับ margin แค่เปลี่ยนชื่อเป็น padding


การกำหนดสีพื้นหลัง (background)
    background-color : <สี> หรือ transaprent (ความโปร่งใส)
        <สี> ได้แก่ rgb , ชื่อสี ,hex

การกำหนดภาพพื้นหลัง (background)
    background-image : url(รูปภาพ)

    background-repeat : xxx;   (ไม่ให้ภาพทำซ้ำ)
        repeat (ค่า default ทำให้ภาพเต็มพื้นที่ของelement)
        repeat-x (จัดเรียงเฉพาะในแนวแกน X)
        repeat-y (จัดเรียงเฉพาะในแนวแกน Y)
        no-repeat (ไม่จัดเรียงแนวแกน x,y แสดงภาพพื้นหลังภาพเดียว)

        กำหนดคุณสมบัติพื้นหลัง
            background-attachment 
                scroll : การเลื่อนพื้นหลังตาม scrollbar
                fixed : การตรึงพื้นหลังไว้กับที่


กำหนดตำแหน่งพื้นหลัง ใช้ background-position
    เช่น background-position : center right;(กลาง,ขวา)
            left right center
                top center bottom

กำหนดขนาดภาพ (background-size)
    background-size : กำหนดค่า
        auto ค่าปกติภาพเท่าเดิม
        px หรือ %  (% สามารถยืดหยุ่นตามอุปกรณ์ที่เปิดได้)
        cover ขยายภาพทั้งความกว้างความสูงเต็มจอในอัตราส่วนเท่ากัน (ส่วนใหญ่ใช้ cover)
        contain ขยายภาพทั้งความความสูงชนของ browser



กำหนดพื้นหลังแบบหลายคุณสมบัติพร้อมกัน ( เขียนในบรรทัดเดียว )
    สามารถกำหนดโดยใช้ property ชื่อว่า background
       background : white url(images/logo.jpg) no-repeat fixed center center;


กำหนดตำแหน่งด้วย float
    float : กำหนดให้ element สามารถลอยอยู่ด้านใดด้านหนึ่ง 
        ค่าที่กำหนดได้คือ    left , right  ( ลอยด้านซ้ายและขวาตามลำดับ)
                         inherit ( ลอยตาม parent element )
                         none ไม่ให้มีการลอย ( default )
    clear : ไม่อนุญาตให้มีการลอยของ element 
        ค่าที่กำหนดได้คือ left , right ( ไม่อนุญาตให้มีการลอยด้านซ้ายและขวาตามลำดับ)
                      both ( ไม่ให้ลอยทั้งคู่)


กำหนด style ให้กับ link
    a:link  -> กำหนด style ให้กับ link ที่ยังไม่ถูกคลิก
    a:visited -> กำหนด style ให้กับ link ที่ถูกคลิกแล้ว
    a:hover -> กำหนด style ให้กับ link เมื่อนำเมาส์ไปวาง
    a:active -> กำหนด style ให้กับ link ขณะที่ถูกคลิก



Display Inline , Block , Inline-Block
    display : การจัดรูปแบบการแสดงผลข้อมูล layout
        - none : ไม่มีการแสดงผล
        - block : แสดงผลแบบ block โดยการขึ้นบรรดทัดใหม่ก่อน (เรียงในแนวตั้ง)
        - inline : แสดงผลแบบ inline โดยไม่มีการขึ้นบรรดทัดใหม่ (เรียงในแนวนอน)
        - inline-block : แสดงผลแบบแนวนอนและขยายพื้นที่ด้านใน 

Visibility : แสดงหรือซ่อนวัตถุหน้าweb โดยไม่กระทบlayout ใช้ visibility
    hidden : ซ่อนวัตถุ
    visible  : แสดงวัตถุ 


การจัดตำแหน่งด้วย Position
    position ใช้ในการจัดตำแหน่งของวัตถุ
        static - จัดวางแบบปกติเป็นค่า default
        relative - ใช้ในการจัดวางและกำหนดตำแหน่งวัตถุโดยการนับจากจุดที่วัตถุนั้นๆอยู่
            กำหนดจุดอ้างอิงโดย top right bottom left
        absolute - ใช้ในการจัดวางวัตถุ ให้ไปอยู่ตำแหน่งใดก็ได้แต่ต้องกำหนดตำแหน่งจากขอบของ element ที่บรรจุ วัตถุนั้นๆอีกที
            (ถ้าไม่มีอะไรครอบก็ถือว่า body เป็น element ที่ครอบวัตถุที่ระบุ absolute )  คือ ขยับอยู่ภายในกล่อง
        fixed - ใช้ในการจัดวางวัตถุให้อยู่ตำแหน่งเดิม (เลื่อนขึ้นลง ก็จะยังอยู่ตำแหน่งเดิมให้เห็น)
        sticky - ให้วัตถุติดขอบเมื่อเลื่อนไปถึง (คล้ายๆกับ fixed)
            กำหนด top =0 คือติดขอบด้านบน


            scroll-behavior: smooth;   /* กดคลิ้กลิ้งแล้วเลื่อนลงแบบ smooth*/



ลำดับความสำคัญของ style 
    เรียงลำดับจาก ล่างขึ้นบน
        ใช้ !importabt กำหนดให้มีความสำคัญที่สุด
            เช่น color:red !important;



จำกัดการแสดงผลข้อมูลด้วย Overflow : ใช้เมื่อมีเนื้อหาบนหน้าเว็บเยอะๆ
    Overflow
        - visible แสดงข้อมูลทั้งหมด
        - hidden ซ่อนข้อมูลที่เกิน
        - scroll ให้มี scroll bar แสดงผลเมื่อมีข้อมูลเกิน
            - overflow:scroll
            - overflow-x : scroll
            - overflow-y : scroll
        - auto ให้มี scroll bar แสดงผลออกมาอัตโนมัติ


Cursor Style : กำหนด style ให้กับ cursor (ตัวที่ใช้คลิ้ก) อยากให้มีไอคอนที่เปลี่ยนไป

    cursor style : https://i.sstatic.net/gJYJv.gif

ิิ
กำหนดเงาให้วัตถุด้วย Box-shadow
    box-shadow : x y blur spread color   (ตามลำดับ)
        x คือ เงาแกน x(+ ขวา,-ซ้าย)
        y คือ เงาแกน y(+ ล่าง ,- บน)
        blur คือ ขนาดความมัวของเงา
        spread คือ ขนาดของเงา 
        color คือ สีของเงา (color name,rgb,hex)


กำหนดค่าความทึบ ใช้ opacity
    opacity : value 
        - ค่าอยู่ระหว่าง 0.0 - 1.0
        - ยิ่งค่าน้อย ยิ่งจาง
        - ยิ่งค่ามาก ยิ่งทึบ


Responsive Web Design : ตอบสนองแสดงผลได้ดีในอุปกรณ์ที่มีขนาดแตกต่างกัน   
    Media Query : รูปแบบการเขียน Style ให้แสดงผลตามขนาดหน้าจอที่แตกต่างกัน  (เขียนที่css)

        @media ขนาดอุปกรณ์ {
            ...style...
        }
        @media screen,printer{
            ...style...
        }

        ความกว้างของอุปกรณ์
            320ox-480px : Mobile devices
            481px-768px : IPads , Tablets
            769px-1024px : Laptops
            1025px-1200px : Desktops
            1201px ขึ้นไป : TV, Widescreen

            * ดูขนาดหน้าจอได้ที่ google inscpect

Viewport Units : สามารถทำให้ web แสดงผลบน smart phone , tablet ได้ผ่านการอ้างอิงพื้นที่หรือสัดส่วนของตามอุปกรณ์ที่ใช้งาน   *สำคัญ*
    เขียน viewport ใน <meta name='viewport'>
    viewport คือช่วยจัดส่วนตามที่กำหนด เช่น 100px แล้ว กำหนด viewport=10% ก็คือ ให้แสดงผลแค่ 10px จาก 100px
    vw - บอกสัดส่วนความกว้างเป็น %
    vh - บอกสัดส่วนความสูงเป็น %
    vmin - ค่า % ต่ำสุดของ viewport
    vmax - ค่า % สูงสุดของ viewport


Flexbox : ช่วยในการจัด element ต่างๆในwebให้มีความง่ายและยืดหยุ่นมากขึ้น 
    (ในปัจจุบันการพัฒนาเว็บมีความซับซ้อนมากยิ่งขึ้นทำให้การใช้ layout modeไม่ดีเท่าไร [layout คือ block ,inline,position และอื่นๆ])

    1) จัดเรียงตำแหน่ง element ได้ง่ายขึ้น จากบนลงล่าง ซ้ายไปขวา อื่นๆ
    2) กำหนดขนาดให้พอดีกับพื้นที่ว่างแบบอัตโนมัติ (Sizing)

    องค์ประกอบของ Flexbox
        1) container (กล่องที่ครอบ items)
        2) items (สมาชิกใน container) แบ่งพื้นที่ให้ item ในจำนวน % ที่เท่ากัน
            เช่น มี 3 item ก็จะแบ่งเป็น 33.33% ให้กับ 3 item
                  (จังเรียงได้หลากหลายแบบ ในแนวนอน หรือ แนวตั้งก็ได้)

    .container{
        display:flex;
        box-sizing : border-box;   
    }
        border-box : กำหนดขนาดให้พอดีกับพื้นที่ว่างโดยคำนวณจากค่าจริงที่ผู้ใช้กำหนด (border(เส้นขอบ) + padding) เพื่อไม่ให้ item แสดงผลเพี้ยน (ระบุหรือไม่ระบุก็ได้)
                     เช่น 500px ให้กับ item เป็นค่าจริง
        flex : กำหนดให้ container แบบ flex   ( จัดเรียงในแนวนอนเป็น default)

    กำหนดทิศทางด้วย flex-direction
        row (ค่าเริ่มต้น) : จัดวาง items ในแนวนอนทิศทางเดียวกับแกนหลัก (แกนหลัก คือ ตามการจัดเรียง item-1 item-2 item-3 ตามลำดับ)
        column : จัดวาง items ในแนวตั้งทิศทางเดียวกับแกนหลัก          ( แกนหลัก -> flex-direction: row หรือ flex-direction: column)
        row-reverse : จัดวาง items ในแนวนอนทิศทางตรงข้ามกับแกนหลัก
        column-reverse : จัดวาง items ในแนวตั้งทิศทางตรงข้ามกับแกนหลัก 

    กำหนดขนาดด้วย flex-wrap (ห่อหุ้มitemด้านใน : ในกรณีที่ item เกินพื้นที่ container ออกมา)
        กรณีที่ขนาด items ใหญ่กว่าพื้นที่ container
            nowrap :  จัดวาง items ที่เกินพื้นที่ container ไปด้านขวามือ (ค่า default)
            wrap  : จัดวาง items ที่เกินพื้นที่ container เรียงจากบนลงล่าง ( ห่อให้items ไม่เกินพื้นที่ container)
            wrap-reverse : จัดวาง items ที่เกินพื้นที่ container เรียงจากล่างขึ้นบน

    Flex-properties (กำหนดคุณสมบัติให้กับ items ที่อยู่ใน container)
        flex-shrink : ให้ item หดตัวเมื่อเทียบกับ item อื่นๆ 
            ค่าเริ่มต้นเป็น 1
                เช่น หด2เท่า เมื่อเทียบกับ item อื่นๆ
        flex-grow : ให้ item ขยายเมื่อเทียบกับ item อื่นๆ
            ค่าเริ่มต้นเป็น 0
                เช่น ขยายตัว2เท่า เมื่อเทียบกับ item อื่นๆ
        flex-basis : กำหนดค่าความยืดหยุ่นเริ่มต้น
            ค่าเริ่มต้เป็น 1 คือค่า default

        flex:1 ทำให้ item ที่อยู่ในแถวเดียวกันมีขนาดเท่ากัน

    Flex Justify (จัดวางตำแหน่ง item)
        **เทียบกับแกนหลัก เช่น กำหนดแกนหลักเป็นแนวนอน หรือ กำหนดแกนหลักเป็นแนวตั้งก็ได้

        justify-content 
            flex-start : ชิดซ้าย container ทิศทางตามแนวนอน/ตั้ง   (แนวนอน : จุดเริ่มต้นคือด้านซ้าย) (แนวตั้ง : จุดเริ่มต้นคือด้านบน)
            center : กึ่งกลาง container ทิศทางตามแนวนอน/ตั้ง
            flex-end : ชิดขวา container ทิศทางตามแนวนอน/ตั้ง
            space-around : ระยะห่างซ้ายขวาและขนาด item เท่ากัน
            space-between : ระยะห่างซ้ายขวาและขนาด item เท่ากัน (แนวนอน : ติดมุมซ้ายและขวา) (แนวตั้ง : ติดมุมบนและล่าง)

    Flex Alignment (จัดวางตำแหน่ง item)
        **เทียบกับแกนหลัก เช่น กำหนดแกนหลักเป็นแนวนอน หรือ กำหนดแกนหลักเป็นแนวตั้งก็ได้   (ทิศตรงข้ามกับแกนที่กำหนด)
                เช่น กำหนดแบบ column ย้าย item แบบแนวนอน

        align-items (item ทุกตัว) และ align-self (item ที่ต้องการ)
            stretch : กำหนดขนาด item เท่ากับขนาด container
            flex-start : ด้านบน container ทิศทางตามแนวนอน/ตั้ง
            center : กึ่งกลาง container ทิศทางตามแนวนอน/ตั้ง
            flex-end : ด้านล่าง container ทิศทางตามแนวนอน/ตั้ง


CSS Grid Layout 
    Flexbox ถูกออกแบบให้จัดการ layout แบบทิศทางเดียว คือ 1มิติ เช่น เรียงลำดับจากบนลงล่าง ซ้ายไปขวา มองแบบsingle(แนวตั้งและแนวนอนไม่ทำพร้อมกัน)
    Grid Layout ถูกออกแบบมาเพื่อจัดการ layout 2มิติ คือ แนวนอนและแนวตั้งในเวลาเดียวกัน มองแบบตาราง

        การใช้งาน -> display:grid;
        กำหนดขนาดแถว (ความสูง) -> grid-template-rows : ความสูงแถวที่1,2,3;
        กำหนดขนาดคอลัมน์ (ความกว้าง) -> grid-template-column : ความกว้างของคอลัมน์ที่1,2,3;
            ใส่ขนาดแบบ auto ได้ คือ สามารถยืดหยุ่นตามขนาดหน้าจอของแต่ละอุปกรณ์ได้
            สามารถย่อการเขียนโดยใช้ repeat() ได้
        เช่น  grid-template-columns: 100px 100px 100px;
                 เปลี่ยนเป็น grid-template-columns: repeat(3,100px);
        
        กำหนด column เริ่มต้น-สิ้นสุด
            เช่น     grid-column-start: 1;    /เริ่มที่เส้นที่ 1
                    grid-column-end: 3;      /จบที่เส้นที่ 3
                        เขียนลัดได้เป็น grid-column: 1/3;
        กำหนด row เริ่มต้น-สิ้นสุด
            เช่น  grid-row-start: 1;
                 grid-row-end: 3;


                 :first-child คือ item ตัวแรก
                 :last-child คือ item ตัวสุดท้าย

    Grid properties อื่นๆ 
        กำหนดสัดส่วนด้วย span  (ใช้แทน grid-column และ grid-row)
            เช่น grid-row:1/span 2;  (คือเริ่มจากเส้นที่ 1 กินพื้นที่ไป 2ส่วน ในแนวนอนนับเป็นช่อง : นับพื้นที่แบบกล่องแทนนับเส้น)
        กำหนดสัดส่วนพื้นที่ด้วยหน่วย fr  (บอกจำนวนเท่าของตัวgrid containerที่ครอบ)
            กำหนดสัดส่วน row column ให้เลย
                เช่น grid-template-columns: 1fr 1fr 1fr; (1ใน3 ของ columns ในขนาดที่เท่ากันทั้งหมด)
                        เขียนแบบลดรูปได้ grid-template-columns: repeat(3,1fr);
                    grid-template-columns: 1fr 3fr 1fr; (1in5 3in5 1in5)
        กำหนดระยะห่างพื้นที่ด้วย gap 
            เช่น   grid-row-gap:10px; (ระยะห่างระหว่างแถว 10px)
        กำหนดชื่อพื้นที่ด้วย grid-template-area  (กำหนดเป็นชื่อพื้นที่แทนการเขียนหมายเลข แค่เอามาใส่ยัดจับใส่ภายใน containe)
            ใช้ grid-area:ชื่อ; (เพื่อกำหนดชื่อ)
                เช่น    
                        .grid-container{
                        display: grid;
                        /* 2 column */
                        /* grid-template-columns: 2fr 4fr; */
                        /* 3 row */
                        /* grid-template-rows: 1fr 5fr 1fr; */

                        grid-template-areas: 
                        'header header'
                        'sidebar content'    
                        'footer footer'
                        ;
                        /* เขียนแบบลดรูปจาก grid-template ได้*/
                        grid-template-areas: 
                        'header header'1fr
                        'sidebar content'5fr    
                        'footer footer'1fr
                        /2fr 4fr;
                    }

                    .header-item{
                        background-color: greenyellow;
                        grid-area: header;
                    }

                    .content-item{
                        background-color: orange;
                        grid-area: content;
                    }

                    .footer-item{                                                                                                                                                                                                                               
                        background-color: black;
                        color: white;
                        grid-area: footer;
                    }

                    .sidebar-item{
                        background-color: blue;
                        grid-area: sidebar;
                    }

Advance Selectors (มีความซับซ้อน)
    Targeted Selectors (เลือกใช้ตามที่ต้องการ) /* child-selector*/
        เช่น             p{
                        background-color: orange;
                    }

                    /* descendant selector*/

                    div p{
                        background-color: greenyellow;
                    }

                    /* child-selector*/
                    div>p{
                        background-color: yellow;
                    }

    Style By attribute
    เช่น
                    a{
                background-color: orange;
            }

            a[target]{
                background-color: red;
                color: white;
            }

            a[target='_blank']{
                background-color: black;
                color: pink;
            }

            a[target='_self']{
                color:blue;
            }

    Special attribute
    เช่น 
                    input[type="email"],input[type="text"]{
                width: 100%;
                margin-bottom: 5px;
            }
            input[type="submit"]{
                color:white;
                background-color: red;
                border-radius: 10px;

            }
    
    Pseudo Selector (เลือกตัวลูกข้างใน ก็คือ item ที่อยู่ข้างใน container)
        fist-child : ตัวแรก
        last-child : ตัวสุดท้าย
        nth-child(ลำดับ) : ระบุลำดับในวงเล็บ
            นับจากล่างขึ้นบน
                เช่น 
                        li:nth-last-child(3){
                            background-color: yellow;
                        }
            นับทุกๆnตัว
                เช่น 
                        li:nth-child(3n){
                        background-color: blue;
                            }                  

            เฉพาะเลขคี่ ใส่ odd
            เฉลาะเลขคู่ ใส่ even 
                    ใส่ลงในวงเล็บของ li:nth-child(...)
    
    Before&After Pseudo
        before : ข้างหน้า (มาก่อน)
        after : ข้างหลัง (มาหลัง)
            เช่น
                    .is-required::before{
                            content: "*";
                            color: red;
                            padding-left:2px ;
                        }


กำหนดเงาให้ข้อความด้วย text-shardow
    text-shadow : x y blur color
        x คือ เงาแกน x (+ขวา,-ซ้าย)
        y คือ เงาแกน y (+ล่าง,-บน)
        blur คือ ขนาดความมัวของเงา
        color คือ สีของเงา (color name,rgb,hex)


CSS Variable : ลดขั้นตอนการทำงานซ้ำซ้อนได้เพื่อให้มีความเป็นระเบียบมากขึ้น (สร้างตัวแปรมาควบคุม style)
     ใช้ :root{} และ item ใช้ var(ชื่อตัวแปร) 
            ตั้งชื่อเองได้(custom variable) คือ --ชื่อตัวแปร  
      เช่น              
                :root{
                    --box:2px solid red;
                    --theme-color:orange;
                    --shadow:10px 10px var(--theme-color);
                    --space:5px;
                    --font:40px;
                }

                .box-1{
                    border:var(--box);
                    background-color: var(--theme-color);
                    box-shadow: var(--shadow);
                    margin: var(--space);
                    font-size:var(--font);
                }
                .box-2{
                    border:var(--box);
                    margin: var(--space);
                }
                .box-3{
                    border:var(--box);
                    background-color: var(--theme-color);
                    margin: var(--space);
                    box-shadow: var(--shadow);
                }


CSS Transform  : การจัดการตำแหน่งในรูปแบบต่างๆ ใช้ transform   พิกัดเริ่มต้นคือ(0,0) [โดยส่วนใหญ่เอาไปใช้กับการกำหนด effect ต่าง]
    translate(x,y) : กำหนดตำแหน่ง element
    scale(x,y) : ขยาย element
    rotate(มุม deg) : กำหนดการหมุนของ element   (หมุนทั้ง2แกน)
        กำหนดแกนได้ คือ rotateX(deg) , rotateY(deg) คือบีบอัดขนาดตามแกน
    skewX(มุม deg) : กำหนดการเอียงของ element แกน x 
    skewY(มุม deg) : กำหนดการเอียงของ element แกน y

CSS Transition : เปลี่ยนค่าใน element จากค่าหนึ่งไปสู่อีกค่าหนึ่งในช่วงเวลาที่กำหนด ใช้ transiton 
    transiton-properties : รูปแบบคุณสมบัติที่การเปลี่ยนแปลงค่า
        เช่น background-color
    transiton-duration : ระยะเวลาในการเปลี่ยนแปลงค่า
    transiton-timing-function : รูปแบบฟังก์ชั่นของการเปลี่ยนแปลง (ease-in)   [ไม่จำเป็นต้องระบุก็ได้เป็นแค่ระยะเวลาในการปรากฎตามกราฟ]
        ตามกราฟ ได้แก่ linear , ease , ease-in , ease-out , ease-in-out
    transiton-delay : ระยะเวลาที่จะเริ่มต้นเปลี่ยนแปลงค่า

     เช่น               
            body{
                background-color: #333;
                display: flex;
                align-items: center;
                justify-content: center;
                height: 100vh;
            }

            .box{
                background: orange;
                width: 100px;
                height: 100px;
                /* transition-property: background-color; */
                /* รอ2วิในการเปลี่ยนแปลง */
                /* transition-duration: 2s;
                transition-timing-function: ease-in; */
                /* รอ3วิก่อนเริ่มทำงาน */
                /* transition-delay: 3s ; */
                /* เขียนแบบย่อ */
                /* transition: background 3s , width 3s , border-radius 3s ease-in 3s; */
                /* ใช้ all ให้ property ทำพร้อมกัน และ เขียนแบบลดรูป */
                transition: all 3s ease-in 0.5s;
            }

            .box:hover{
                background-color: red;
                width: 300px;
                border-radius: 50%;
            }

CSS Animation  : ต่างจาก transition และ เล่นเองโดยอัตโนมัติ
    animation-name : ตั้งชื่อ animation
        พิมพ์คำสั่ง @keyframes ชื่อanimation{ } เพื่อกำหนด properties ต่างๆ
    animation-duration : ระยะเวลาของ animation จากเริ่มต้นไปสิ้นสุด
    animation-timing-function : รูปแบบการเล่น animation
    animation-iteration-count : จำนวนการเล่น animation (infinite คือไม่สิ้นสุด)
        พิมพ์ infinite เพื่อให้ animation เล่นแบบไม่รู้จบ
    animation-direction : ทิศทางการเล่น (เล่นจาก frame 1 ไป frame 10 หรือแบบ ย้อนกลับก็ได้)
        normal คือ เล่นปกติ
        alternative คือ สลับขนาด
            alternative-reverse
        reverse คือ เล่นจากหลังไปหน้า
    animation-delay : ระยะเวลาที่จะเริ่มต้น


    เช่น
                body{
                    background-color: #333;
                }
                .box{
                    background-color: white;
                    width: 100px;
                    height: 100px;
                    animation-name: animate1;
                    animation-duration: 2s;
                    animation-iteration-count: infinite;
                    animation-direction: alternate ;
                    animation-timing-function:ease-in-out;
                }

                @keyframes animate1{
                    from{
                        width: 100px;
                    }
                    to{
                        width: 400px;
                    }
                }


    กำหนดช่วงที่เกิด animation แต่ละ frame ที่เกิดขึ้น แบบเป็น %
    เช่น
            body{
                background-color: #333;
            }
            .box{
                background-color: white;
                width: 100px;
                height: 100px;
                position: relative;
                /* animation-name: animate2;
                animation-duration: 5s;
                animation-iteration-count: infinite ; */
                /* เขียนแบบลดรูป */
                animation: animate2 5s infinite;

            }

            @keyframes animate2{
                0%{
                    top:0;
                    left:0;
                    transform: rotate(0deg);
                    background-color: red;
                }
                25%{
                    top:0;
                    /* เว้นระยะจากทางซ้ายมือ 300px  */
                    left:300px;
                    transform: rotate(45deg);
                    background-color: yellow;
                }
                50%{
                    /* เว้นระยะจากด้านบน 300 */
                    top:300px;
                    left: 300px;
                    transform: rotate(90deg);
                    background-color:green ;
                }
                75%{
                    top:300px;
                    left:0;
                    transform: rotate(270deg);
                    background-color: orange;
                }
                100%{
                    top:0;
                    left:0;
                    transform: rotate(360deg);
                    background-color: red;
                }
            }
