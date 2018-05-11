> BeanUtils位于org.apache.commons.beanutils.BeanUtils下面

-----
## 1、bean 转换成 map
```java
 Person person1=new Person();  
        person1.setName("name1");  
        person1.setSex("sex1");  
        Map<String, String> map=null;  
            map = BeanUtils.describe(person1);  
```

## 2、map 转换成 bean
```java
     public static <T> T map2Bean(Map<String, String> map, Class<T> class1) {  
        T bean = null;  
        try {  
            bean = class1.newInstance();  
            BeanUtils.populate(bean, map);  
        } catch (InstantiationException e) {  
            e.printStackTrace();  
        } catch (IllegalAccessException e) {  
            e.printStackTrace();  
        } catch (InvocationTargetException e) {  
            e.printStackTrace();  
        }  
        return bean;  
    }  
        
```


## 3、 2bean转为固定map
```java
    BeanUtils.populate( Object bean, Map properties );
```
