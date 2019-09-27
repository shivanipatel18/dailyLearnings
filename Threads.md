# Looper

Looper is a class which is used to execute the Messages(Runnables) in a queue. Normal threads have no such queue, e.g. simple thread does not have any queue. It executes once and after method execution finishes, the thread will not run another Message(Runnable).

#### Where we can use Looper class?

If you want to execute multiple Runnables then you should use the Looper class which is responsible for creating a queue in the thread. For example, while writing an application that downloads files from the internet, we can use Looper class to put files to be downloaded in the queue.

#### How it works?

There is prepare() method to prepare the Looper. Then you can use loop() method to create a message loop in the current thread and now your Looper is ready to execute the requests in the queue until you quit the loop.

Here is the code by which you can prepare the Looper.

```
class LooperThread extends Thread {
      public Handler mHandler;

      @Override
      public void run() {
          Looper.prepare();

          mHandler = new Handler() {
              @Override
              public void handleMessage(Message msg) {
                  // process incoming messages here
              }
          };

          Looper.loop();
      }
  }
```
