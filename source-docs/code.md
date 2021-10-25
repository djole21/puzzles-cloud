# This is heading 
``` java
    private String createTitleFromFileName(String title) {
        String newTitle = title.substring(0, title.lastIndexOf("."));
        newTitle = newTitle.replaceAll("_", "");
        System.out.println(newTitle);
        return StringUtils.capitalize(newTitle);
    }
```
