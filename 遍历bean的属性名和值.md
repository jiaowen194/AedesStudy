```java
public static void testReflect(Object model) throws Exception{
  for (Field field : model.getClass().getDeclaredFields()) {
    field.setAccessible(true);
    System.out.println(field.getName() + ":" + field.get(model) );
  }
}

```
