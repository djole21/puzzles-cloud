# This is heading 
``` java
    private String createTitleFromFileName(String title) {
        String newTitle = title.substring(0, title.lastIndexOf("."));
        newTitle = newTitle.replaceAll("_", "");
        return StringUtils.capitalize(newTitle);
    }
```


private String createTitleFromFileName(String title) {
    String newTitle = title.substring(0, title.lastIndexOf("."));
    newTitle = newTitle.replaceAll("_", "");
    return StringUtils.capitalize(newTitle);
