# sunwoo
<!DOCTYPE html>
<html>
<head>
    <title>book 객체 만들기</title>
</head>
<body>
<h3>book 객체 배열 만들기</h3>
<hr>
<script>
var bookArray = new Array();
for(i=0 ; i<5; i++)
{
    var input = prompt("콤마(,)로 분리하면서 첵제목 저자 가격순으로 입력");
    var ar = input.split(",");
    var book = new Object();
    book.title = ar[0];
    book.author = ar[1];
    book.price = ar[2];
    bookArray[i] = book;
}
// bookArray 객체 출력
for(i=0 ; i<bookArray.length ; i++)
{
    document.write(bookArray[i].title + ",");
    document.write(bookArray[i].author + ",");
    document.write(bookArray[i].price + "<br>");
}
// 가장 가격이 비싼 책은?
    var most = bookArray[0];
    for(i=0 ; i<bookArray.length ; i++) 
    { 
        if(bookArray[i].price > most.price)
        most = bookArray[i];
    }    
 
        document.write("<br> 가장 가격이 비싼 책은 " + most.title);
</script>
</body>
</html>
