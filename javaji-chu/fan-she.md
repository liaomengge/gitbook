一、如何针对包下方法进行特殊处理

1. AOP处理
2. 扫描包指定的注解

```
public class AnnotationScanUtil {

    public static void scanPackage(String packageName, Class<? extends Annotation> clazz) {
        Reflections reflections = new Reflections(packageName);
        Set<Class<?>> classesList = reflections.getTypesAnnotatedWith(clazz);

        //...
    }
}
```



