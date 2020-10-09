fun main(){
    val a:Calculator=Calculator()
    var i=0
    var signal=""
    var array = emptyArray<Double>()
    print("Введите цифру: ") ;array+= readLine()?.toDouble()?:0.0;a.addDigit(array[0]);i++
    while(signal!="3"){
    print("Введите знак: ");a.znak=readLine().toString();
    print("Введите цифру: ");array+= readLine()?.toDouble()?:0.0;a.addDigit(array[i]);i++
    a.calc()
    println("Результат: "+a.itog)
    print("Продолжить - 1, Очистить все - 2 , Стоп - 3: ");signal = readLine().toString();
    if(signal=="2"){a.clearAll();print("Введите цифру: ") ;array+= readLine()?.toDouble()?:0.0;a.addDigit(array[i]);i++;}
    else if(signal=="1")a.i=1
    }
}