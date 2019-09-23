# 2019.9.23
牛客网补充
1.sleep()方法
  在指定时间内让当前正在执行的线程暂停执行，但不会释放“锁标志”。不推荐使用。sleep()使当前线程进入阻塞状态，在指定时间内不会执行。
2.wait()方法
  在其他线程调用对象的notify或notifyAll方法前，导致当前线程等待。线程会释放掉它所占有的“锁标志”，从而使别的线程有机会抢占该锁。当前线程必须拥有当前对象锁。如果当前线程不是此锁的拥有者，会抛出IllegalMonitorStateException异常。唤醒当前对象锁的等待线程使用notify或notifyAll方法，也必须拥有相同的对象锁，否则也会抛出IllegalMonitorStateException异常。waite()和notify()必须在synchronized函数或synchronized　block中进行调用。如果在non-synchronized函数或non-synchronized　block中进行调用，虽然能编译通过，但在运行时会发生IllegalMonitorStateException的异常。
3.yield方法 
  暂停当前正在执行的线程对象。yield()只是使当前线程重新回到可执行状态，所以执行yield()的线程有可能在进入到可执行状态后马上又被执行。yield()只能使同优先级或更高优先级的线程有执行的机会。 
4.join方法
  等待该线程终止。等待调用join方法的线程结束，再继续执行。
5.抽象类表示的是is-a关系，强调的是从属关系；接口表示的是like-a关系，强调的是功能。
6.byte [  ]  String.getBytes(String charsetName);  得到的是以charsetName编码得到的byte数组；
String的构造函数有： String (byte[] bytes, String  charsetName);
7.一个对象成为垃圾是因为不再有引用指着它，但是线程并非如此
8.当没有任何对象的引用指向该对象时+在下次垃圾回收周期来到时=>对象才会被回收
9.finalize方法是确保一个对象在被回收之前，要释放该对象占有的某些资源（例如文件句柄）

10.
