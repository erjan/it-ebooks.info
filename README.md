# it-ebooks.info
it-ebooks.info android app - search and download best new software, IT ebooks

Bugs I had fixed:

long book_id = book_id = jsonBook.getInt(BOOK_ID); //  because I used getInt, i had negative book ids 

1 public void execute(){
          //super.execute();   this downloaded list of books twice and added them twice 
          ProcessData processData = new ProcessData() ;
          processData.execute() ;
      }

2 <style name="Theme.Base" parent="AppTheme"><item name="colorPrimary"> @color/flickrPrimaryBackgroundColor</item><item name="colorPrimaryDark"> @color/flickrSecondaryBackgroundColor</item>




3 if you have space after >@color - the color will not be displyaed, this is a error!




4 android {compileSdkVersion 21
  buildToolsVersion "21.1.2" or "21.1.1" - this was causing build gradle errors



5 I created new java class recycler item click listener OUTSIDE OF package! so it did not recognize it, if i left the file outside , i would need to access it with package_name.recyclerListener!


6 stupid error by me: i learned this bug:

String method1(){
.....
return " " ;
}
String method2(){
intermediate_string = method1();
.....
}

public void boss_method(){
    string s1 = method1();
    string result = method2(s1);
    //basically I just returned " " empty string instead of actual result i computed

}

7 if you try to do http url connection outside of doIn background() it throws network on main thread exception

i tried to do this in separate method isDataAvailable() inside ProcessData class. Now i see that this was duplicate code - i essentially do same work twice that I do in doinbackground()!
so - the point is to move this code into doinbackg-d() and introduce another state variable isdataAvailable -not the whole method!


8. another thing learned: 
boolean inner_x ;
public data( boolean inner_x){
inner_x = true ;//this does not work because: i assign the argument again to true , not the actual inner x to true!
}

must use this keyword:
public data(boolean inner_x){
this.inner_x = inner_x ;
} tip: focus on a variable and IDE will highlight where it is used - i see that it is not used at all! 
