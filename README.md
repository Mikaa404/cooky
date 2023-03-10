## Maven Dependency

```xml

<dependency>
    <groupId>com.mikaa404</groupId>
    <artifactId>cooky</artifactId>
    <version>[1.0,)</version>
</dependency>
```

## Example Usage

```java
import com.mikaa404.browser.ChromeBrowser;
import com.mikaa404.cookie.ICookie;

import java.util.List;

class Main {
    public static void main(String[] args) {
        List<ICookie> cookieList = ChromeBrowser.getInstance().getAllCookies();
        // This will get cookies stored in first profile. If you have multiple profile configured, you can specify your profile name.
        List<ICookie> cookieListByProfile = ChromeBrowser.getInstance().getAllCookies("Profile 1");
        
        
        // do something with cookies
        for (ICookie c : cookieList) {
            System.out.printf("%s - %s - %s - %s\n", c.getHostKey(), c.getPath(), c.getName(), c.getValue());
        }
    }
}
```

## Executable Usage

1. Download jar from release. (e.g. `cooky-1.1.1.jar`)

2. Make sure java 1.8+ is installed.

3. Run

```shell
java -jar cooky-1.1.1.jar
```

## Note

Only supports Chrome on macOS and Windows currently. 
