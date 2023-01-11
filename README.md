# Programs



f

rom Maciej Gaszynski to Everyone:    4:32  PM



String pattern = "F";
pattern = "Ba";
long count = Stream.of("Foo", "Bar", "Baz")
    .filter(s -> s.startsWith(pattern))
    .count();




class Point {
    int x, y;
    Point(int x, int y) {
      this.x = x;
      this.y = y;
    }
}
new Point(1, 2).equals(new Point(1,2))



class Foo {
    int count = 0;
    void increment() {
        count = count + 1;
    }
    void run() {
        ExecutorService executor = Executors.newFixedThreadPool(2);
        IntStream.range(0, 10000)
            .forEach(i -> executor.submit(this::increment));
        // stop(executor);
        System.out.println(count);
    }
}



class Foo {
    static synchronized bar() {
    }
    synchronized baz() {
    }
}
Thread 1:
foo.bar();
Thread 2:
foo.baz();

Lock lc = new ReentrantLock();

lc.lock()
lc.unlock()





class Point {
    int x, y;
    int hashCode() {
        return x + y;
    }
    boolean equals(Object p) {
        return y == p.y;
    }
}



1->linked list
2->linked list
3
4




@Test
void shouldCreateMailMessageAccordingToConfiguration() {
    // given
    ArgumentCaptor<SimpleMailMessage> captor = ArgumentCaptor.forClass(SimpleMailMessage.class);
    MailSender mailSender = mock(MailSender.class);
    ResultReporterConfiguration configuration = new ResultReporterConfiguration("FROM", "TO", "SUBJECT");
    ResultReporter resultReporter = new ResultReporter(mailSender, configuration);
    // when
    resultReporter.reportResult();
    // then
    verify(mailSender).send(captor.capture());
    assertThat(captor.getValue().getTo()).containsExactly("TO");
    assertThat(captor.getValue().getFrom()).isEqualTo("FROM");
    assertThat(captor.getValue().getSubject()).isEqualTo("SUBJECT");
}

class B {

}

class A {

@Autowired
private B b;

@Autowired
A() {

}

public int result() {
    int val = b.someMethod();
    return val;
}

}


class Test {

@test
 public void testResult() {
   
   A a = new A();
   

 }   


}




@Component
@RequiredArgsConstructor
class ReportGenerator {
    private final MeterRegistry meterRegistry;
    private final List<String> customers;
    @Cacheable("report")
    @Transactional
    public void generate(String customerId) {
        meterRegistry.forEachMeter(m -> {
            // match and generate
        });
    }
    public void generateForAllCustomers() {
        customers.forEach(this::generate);
    }
}



@SpringBootTest
class ReportGeneratorTest {
    @Autowired
    ReportGenerator reportGenerator;
    @Test
    void shouldInjectProperBean() {ReportGenerator$ jsd
        assertEquals(ReportGenerator.class, reportGenerator.getClass());
    }
}





