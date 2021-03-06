Вопросы на собеседование iOS-разработчика
==

Вопросов: 176 | Ответов: 40
--------

Objective-C, Foundation:
------------------------
- Что такое `свойство (property)`? [[-]](https://gist.github.com/arthurigberdin/d9105edc388f25ebe1ae)
- Что такое `назначенный инициализатор (designated initializer)`? Приведите пример назначенного инициализатора (имеется ввиду `if (self  = [super ...])`)? [[-]](https://gist.github.com/arthurigberdin/ec6f06ba14ba9d175252)
- Суть `рантайма (Runtime), отправление сообщения`? Как работает Runtime? [[-]](https://gist.github.com/arthurigberdin/811ab333c46b4fa2a46f)
- Как добавить свойство в существующий объект с закрытой реализацией? Можно ли это сделать через runtime? [[-]](https://gist.github.com/arthurigberdin/6df58c356bfca9655ffa)
- Объявление `свойств (property): retain, assign, nonatomic, readonly, copy`?  [[-]](https://gist.github.com/arthurigberdin/a995a091d3df97d8adac)
- С подвохом: вопрос о несуществующем параметре `atomic`, что он означает? Приведите пример кейса с использованием `atomic`? [[+]](https://gist.github.com/arthurigberdin/b33d31ec5f994b228a0e)
- Как правильно реализовать сетер для свойства с параметром retain?
- Вопрос о циклах в графах владения, и почему свойства delegate (предоставляющие доступ к делегату) обычно задаются как `assign` или `weak`?
- Можно ли чтобы разные классы реализовывали один протокол. (ClassA, ClassB и ClassC - реализуют ClassCProtocol)?
- Для чего нужен @dynamic, приведите примеры использования?
- Для чего нужен @synthesize, приведите примеры использования?
- В чем разница между `точечной нотацией` и использованием квадратных скобок? [[-]](https://gist.github.com/arthurigberdin/45af3eefeb936133c8c5)
- Что происходит когода мы пытаемся вызвать метод у nil указателя? Разница между nil и Nil и [NSNull null]?
- Что такое `селектор (selector)`? Как его вызвать? как отложить вызов селектора? Что делать если селектор имеет много параметров? `(NSInvocation)` Как запустить селектор в `(фоновом) потоке`? [[-]](https://gist.github.com/arthurigberdin/8a3a264810ee97927d19)
- Как запустить `поток`? Что первым нужно сделать при запуске `потока`?
- `(NSAutoreleasePool)` Что такое `runLoop`, кодга он используется? `(timers, nsurlconnection ...)`?
- Что такое `делегат (delegate)`? как его создать и использовать? [[+]](https://gist.github.com/arthurigberdin/1304fb056c85f3fd8535)
- В чем отличия коммуникационных паттернов? (`Notification` vs `Delegates` vs `Observing`)? [[-]](https://gist.github.com/arthurigberdin/3b1e2a1598efa76a5655)
- Что такое `AppDelegate`? Зачем он нужен? [[+]](https://gist.github.com/arthurigberdin/780eafb581fb2f72dec3)
- Управление `колбэками (callbacks)`: `Selectors` vs `Delegate prototocls` vs `Blocks`?
- Как `использовать` self внутри блоков? Приведите пример `retain cycle` в блоке? [[-]](https://gist.github.com/arthurigberdin/67a2e19c09f3c26eb926)
- Как представлены `Си-структуры` (CGRect, CGSize, CGPoint) в Objective-C?
- Какие существуют `root классы` в iOS? Для чего нужны `root классы`? [[+]](https://gist.github.com/arthurigberdin/83032db4d6d18f9bf399)
- Как работает `proxy`?
- Как имитировать `множественное наследование`? [[+]](https://gist.github.com/arthurigberdin/de9765cf851e47379cf2)
- Что такое `тип id`. Что случится во время компиляции если мы посылаем сообщение объекту `типа id`? Что случится во время выполнения если этот метод существует? [[+]](https://gist.github.com/arthurigberdin/f2d90d8f81638b281c35)
- Что такое `указатель isa`? Для чего он нужен? [[+]](https://gist.github.com/arthurigberdin/c12de01c73f9c90c2f9c)
- Цепочка ответсвенности, что происходит с методом после того как он не нашелся в объекте класса, которому его вызвали (в сторону forwardInvocation:)? [[+]](https://gist.github.com/arthurigberdin/f0a0378b305d48173cc7)
- Чем `категория` отличается от `категории продолжения класса` (extension, наименованная категория)? [[-]](https://gist.github.com/arthurigberdin/ec9ac3bfd013522fb7c3)
- Можно ли добавить `ivar` в категорию? [[+]](https://gist.github.com/arthurigberdin/26b85da45706a4a2aa34)
- Когда лучше использовать `категорию`, а когда `наследование`? [[+]](https://gist.github.com/arthurigberdin/5b09bcc3c6947ba25329)
- Что такое `notifications (уведомления)`? как мы должны их использовать?
- Какая разница между использованием `делегатов (delegation)` и `нотификейшенов (notification)`? [[-]](https://gist.github.com/arthurigberdin/ee09ee7d0ae237a3fdc3) [[+]](https://gist.github.com/arthurigberdin/3b1e2a1598efa76a5655)
- В чем разница между `NSArray и NSMutableArray`? непотоко-безопасный NSMutableArray? [[-]](https://gist.github.com/arthurigberdin/ed8aa7dfaea3b28ef467)
- Чем отличается `NSSet от NSArray`? Какие `операции` происходят быстро в `NSSet` и какие в `NSArray`? [[-]](https://gist.github.com/arthurigberdin/82557661c44d81e85bc1)
- `Формальный и неформальный (informal)` протокол? `Протоколы (protocols)`: основные отличия между c#/java интерфейсами и Objective-C протоколами? Что делать в случае если класс не реализует какой-то метод из протокола? [[-]](https://gist.github.com/arthurigberdin/da734c67aa6fad9f1d68)
- Есть ли `приватные и защищенные` методы в Objective-C? [[+]](https://gist.github.com/arthurigberdin/c09a5a930ec34d86d091)
- Что такое `быстрое перечисление (fast enumeration)`? 
- Что такое `KVO`? Когда его нужно использовать? Методы для обозревания объектов? Работает ли `KVO с instance переменными (полями)` объекта?
- Что такое `KVC`? Когда его нужно использовать?
- Как удалить объект в ходе итерации по циклу?
- Что такое `Run Loop`?
- Как лучше всего загрузить `UIImage c диска(с кеша)`?
- Какой контент лучше хранить в `Documents`, а какой в `Cache`?
- Как связаны `NSRunLoop и NSAutoreleasePool` на пальцах?
- Почему нам не следует вызывать `instance методы в методе initialize`?
- `NSCoding, archiving`?
- Протокол `NSCopying`, почему мы не можем просто использовать любой собственный объект в качестве ключа в словарях (NSDictionary) , что нужно сделать чтобы решить эту проблему? (разница между глубоким и поверхностным копированием)?
- `Антипаттерны` в Objective-C?

Memory Management:
------------------
- Как происходит `ручное управление памятью - MRC` в iOS?
- `autorelease vs release`?
- Что означает `ARC`?
- Что делать, если проект написан с использованием ARC, а нужно использовать классы сторонней библиотеки написанной без ARC?
- `Weak vs assign`, `strong vs copy`?
- `Atomic vs nonatomic`. Чем отличаются? Как вручную переопределить atomic/nonatomic сеттер в не ARC коде?
- Зачем все свойства ссылающиеся на делегаты `strong/retain`. :))) 
- Что такое `autorelease pool`?
- Как можно заимплементировать `autorelease pool на с++`?
- Если я вызову `performSelector:withObject:afterDelay:` - объекту пошлется сообщение retain?
- Как происходит обработка `memory warning`(предупреждение о малом  количестве памяти)? Зависит ли обработка от версии iOS, как мы должны их обрабатывать?
- Напишите простую реализацию `NSAutoreleasePoll` на Objective-C?
- Когда нужно использовать метод `retainCount` (никогда, почему?) Объясните что такое `подсчет ссылок (retain count)`?
- Темы управления памятью, такие как владение `retain/release/autorelease`?
- Что случится если вы добавите только что созданный объект в `Mutable Array`, и пошлете ему сообщение `release`? Что случится если послать сообщение `release` массиву? Что случится если вы удалите объект из массива и попытаетесь его использовать?
- С подвохом: как работает `сборщик мусора` в iOS? [[+]](https://gist.github.com/arthurigberdin/2f4c901b328e9f590ead)
- Нужно ли `ретейнить` (посылать сообщение retain) `делегаты`?
- Для чего используется класс `NSCoder`?
- Опишите правильный способ управления памятью выделяемой под `Outlet'ы`?
- Реализуйте следующие методы: `retain, release, autorelease`?

Networking:
----------
- Преимущества и недостатки `синхронного и асинхронного` соединения?
- Что означает `http, tcp`?
- Какие различия между `HEAD, GET, POST, PUT`? 
- Как загрузить что-то из интернета? В чем разница между `синхронными и асинхронными запросами`? Небольшое задание. Опишите как загрузить изображение из интернета и отобразить его в ImageView — все это должно происходить после нажатия кнопки.
- Что такое REST (Restful)?

Multithreading:
---------------
- Что такое `GCD`? Где используется `GCD`? Как `GCD` связан с многопоточностью? Типы queue? Queue == Thread? [[+]](https://gist.github.com/arthurigberdin/c812974bc5e058444f8d)
- `NSOperation` vs `GCD`?
- Что такое `deadlock`?
- Что такое `livelock`?
- Что такое `семафор (semafor)`?
- Что такое `мьютекс (mutex)`?
- `Асинхронность` vs `многопоточность`. Чем отличаются?
- Какие технологии в iOS возможно использовать для работы с потоками. Преимущества и недостатки.
- Как запустить поток? Что первым нужно сделать при запуске потока? (NSAutoreleasePool - пул автоосвобождения) Что такое runLoop, кодга он используется? (timers, nsurlconnection …)
- Чем отличается `dispatch_async от dispatch_sync`?
- Для чего при разработке под iOS использовать `POSIX-потоки`? `pthread_create(&thread, NULL, startTimer, (void *)t);`
- А чем реально `POSIX-потоки` лучше чем `GCD или NSOperationQueue вместе с NSOperation`? Приходилось ри реально использовать POSIX и как в этом были прюсы? Реально, просто интересно…
 `Use POSIX calls if cross-platform portability is required. If you are writing networking code that runs exclusively in OS X and iOS, you should generally avoid POSIX networking calls, because they are harder to work with than higher-level APIs. However, if you are writing networking code that must be shared with other platforms, you can use the POSIX networking APIs so that you can use the same code everywhere. `

UIKit:
------
- Разница между свойствами `bounds и frame` объекта UIView? Понимание системы координат?
- Какие бывают `состояния` у приложения?
- Цикл жизни `UIViewController`? [[+]](https://gist.github.com/arthurigberdin/c30ff516ce9eb2007418)
- Что такое `View` (представление) и что такое `window`?
- Какого разрешение экранов iphon'ов, и в чем разница между `points (точками)` и `пикселями (pixels)`?
- Что такое `responder chain` (цепочка обязанностей, `паттерн chain of responsibility`, на примере UI компонентов iOS ), `becomeFirstResponder`.
- Что означают `IBOutlet` и `IBAction`, для чего они нужны, и что значат для препроцессора?
- Как работает `UITableView`?
- Как многопоточность работает с `UIKit`?
- Что можно сделать если клавиатура при появлении скрывает важную часть интерфейса?
- Почему мы должны `релизить IBOutlet'ты` во viewDidUnload?
- Что такое `awakeFromNib`, в чем разница между `xib и nib` файлами?
- Иерархия наследования UIButton.

Базы данных, CoreData:
----------------------
- Составить SQL запрос на выборку всех проектов  на которых сидит девелопер с
id ==3. (`Developers:id,name; Projects:id,name; Developers&Projects:project_id,developer_id`)?
- Зачем нужно делать `двустороннии связи` в таблицах?

- Что такое `Core Data`?
- В каких случаях лучше использовать `SQLite`, а в каких `Core Data`?
- Что такое `контекст (Managed object context)`? Как происходят `изменения в NSManagedObjectContext`?
- Что такое `Persistent store coordinator`? Зачем нужен `NSPersistentStoreCoordinator`?
- Какие есть нюансы при использовании `Core Data в разных потоках`? Как `синхронизировать данные между потоками`(Как синхронизировать контекст)? Синхронизация разных типов NSManagedObjectContext (получение и изменение данных в child контекстах)? 
- Использовали ли `NSFetchedResultsController`? Почему? 
- Что такое `Fault` и зачем он нужен?
- Что таке `Fetched Property` и особенности работы с ним по сравнению с обычной связью?
- Как использовать `СoreData` совместно с `многопоточностью`?
- Что такое `NSManagedObjectId`? Можем ли мы сохранить его на потом если приложение закроется?
- Какие `типы хранилищ` поддерживает CoreData?
- Что такое `ленивая загрузка (lazy loading)`? Что ее связывает с CoreData? Опишите ситуация когда она может быть полезной?
- Что такое `нормализация` данных?

CoreAnimation, CoreGraphics:
----------------------------
- Что такое `CALayer`? [[+]](https://gist.github.com/arthurigberdin/feae78faec51105d97d5)
- Чем отличается `UIView от CALayer`?
- Какие типы `CALayer` есть?
- Чем отличается `UIView based Animation от Core Animation`?
- Можно ли `отследить изменение alpha`, через KVO в CALayer?
- Тайминги в `CoreAnimation`?
- Что такое `backing store`?
- Чем отличаются `аффинные преобразования от трехмерных`?
- Нужно ли `ретейнить (посылать сообщение retain)` делегат для `CAAnimation`?

Паттерны:
--------

Структуры данных:
--------

Algorithms:
-----------
- Напишите код, который `разворачивает строку на С++`. (переставить символы в строке в обратном порядке)?
- Поменять местами a и b не используя промежуточную переменную?
- Написать функцию вычисления n-го числа последовательности фебоначи. (если решить через рекурсию, спросят чем опасно такое решение)?
- Решить задачку о массиве: дан массив из 1001 элемента в котором присутсвуют все числа от 1 до 1000 и одно повторяется дважды, узнать какое, если к каждому элементу можно обратиться только 1 раз?
- Как из строки вытащить подстроку?

Logical:
--------
- Есть 4 человека, каждый проходит мост за 1, 2, 5, и 10 минут соответственно. Через мост они могут переходить только парами, держась за руку и только с фонариком. Притом один должен вернуться обратно и передать фонарик. Необходимо переправить всех за 17 мин на другую сторону. Задача решаема.


Code Puzzels:
-------------

- Что произойдет здесь (компиляция  + время выполнения): 

```objc
NSString *s = [NSNumber numberWithInt:3]; 
int i = [s intValue];
```

- Что не так с этим кодом? Зачем нужны `инициализаторы`?

```objc
[[[SomeClass alloc] init] init];
```

- Сработает ли `таймер`? Почему? 

```objc
void startTimer(void *threadId) 
{
   [NSTimer  scheduleTimerWithTimeInterval:10.0f 
      target:aTarget 
          selector:@selector(tick: ) 
          userInfo:nil
           repeats:NO];
}

pthread_create(&thread, NULL, startTimer, (void *)t);
```

- Какой метод вызовется: класса A или класса B? Как надо изменить код, чтобы вызвался метод класса A?

```objc
@interface A : NSObject
- (void)someMethod;
@end

@implementation A
- (void)someMethod
{
    NSLog(@"This is class A");
}
@end

@interface B : A
@end

@implementation B
- (void)someMethod 
{
    NSLog(@"This is class B");
}
@end

@interface C : NSObject
@end

@implementation C
- (void)method 
{
    A *a = [B new];
    [a someMethod];
}
```

- В каких случаях лучше использовать `strong`, а в каких `copy` для NSString? Почему?

```objc
@property (nonatomic, strong) NSString *someString;
@property (nonatomic, copy) NSString *anotherString;
```

- Что выведется в консоль? Почему?

```objc
- (BOOL)objectsCount
{
    NSMutableArray *array = [NSMutableArray new];
    for (NSInteger i = 0; i < 1024; i++) 
    {
        [array addObject:[NSNumber numberWithInt:i]];
    }
    return array.count;
}

- (void)someMethod 
{
    if ([self objectsCount]) 
    {
        NSLog(@"has objects");
    }
    else
    {
        NSLog(@"no objects");
    }
}
```

- Выведется ли в дебагер «Hello world»? Почему?

```objc
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
    dispatch_sync(dispatch_get_main_queue(), ^{
        NSLog(@"Hello world");
    });

   /* Another implementation */
   return YES;
}
```

- Что выведется в консоль?

```objc
 dispatch_async(dispatch_get_main_queue(), ^
    {
        NSLog(@"A %d", [object retainCount]);
        dispatch_async(dispatch_get_main_queue(), ^
        {
            NSLog(@"B %d", [object retainCount]);
        });
        NSLog(@"C %d", [object retainCount]);
    });
    NSLog(@"D %d", [object retainCount]);
```

- Что произойдет при исполнении следующего кода? 

```objc
Ball *ball = [[[[Ball alloc] init] autorelease] autorelease];
```
Additional:
-----------------------------
- Анкета в которой просят оценить свои знания по технологиям по 10 бальной шкале.

General:
--------
- Что такое `куча (heap)` и `стэк (stack)`? В какой памяти создаются объекты, примитивные типы и блоки? [[+]](https://gist.github.com/arthurigberdin/0f82aa713439a93f1974)
- Что такое `полиморфизм`?  [[+]](https://gist.github.com/arthurigberdin/f59ac4b1e360b8d4e673)
- Что такое `инкапсуляция`? Что такое `нарушение инкапсуляции`? [[+]](https://gist.github.com/arthurigberdin/73dde36439b947e28764)
- Какие полезные быстрые клавиши знаешь, используешь? [[-]](https://gist.github.com/arthurigberdin/2b37c29e96363b5e3468)
- Чем `абстрактный класс` отличается от `интерфейса`? [[-]](https://gist.github.com/arthurigberdin/2d959bb91c454859010c)
- Расскажите о `паттерне MVC`. Чем отличается `пассивная` модель от `активной`?[[+]](https://gist.github.com/arthurigberdin/ea1827b7628019a0dc4e)
- Реализация `синглтона (Singleton)` в `ARC` и в `non-ARC`?[[-]](https://gist.github.com/arthurigberdin/3670dbea7d6c2e0f10f9)
- Назовите основные отличия `синглтона` от `статического класса`, и когда следует использовать один, а когда другой? [[+]](https://gist.github.com/arthurigberdin/9eea0fa48405f36e592d)
- Как пересоздать синглтон? Можно ли `обнулить объект синглтона`? [[-]](https://gist.github.com/arthurigberdin/8820aa764b0c179eea65)
- Что такое сериализация объекта?
- Какие знаете паттерны? Классификация паттернов? [[-]](https://gist.github.com/arthurigberdin/824796346653351a86d9)
- Паттерн `MVC vs MVP vs MVVM`? https://habrahabr.ru/post/215605/
- Что такое `responder chain`?
- Как работают `push нотификации`? [[-]](https://gist.github.com/arthurigberdin/dffa57f7268d99f96aad)
- Принципы `DRY`?
- Принципы `KISS`? 
- Принципы `SOLID`? [[-]](https://gist.github.com/arthurigberdin/bb53805be1b988bc9237)
- Что такое `IoC`? 
- Что такое Dependency Injection?
- Игра в `разбитые окна`?
- Что такое `VIPER`?
- Что такое `TDD`?
- Что такое `DDD`?

Swift
----------
- `Фундаментальные` типы и `коллекции`? [[-]](https://gist.github.com/arthurigberdin/02575edda45a33c0f68063bd49ced3a9)
- Aттрибут `@UIApplicationMain` ?
- Что такое `Bridge Header`? Как использовать Objective-C код в Swift проекте?
- Оператор `guard`?
- `Интерполяция` vs `конкатенация` строк?
- `let` vs `var`?
- `typealias`? Создание своего собственного типа?
- nil в Swift vs nil в Objective-C? Различия?
- Оператор `??`?

