****

#### Description 

* "clients should **not** be forced to depend on methods they **do not** use."

* In other words, a class **should not** be forced to implement methods that it does **not** need or use, simply because those methods are defined in an interface that it implements.

*Example 

1. Instead having one interface having defined methods like this 

```java 

public interface Machine {
    void print(Document document);
    void scan(Document document);
    void copy(Document document);
}
```

2. We should break down `Machine` into smaller, more specialized interfaces: 

```java

public interface Printer {
    void print(Document document);
}

public interface Scanner {
    void scan(Document document);
}

public interface Copier {
    void copy(Document document);
}
```

3. `Printer` can implement the `PrinterImpl` interface, while `ScannerCopier`can implement both `Scanner` and `Copier` interfaces

```java

public class PrinterImpl implements Printer {
    @Override
    public void print(Document document) {
        // print document
    }
}

public class ScannerCopierImpl implements Scanner, Copier {
    @Override
    public void scan(Document document) {
        // scan document
    }

    @Override
    public void copy(Document document) {
        // copy document
    }
}
```

