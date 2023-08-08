```
> jshell
|  JShellへようこそ -- バージョン20.0.2
|  概要については、次を入力してください: /help intro

jshell> "test"
$1 ==> "test"

jshell> "test
|  エラー:
|  文字列リテラルが閉じられていません      
|  "test
|  ^
|  エラー:
|  構文解析中にファイルの終わりに移りました
|  "test
|       ^

jshell> "test" + "er"
$2 ==> "tester"

jshell> "test" + 123
$3 ==> "test123"

jshell> "test" + 12 - 3
|  エラー:
|  二項演算子'-'のオペランド型が不正です
|    最初の型: java.lang.String
|    2番目の型: int
|  "test" + 12 - 3
|  ^-------------^

jshell> "test" + 12 + 3
$4 ==> "test123"

jshell> 12 + 3 + "test"
$5 ==> "15test"

jshell> "文字列に\"を含む"
$6 ==> "文字列に\"を含む"

jshell> System.out.println($6)
文字列に"を含む

jshell> "改行\nする"
$8 ==> "改行\nする"

jshell> System.out.plintln($8)
|  エラー:
|  シンボルを見つけられません
|    シンボル:   メソッド plintln(java.lang.String)
|    場所: タイプjava.io.PrintStreamの変数 out
|  System.out.plintln($8)
|  ^----------------^

jshell> System.out.println($8)
改行
する

jshell> """
...> test
...> foo
...> """
$10 ==> "test\nfoo\n"

jshell> 3 / 0
|  例外java.lang.ArithmeticException: / by zero
|        at (#11:1)

jshell> 0 / 3
$12 ==> 0

jshell> 3.0 / 0
$13 ==> Infinity

jshell> "test".toUpperCase()
$14 ==> "TEST"

jshell> "test".to
toCharArray()   toLowerCase(    toString()      toUpperCase(    
jshell> "test".toUpperCase()
$15 ==> "TEST"

jshell> "test".length(
...> )
$16 ==> 4

jshell> "test".rep
repeat(         replace(        replaceAll(     replaceFirst(   
jshell> "test".repeat(5)
$17 ==> "testtesttesttesttest"

jshell> "test".rep
repeat(         replace(        replaceAll(     replaceFirst(   
jshell> "test".repla
replace(        replaceAll(     replaceFirst(   
jshell> "test".replace("es", "")
$18 ==> "tt"

jshell> 'test'.replace('es', "")
|  エラー:
|  文字リテラルが閉じられていません
|  'test'.replace('es', "")
|  ^
|  エラー:
|  文字リテラルが閉じられていません
|  'test'.replace('es', "")
|       ^
|  エラー:
|  文字リテラルが閉じられていません
|  'test'.replace('es', "")
|                 ^

jshell> 'test'.replace('es', '')
|  エラー:
|  文字リテラルが閉じられていません
|  'test'.replace('es', '')
|  ^
|  エラー:
|  文字リテラルが閉じられていません
|  'test'.replace('es', '')
|       ^
|  エラー:
|  文字リテラルが閉じられていません
|  'test'.replace('es', '')
|                 ^

jshell> "test".replace("es","")
$19 ==> "tt"

jshell> "test".replace("es","alen")
$20 ==> "talent"

jshell> "test".replace(
$1    $10   $14   $15   $17   $18   $19   $2    $20   $3    $4    $5    $6    $8

シグネチャ:
String String.replace(char oldChar, char newChar)
String String.replace(CharSequence target, CharSequence replacement)

<ドキュメントを表示するにはタブを再度押してください>
jshell> "test".replace(
String String.replace(char oldChar, char newChar)
Returns a string resulting from replacing all occurrences of oldChar in this string with
newChar .
If the character oldChar does not occur in the character sequence represented by this String
object, then a reference to this String object is returned. Otherwise, a String object is
returned that represents a character sequence identical to the character sequence represented
by this String object, except that every occurrence of oldChar is replaced by an occurrence of
newChar .
Examples:
"mesquite in your cellar".replace('e', 'o')
returns "mosquito in your collar"
"the war of baronets".replace('r', 'y')
returns "the way of bayonets"
"sparring with a purple porpoise".replace('p', 't')
returns "starring with a turtle tortoise"
"JonL".replace('q', 'x') returns "JonL" (no change)


Parameters:
oldChar - the old character.

<次のページを表示するにはタブを再度押してください>
jshell> "test".
charAt(                chars()                codePointAt(           codePointBefore(       codePointCount(        codePoints()           compareTo(             compareToIgnoreCase(   concat(                
contains(              contentEquals(         describeConstable()    endsWith(              equals(                equalsIgnoreCase(      formatted(             getBytes(              getChars(              
getClass()             hashCode()             indent(                indexOf(               intern()               isBlank()              isEmpty()              lastIndexOf(           length()
lines()                matches(               notify()               notifyAll()            offsetByCodePoints(    regionMatches(         repeat(                replace(               replaceAll(            
replaceFirst(          resolveConstantDesc(   split(                 startsWith(            strip()                stripIndent()          stripLeading()         stripTrailing()        subSequence(
substring(             toCharArray()          toLowerCase(           toString()             toUpperCase(           transform(             translateEscapes()     trim()                 wait(                  
jshell> "test".substring(
$11   $12   $16

シグネチャ:
String String.substring(int beginIndex)
String String.substring(int beginIndex, int endIndex)

<ドキュメントを表示するにはタブを再度押してください>
jshell> "test".substring(1,2)
$21 ==> "e"

jshell> "test".substring(1,3)
$22 ==> "es"

jshell> "消費税抜き%,d円は消費税込みで%,d円".formatted(1000, 1000)
$23 ==> "消費税抜き1,000円は消費税込みで1,000円"

jshell> "消費税抜き%,d円は消費税込みで%,d円".formatted(1000, 1000 * 1.1)
|  例外java.util.IllegalFormatConversionException: d != java.lang.Double
|        at Formatter$FormatSpecifier.failConversion (Formatter.java:4510)
|        at Formatter$FormatSpecifier.printInteger (Formatter.java:3055)
|        at Formatter$FormatSpecifier.print (Formatter.java:3010)
|        at Formatter.format (Formatter.java:2781)
|        at Formatter.format (Formatter.java:2717)
|        at String.formatted (String.java:4217)
|        at (#24:1)

jshell> "消費税抜き%,d円は消費税込みで%,d円".formatted(1000, (1000 * 1.1))
|  例外java.util.IllegalFormatConversionException: d != java.lang.Double
|        at Formatter$FormatSpecifier.failConversion (Formatter.java:4510)
|        at Formatter$FormatSpecifier.printInteger (Formatter.java:3055)
|        at Formatter$FormatSpecifier.print (Formatter.java:3010)
|        at Formatter.format (Formatter.java:2781)
|        at Formatter.format (Formatter.java:2717)
|        at String.formatted (String.java:4217)
|        at (#25:1)

jshell> var t = "test"
t ==> "test"

jshell> t
t ==> "test"

jshell> var n = 5
n ==> 5

jshell> n + 10
$29 ==> 15

jshell> n += 20
$30 ==> 25

jshell> n *= 20
$31 ==> 500

jshell> var r10 = 11.75
r10 ==> 11.75

jshell> r10 * r10 * Math.
E                       IEEEremainder(          PI                      TAU                     abs(                    absExact(               acos(                   addExact(               asin(                   
atan(                   atan2(                  cbrt(                   ceil(                   ceilDiv(                ceilDivExact(           ceilMod(                class                   copySign(               
cos(                    cosh(                   decrementExact(         divideExact(            exp(                    expm1(                  floor(                  floorDiv(               floorDivExact(
floorMod(               fma(                    getExponent(            hypot(                  incrementExact(         log(                    log10(                  log1p(                  max(                    
min(                    multiplyExact(          multiplyFull(           multiplyHigh(           negateExact(            nextAfter(              nextDown(               nextUp(                 pow(
random()                rint(                   round(                  scalb(                  signum(                 sin(                    sinh(                   sqrt(                   subtractExact(          
tan(                    tanh(                   toDegrees(              toIntExact(             toRadians(              ulp(                    unsignedMultiplyHigh(
jshell> r10 * r10 * Math.pow(
$11   $12   $13   $16   $29   $30   $31   n     r10

シグネチャ:
double Math.pow(double a, double b)

<ドキュメントを表示するにはタブを再度押してください>
jshell> r10 * r10 * Math.pow(3.5)
|  エラー:
|  クラス java.lang.Mathのメソッド powは指定された型に適用できません。
|    期待値: double,double
|    検出値:    double
|    理由: 実引数リストと仮引数リストの長さが異なります
|  r10 * r10 * Math.pow(3.5)
|              ^------^

jshell> r10 * r10 * Math.pow(3.0)
|  エラー:
|  クラス java.lang.Mathのメソッド powは指定された型に適用できません。
|    期待値: double,double
|    検出値:    double
|    理由: 実引数リストと仮引数リストの長さが異なります
|  r10 * r10 * Math.pow(3.0)
|              ^------^

jshell> r10 * r10 * Math.PI
$33 ==> 433.73613573624084

jshell> var i = "real"
i ==> "real"

jshell> /v real
|  指定されたスニペットは存在しません: real

jshell> /v i
|    String i = "real"

jshell> String u = "your name"
u ==> "your name"

jshell> /v u
|    String u = "your name"

jshell> int j
j ==> 0

jshell> /v j
|    int j = 0

jshell> Int c = 5
|  エラー:
|  シンボルを見つけられません
|    シンボル:   クラス Int
|    場所: クラス
|  Int c = 5;
|  ^-^

jshell> int c = 5
c ==> 5

jshell> /v c
|    int c = 5

jshell> char ch = 93
ch ==> ']'

jshell> char ch = 91
ch ==> '['

jshell> char ch = 95
ch ==> '_'

jshell> char ch = 95
ch ==> '_'

jshell> int i = 2234
i ==> 2234

jshell> double d = i
d ==> 2234.0

jshell> int j = (int)d
j ==> 2234

jshell> import java.time
|  エラー:
|  シンボルを見つけられません
|    シンボル:   クラス time
|    場所: パッケージ java
|  import java.time;
|         ^-------^

jshell> import java.time.*

jshell> Lo
LocalDate               LocalDateTime           LocalTime               Locale                  Long                    LongBinaryOperator      LongConsumer            LongFunction            LongPredicate           
LongStream              LongSummaryStatistics   LongSupplier            LongToDoubleFunction    LongToIntFunction       LongUnaryOperator
jshell> Local
LocalDate       LocalDateTime   LocalTime       Locale          
jshell> LocalDa
LocalDate       LocalDateTime   
jshell> LocalDateTime.
MAX              MIN              class            from(            now(             of(              ofEpochSecond(   ofInstant(       parse(           
jshell> LocalDateTime.now()
$46 ==> 2023-08-07T23:14:46.792140700

jshell> LocalTime.now()
$47 ==> 23:14:53.313002900

jshell> BigDecimal.valueOf(597).multiply(Big
BigDecimal   BigInteger   
jshell> BigDecimal.valueOf(597).multiply(BigDecimal.valueOf(0.05))
$48 ==> 29.85

jshell>
```