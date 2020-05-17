# Quantum Computer คืออะไร? จะส่งผลอย่างไร? หลังจาก Google เปิดตัว “Sycamore Processor”

> Source : [Beartai.com : 25/10/2019](https://www.beartai.com/article/tech-article/371839).

![enter image description here](https://www.beartai.com/wp-content/uploads/2019/10/73195771_2128943534074176_4038582891167350784_n.png)

ก่อนอื่นอยากให้ทุกท่านที่ยังไม่เข้าใจเทคโนโลยีคอมพิวเตอร์ควอนตัมได้เข้าใจตัวเทคโนโลยีนี้กันก่อนนะครับ ก่อนจะเข้าสู่เนื้อหาว่า Google ประกาศว่าประสบความสำเร็จอะไร ด้านไหนในเทคโนโลยีคอมพิวเตอร์ควอนตัม และเทคโนโลยีนี้จะส่งผลอย่างไรต่อทุกคนบนโลก

## เทคโนโลยี Quantum Computer คืออะไร ?

หากจะพูดถึงคอมพิวเตอร์ควอนตัมคงจะต้องเริ่มจาก Qubit หรือ Quantum Bit กันก่อน เทคโนโลยีของคอมพิวเตอร์ควอนตัมนั้นเริ่มมาจากสิ่งที่เรียกว่า “Superposition” ใน Quantum Physics เมื่ออนุภาคขนาดเล็กสามารถมีตัวตนอยู่ได้หลายที่ในขณะเดียวกัน ซึ่งคอมพิวเตอร์ในปัจจุบัน ฐานที่เล็กที่สุดของการคำนวณคือ Bit หรือ Binary Digits ที่มีสถานะเป็น “0” และ “1” แต่กับคอมพิวเตอร์ควอนตัมเราจะไม่รู้ค่าของมันเลย มันอาจจะเป็น “0” หรือเป็น “1” หรือทั้งคู่ จนกว่าเราจะทำการวัดค่าของมัน ซึ่งก็คือสถานะ Superposition นั่นเอง Qubit จะยังไม่ตัดสินใจแสดงเป็นค่าใดค่าหนึ่ง ถึงแม้มีโอกาสที่ค่านั้นจะถูกกำหนดไว้แล้วก็ตาม

## Concept ของ Quantum Bit หรือ Qubit

![enter image description here](https://www.beartai.com/wp-content/uploads/2019/10/74666212_694349551049588_6526063829720236032_n-768x433.png)

โดยปกติ 1 Bit จะเก็บค่าได้แค่ “0” และ “1” แต่ Qubits จะเก็บค่าได้ซับซ้อนมากกว่านั้น คือไม่เป็น “0” และ “1” ก็เป็นทั้งคู่ หรือไม่เป็นทั้งคู่ นั่นแปลว่าใน 1 Qubits จะเกิด 2 ความเป็นไปได้ ซึ่งตามคอนเซ็ปต์ของ Superposition แล้ว หากเรามี 2 Qubits จะเกิด 4 ความเป็นไปได้ และ 3 Qubits เกิด 8 ความเป็นไปได้ และ 4 Qubits จะเกิด 16 ความเป็นไปได้ โดยจะอยู่ในรูปแบบ 2 กำลัง X ไปเรื่อย ๆ

## พูดถึง Quantum Computer ในแบบของ Google

![](https://www.beartai.com/wp-content/uploads/2019/10/73370634_504761833637878_886291824656777216_n-1024x576.png)

Google เริ่มโครงการ Quantum Computer ครั้งแรกจากความต้องการที่จะพัฒนา AI ในปี 2013 จึงจัดตั้งแลบเฉพาะเพื่อการศึกษา และค้นคว้าเกี่ยวกับ Quantum Computer เพื่อ AI หรือ QuAIL \(Quantum Artificial Intelligence Laboratory\) และยังได้รับการร่วมมือกับ NASA อีกด้วย โดยจุดประสงค์หลักคือการนำ Quantum Computer มาใช้งานกับ Machine Learning หรือ AI นั่นเอง จนในช่วงปี 2014 Google เริ่มต้นที่จะวิจัย Quantum Computer เพื่อที่จะสร้าง Quantum Processor ของตนเอง โดยใช้ชื่อ “Bristlecone” ซึ่งเดิมที Google ต้องซื้อ Quantum Computer มาจาก D-Wave \(เครื่อง D-Wave Two\) เพื่อใช้ในงานวิจัย

## มันทำงานอย่างไร ?

![enter image description here](https://www.beartai.com/wp-content/uploads/2019/10/030518_EC_google-quantum-computer_main.jpg)

ในชิปของ Quantum Processor ค่าไฟฟ้าจะถูกสะท้อนไปมาในวงจรที่มีรูปแบบพิเศษ ซึ่งถูกสร้างจากอลูมิเนียมบนชิปซิลิกอน โดยตัววงจรจะตีพลังงานกลับไปกลับมาด้วยพลังงานไฟฟ้าที่แตกต่างกัน 2 ค่าคือ “0” และ “1” เพื่อที่จะแปลงเปลี่ยนเป็นค่าสถานะควอนตัม แต่ละชิปของ Quantum Processor นั้นจะมี Qubits จำนวนมาก ซึ่งแต่ละ Qubit จะต้องกำหนดตัวเองเป็น 1 สถานะควอนตัม แต่จะต้องมี 2 ระดับในนั้น และเมื่อมีอนุภาคอื่น ๆ มาจับคู่เพื่อเกิดปฏิกิริยากับ Qubit แล้ว จะทำให้สถานะควอนตัมใน 2 ระดับนั้น ถูกแยกออกจากกันได้ตามอุดมคติ เกิดเป็น Clean Qubit Environment และเรายังสามารถควบคุมตัว Qubits เหล่านั้นให้มันจับคู่กัน หรือแลกเปลี่ยนพลังงานได้ตามความต้องการ

## แล้วอะไรคือ Clean Qubit Environment ?

![](https://www.beartai.com/wp-content/uploads/2019/10/72973517_2752639718121080_2137546025684959232_n-1024x682.png)

หากเราไม่ได้ใช้งาน Qubit ตัวมันจะต้องมีสถานะคงที่ กล่าวได้ว่า Qubit จะต้องไม่มีปฏิกิริยาเกิดขึ้นกับอนุภาคอื่น ๆ เลย จนกว่าเราจะใช้งานมันตามความต้องการเฉพาะ และนี่เป็นหนึ่งในวิธีการสร้าง Quantum Computer นักวิทยาศาสตร์จะต้องสร้างวงจรไฟฟ้าของ Qubit ด้วยสภาวะ “Superconductor” หรือสภาวะที่เป็นสื่อนำแบบยิ่งยวด \(นั่นแปลว่าอัตราการสูญเสียค่าพลังงานไฟฟ้าในวงจรไฟฟ้านี้จะน้อยมาก ๆ และมันสำคัญอย่างไรจะอธิบายในหัวข้อถัดไป\) และสภาวะ Superconductor นี้ จะทำงานได้ในอุณหภูมิที่ต่ำมาก ๆ โดยนักวิทยาศาสตร์จะใช้อุปกรณ์ที่เรียกว่า Cryostat \(อุปกรณ์ที่ทำให้เกิดสภาพแวดล้อมอุณภูมิที่ต่ำมาก ๆ\) ทำให้อุณภูมิคงที่ที่อุณภูมิ 50 องศามิลลิเควิน หรือประมาณ -273.1 องศาเซลเซียส และยังต้องอาศัยสภาวะสุญญากาศ ที่จะทำให้เกิด Clean Qubit Environment อีกด้วย

## อธิบายการทำงานของ Quantum Computer ทั้งหมดแบบคร่าว ๆ

![](https://www.beartai.com/wp-content/uploads/2019/10/109341788_mediaitem109341787.jpg)

โดยเครื่อง Cryostat จะเป็นเครื่องแบบพิเศษที่ถูกออกแบบมาใช้งานกับ Quantum Processor โดยเฉพาะ ซึ่งประกอบด้วยชั้นแผงหลาย ๆ ชั้น มันจะทำงานแบบจากด้านบนไล่ลงไปด้านล่าง โดยส่วนด้านบนจะเป็นส่วนที่มีอุณหภูมิสูงที่สุด และค่อย ๆ เย็นลงไปจนสุดด้านล่าง ทั้งหมดนี้เพื่อสร้างความเย็นที่เอื้อต่อระบบการทำงานของ Quantum Processor

![](https://www.beartai.com/wp-content/uploads/2019/10/72467328_542613559861246_9013784702326145024_n-1024x576.png)

อุปกรณ์ทั้งหมดจะถูกติดตั้งรอบ ๆ แผงที่เป็นชั้นเหล่านั้น และด้านส่วนล่าง ที่เป็นส่วนที่เย็นที่สุดจะถูกติดตั้งด้วย Quantum Processor นั่นเอง ซึ่งแต่ละชิป Qubit ทั้งหมดจะต้องถูกต่อเข้ากับเครื่อง Cryostat ผ่านสายที่จะหล่อเลี้ยงให้อยู่ในระดับอุณหภูมิที่ระบบต้องการ และสายเหล่านั้นยังใช้เพื่อเชื่อมต่อเพื่อระบุค่าสัญญาณของ Qubits ที่เข้าออกจากตัว Quantum Processor อีกด้วย โดยจะมีคอมพิวเตอร์ที่อยู่ด้านนอกควบคุมการส่ง และอ่านสัญญาณ Qubits ที่สร้างด้วยสัญญาณไมโครเวฟรูปแบบเฉพาะด้วยคอมพิวเตอร์อีกทีหนึ่ง \(เป็นส่วนสำคัญว่าทำไม Quantum Processor ต้องทำงานในระดับที่มีความเย็นต่ำมาก เพราะต้องการให้เกิดการสูญเสียสัญญาณให้น้อยมากที่สุด\)

## Quantum Computer Supremacy คืออะไร ?

![](https://www.beartai.com/wp-content/uploads/2019/10/73325573_530486201080739_7080892893338009600_n-1024x576.png)

Quantum Computer Supremacy เป็นเหมือนจุดสูงสุดในการพัฒนาเทคโนโลยีคอมพิวเตอร์ควอนตัม โดยนิยามนี้เริ่มจากการทดลองลดอัตราการเกิดข้อผิดพลาดในระบบ ซึ่งปกติจะเกิดข้อผิดพลาดอยู่บ้างจากการลัดกันของวงจร โดยตอนแรกสามารถแก้ปัญหานี้ได้โดยการปรับค่าของวงจรควอนตัมให้ถูกต้อง ด้วยวิธีการจำลองการทำงานของคอมพิวเตอร์ควอนตัม ด้วยซูเปอร์คอมพิวเตอร์ในปัจจุบัน เพื่อหาค่ามาตราฐานสำหรับวงจร และนำมาปรับใช้กับคอมพิวเตอร์ควอนตัม แต่วิธีนี้เมื่อเริ่มจำลองการทำงานที่ซับซ้อนมากขึ้นเรื่อย ๆ ซูเปอร์คอมพิวเตอร์ปกติจะทำงานตามไม่ทัน จึงเกิดนิยาม Quantum Computer Supremacy ขึ้นมา

![](https://www.beartai.com/wp-content/uploads/2019/10/73243273_2495005723920326_137386013705109504_n-1024x579.png)

ก่อนอื่นจะต้องอธิบายเกี่ยวกับ “Church-Turing Thesis” หรือ “ทฤษฏีการคำนวณ” ก่อน ในทฤษฏีการคำนวณของวิทยาการคอมพิวเตอร์นั้น กล่าวไว้ว่า “การทำงานของคอมพิวเตอร์ทั้งหมดในโลกนี้จะต้องสมมูลกัน” กล่าวคือ ต้องสามารถจำลองซึ่งกันและกันได้ แต่พอนำทฤษฎีการคำนวณนี้มาเทียบกับคอมพิวเตอร์ควอนตัมแล้ว ทฤษฏีนี้มันไม่เป็นจริงเลย ซึ่งคอมพิวเตอร์ควอนตัมสามารถคำนวณได้รวดเร็วอย่างทวีคูณ เพราะฉะนั้นการพิสูจน์ว่าสามารถวิจัยจนสำเร็จในนิยาม “Quantum Computer Supremacy” หรือการทดลองไปถึงจุดขึ้นสูงสุดของเทคโนโลยีคอมพิวเตอร์ควอนตัมได้แล้วนั้นคือการแหกกฏทฤษฏีการคำนวณนี้โดยสิ้นเชิง

โดยวิธีที่จะทดลองว่าสำเร็จได้จริงนั้น Google จะต้องทำการทดลอง ด้วยการนำวงจรไฟฟ้าซับซ้อนวงจรหนึ่งมาทดสอบเวลาในการคำนวณ ทั้งบนคอมพิวเตอร์ควอนตัม และคอมพิวเตอร์ปกติ แล้วนำมาเทียบเพื่อดูความแตกต่างของระยะเวลาในการคำนวณ จนกว่าจะถึงจุดที่คอมพิวเตอร์ปกติที่เทียบกับควอนตัมคอมพิวเตอร์แล้ว คำนวณได้นานเกินไปกว่าช่วงชีวิตคนจะรอไหว หรือก็คือเป็นไปไม่ได้นั่นเอง นั่นถือว่าเป็นการประสบความสำเร็จในการทดสอบคอมพิวเตอร์ควอนตัมขั้นสูงสุดแล้ว

![](https://www.beartai.com/wp-content/uploads/2019/10/76612249_3022706091091770_3375989962766811136_n-1024x580.png)

และล่าสุด Google ทดลองจนสำเร็จตามนิยามของ Quantum Computer Supremacy แล้ว โดยใช้ชิปประมวลผลควอนตัมที่ชื่อ Sycamore Processor ซึ่งเจ้าชิปตัวนี้บรรจุ Qubits ไว้ถึง 53 ตัว \(น้อยกว่า Bristlecone ที่ 72 แต่ใช้งานได้จริงตามทฤษฏี\) ซึ่งจากตัวชิปมีทั้งหมด 53 Qubits แปลว่า ในหนึ่งชิป เกิดได้ทั้งหมด 2 ยกกำลัง 53 ความเป็นไปได้ นั่นแปลว่าในหนึ่งการคำนวณสามารถคำนวณได้ถึง 10,000 ล้านล้าน ความเป็นไปได้เลยทีเดียว โดย Google เคลมว่า มันสามารถคำนวณสิ่งที่ซูเปอร์คอมพิวเตอร์ที่เร็วที่สุดในโลกต้องใช้เวลา 10,000 ปีในการคำนวณ แต่ชิปตัวนี้ใช้เวลาเพียง 3.20 นาที

## แล้วเทคโนโลยี Quantum Computer จะส่งผลอะไรต่อโลกนี้บ้าง ?

ในเมื่อประสิทธิภาพของเทคโนโลยีคอมพิวเตอร์ถูกพัฒนาไปมากขนาดนี้ มันจะส่งผลอย่างไรต่อสิ่งรอบตัวเรา หรือโลกใบนี้บ้าง

* AI ที่สามารถพูดคุย และโต้ตอบได้อย่างแท้จริง

AI ที่สามารถตอบสนองและพูดคุยในปัจจุบัน ยังต้องใช้เวลาในการตอบโต้อยู่บ้าง แต่เมื่อมาถึงยุคของคอมพิวเตอร์ควอนตัน หากนำเทคโนโลยี AI และคอมพิวเตอร์ควอนตัมมาใช้งานร่วมกัน ปัญญาประดิษฐ์เหล่านี้จะสามารถเข้าถึงการคำนวณที่รวดเร็วอย่างมาก ทำให้ตอบโต้มนุษย์ได้อย่างไร้ความหน่วง เสมือนพูดคุยกับมนุษย์ทั่วไปเลยทีเดียว

* เนื่องด้วยจากเทคโนโลยี AI และ Machine Learning อาจสร้างยาชนิดใหม่ ช่วยชีวิตคนได้เพิ่มขึ้น

ด้วยการคำนวณที่เร็วมาก ทำให้ทุกอุตสาหกรรมส่วนใหญ่ได้รับประโยชน์ รวมถึงวงการแพทย์ด้วย ซึ่งด้วยเทคโนโลยีอย่าง Machine Learning อาจจะเป็นส่วนช่วยในการคำนวณเพื่อหาสูตรยาชนิดใหม่ที่นำมาใช้รักษาโรคที่ยังไม่มีทางรักษาในปัจจุบัน หรือมีอยู่แล้ว แต่ช่วยลดต้นทุนลงได้

* ระบบความปลอดภัยที่ซับซ้อนจนแทบไม่สามารถเจาะได้

นอกจากคอมพิวเตอร์ควอนตัมจะมีประสิทธิภาพในการคำนวณที่รวดเร็วมากแล้ว ยังมีประโยชน์ต่อระบบความปลอดภัยอย่างมากด้วย เพราะการแฮกระบบคอมพิวเตอร์ควอนตัมนั้นแทบจะเป็นไปไม่ได้เลย ด้วยระบบ Quantum Key และระบบ Quantum Safe Alrorithm ซึ่งจริง ๆ ในปัจจุบันมีบริการที่เริ่มใช้การเข้ารหัสด้วยระบบ QSC \(Quantum- Safe Cryptography\) อย่าง ETSI

* สามารถแก้ปัญหาทางวิทยาศาตร์ที่มีข้อถกเถียงกันมานานในปัจจุบัน

ในเมื่อคอมพิวเตอร์ควอนตัมสามารถคำนวณได้อย่างรวดเร็ว ปริศนาทางวิทยาศาสตร์หลาย ๆ อย่างที่ยังไม่ได้แก้ปริศนา อาจจะถูกแก้ไขได้รวดเร็วขึ้น ทำให้ข้อถกเถียงในปัจจุบันเกี่ยวกับปัญหา และปริศนาเหล่านั้นหายไป

### สรุปแล้ว Google สามารถพัฒนา Quantum Computer ไปถึงจุด “Quantum Supremacy” ได้แล้วจริงหรือ ?

![](https://www.beartai.com/wp-content/uploads/2019/10/images-3.jpeg)

ทาง IBM ได้ออกมาแย้งว่า Google อาจจะยังไม่ได้พัฒนาไปถึงขั้นนั้น หรือพูดง่าย ๆ ว่า Google อาจจะโม้ว่าทำได้แล้ว โดย IBM ได้ออกมาโชว์จำลองการคำนวณโปรแกรมอัลกอริทึมที่ชื่อ Schrödinger-Feynman ซึ่งเป็นตัวเดียวกับที่ Google เคลมว่าหากเป็นคอมพิวเตอร์ปกติ จะต้องใช้เวลาถึง 10,000 ปีในการคำนวณ แต่ด้วยโมเดลของ IBM ที่จำลองขึ้นมาด้วยซูเปอร์คอมพิวเตอร์ธรรมดานั้น ใช้ประโยชน์จากพื้นที่เก็บข้อมูลขนาดใหญ่ สามารถคำนวณอัลกอริทึมนี้ได้ภายในเวลาเพียง 2 วันกว่า และไม่ได้ใช้เวลานานถึง 10,000 ปีตามที่ Google อ้าง

\(จริง ๆ ถ้าไม่ได้ใช้โมเดลนั้น ก็น่าจะใช้เวลาถึง 10,000 ปีแหละ แต่ Google ไม่ได้คำนึงถึงตรงนั้น\)

แต่ถึงอย่างไรก็ตาม เทคโนโลยีคอมพิวเตอร์ควอนตัมยังต้องใช้เวลาอีกหลายปี กว่าจะถูกพัฒนาจนอยู่ในรูปแบบที่ผู้ใช้งานทั่วไปเข้าถึงได้ โดยกลุ่มแรกที่จะได้เข้าถึงก่อนคือพวกอุตสาหกรรมทั้งหลาย ที่มีกำลังพอจะซื้อเทคโนโลยีเหล่านี้มาใช้งาน เพราะการมาของเทคโนโลยีใหม่ในช่วงแรกจะต้องใช้เงินที่สูงมากในการที่จะได้เข้าถึงมันก่อน

**อ้างอิง** : [Google AI Quantum,](https://ai.google/research/teams/applied-science/quantum/) [Google Youtube Channel](https://www.youtube.com/watch?v=-ZNEzzDcllU), [IBM](https://www.ibm.com/blogs/research/2019/10/on-quantum-supremacy/) 
