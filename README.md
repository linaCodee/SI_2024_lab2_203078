#SI_2024_lab2_203078
Лина Цакончева 203078

2. Изработка на control flow graph на word документ

3. Цикломатска комплексност изнесува 10 која ја добив преку формулата Р+1 каде Р е бројот на предикатни јазли односно 7 за if услови и 2 за for циклуси па 9+1=10

4. if (allItems == null)
Во случај кога allItems=null и вредност за payment е поголема од 0 тогаш се фрла exception односно RuntimeException("allItems list can't be null!") 

if (item.getName() == null || item.getName().length() == 0) во случај кога вредноста на името е null или пак должината на името е 0, а сите други вредности се пополнети и вредноста на payment ако е поголема од 0, тогаш задачата ќе продолжи да се извршува бидејќи името ќе се сетира на unknown

if (item.getBarcode() != null) доколку вредноста на баркодот изнесува null и сите други вредности се пополнети правилно, на пример getName="Item", getBarcode="2r13f", getPrice=100, getDiscount=0.20, тогаш ќе се фрли exception односно RuntimeException("No barcode!") 

if (allowed.indexOf(c) == -1) доколку внесениот бар-код содржи невалидни карактери тогаш ќе се фрли exception т.е. RuntimeException("Invalid character in item barcode!")

if (item.getDiscount() > 0) доколку вредноста на попустот е поголема од 0 и на пример изнесува 0.2 во таков случај ако цената на предметот изнесува 100ка тогаш сумата сега ќе биде еднаква на 20

if (item.getDiscount() > 0) доколку вредноста на попустот не е поголема од 0 тогаш вредноста на производот ако изнесувала 0 тогаш главната сума ќе си остане 100

if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0') со влезни параметри за getName="Item1", getBarcode="03m23", getPrice=400, getDiscount=0.10 тогаш сумата ќе биде 40 по одземените 30

if (sum <= payment) доколку влезниот параметар за payment е поголем од сумата тогаш резултатот ќе биде true. За getPrice=100 a вредноста на getDiscount=10, при што payment=50, во овој случај sum=10 и со тоа овој услов ќе враќа true. Доколку payment изнесува пак 9 во тој случај овој услов ќе враќа false

5. if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0')
за вредности getName="Item1", getBarcode="01234", getPrice=310, getDiscount=0.10 условот е точен при што истиот се извршува и сумата се намалува за 30

if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) != '0')
за вредности getName="Item1", getBarcode="01234", getPrice=310, getDiscount=0.10 уловот е точен и вредноста треба да се намали за 30

if (item.getPrice() > 300 && item.getDiscount() <= 0 && item.getBarcode().charAt(0) != '0')
за вредности getName="Item1", getBarcode="0234", getPrice=310, getDiscount=-1.10 условот е невистинит и сумата не се намалува

if (item.getPrice() <= 300 && item.getDiscount() <= 0 && item.getBarcode().charAt(0) != '0')
за вредности getName="Item1", getBarcode="234", getPrice=300, getDiscount=-1.10 условот е точен и сумата ќе за намали за 30

if (item.getPrice() <= 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) != '0')
за вредности getName="Item1", getBarcode="234", getPrice=300, getDiscount=-1.10 условот не е точен и сумата нема да се намали

if (item.getPrice() <= 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0')
за вредности getName="Item1", getBarcode="0234", getPrice=300, getDiscount=0.10 условот е точен и сумата ќе се намали

if (item.getPrice() <= 300 && item.getDiscount() <= 0 && item.getBarcode().charAt(0) == '0')
за вредности getName="Item1", getBarcode="234", getPrice=300, getDiscount=-0.10 условот не е точен и сумата нема да се намали

if (item.getPrice() > 300 && item.getDiscount() <= 0 && item.getBarcode().charAt(0) == '0')
за вредности getName="Item1", getBarcode="0234", getPrice=350, getDiscount=-0.10 условот е точен и сумата ќе се намали