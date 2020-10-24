## Refactoring Examples


## FlashGet

From Purich's FlashGet code: https://github.com/jeanyjean/PA4-FlashGet

### initComponents() method

In the `src/FlashGetPackage/FlashGet.java` class 

https://github.com/jeanyjean/PA4-FlashGet/blob/master/src/FlashGetPackage/FlashGet.java

* Refactoring: rename method.

I have rename each initComponents method to be easier to understand and looks better by naming it first, second, and third

```java
    private FlowPane initFirstComponents(){
    private FlowPane initSecondComponents(){
    private FlowPane initThirdComponents(){
```
    
### createProgressBar() method

* Refactoring: Extract method.

I created a method named createProgressBar() that will create progress bar and set progress to 0.0.

```java
    private ProgressBar createProgressBar(){
    ProgressBar newProgressBar = new ProgressBar();
    newProgressBar.setProgress(0.0);

    return newProgressBar;
    }
```
Use the method instead of creating and setting each progressbar individually.

```java
    progressBar2 = createProgressBar();
    progressBar3 = createProgressBar();
    progressBar4 = createProgressBar();
    progressBar5 = createProgressBar();
    progressBar6 = createProgressBar();
```
### DownloadHandler Class's handle method

* Refactoring: Extract method.

The method seems to be doing too many tasks so I extracted a part of the code to another method called downloadFiles.

```java
    private void downloadFiles(File selectedFile, ChangeListener<Long> valueListener) {
```

```java
    class DownloadHandler implements EventHandler<ActionEvent> {
        @Override
        public void handle(ActionEvent actionEvent) {
        .
        .
        .
        downloadFiles(selectedFile, valueListener);
```

