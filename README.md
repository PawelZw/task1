# task1


🔥 An simple application that downloads table Statistics Electricity Imbalance from
https://www.ote-cr.cz/en/statistics/electricity-imbalances and store it as a HTML file..


💡 Technologies
  Java



![task 12](https://user-images.githubusercontent.com/108124357/204152624-9d627f05-9466-4eeb-8237-9ebce0931f7d.jpg)


 

# Application downloads only table Statistic Electricyty Imbalance: 



# Code describing the program:
 
```

package task1;

import org.jsoup.Jsoup;
import org.jsoup.nodes.Document;
import org.jsoup.select.Elements;

import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;

public class Task1 {
    public static void main(String[] args) throws IOException {
        Document doc = Jsoup.connect("https://www.ote-cr.cz/en/statistics/electricity-imbalances?version=0&date=2022-09-22").get();
        log(doc.title());

        Elements newsHeadlines = doc.select("table");
        System.out.println(newsHeadlines.get(0));
        Files.writeString(Path.of("table.HTML"),newsHeadlines.get(0).toString());

    }
    private static void log(String msg, String... vals) {
        System.out.println(String.format(msg, vals));
    }
}


```
 

🙋‍♂️ Feel free to contact me
Write sth nice ;) Find me on pawelzwolicki@gmail.com

 
👏 Thanks 
