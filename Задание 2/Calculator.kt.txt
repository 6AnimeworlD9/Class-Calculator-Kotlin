class Calculator {
    public var i=0
    public val digits: Array<Double> = arrayOf(0.0,0.0)
    public var itog=0.0
    public var znak:String=""

    fun addDigit(digit: Double)
    {
      if(i==0){digits[0]=digit;i++}
      else {digits[1]=digit;i=0}
    }
    fun calc()
    {
        if(znak=="+")
            itog=digits[0]+digits[1]
        else if(znak=="-")
            itog=digits[0]-digits[1]
        else if(znak==":")
            itog=digits[0]/digits[1]
        else if(znak=="*")
            itog=digits[0]*digits[1]
        digits[0]=itog
    }
    fun clearAll()
    {
        digits[0]=0.0
        digits[1]=0.0
        i=0
    }
}