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
