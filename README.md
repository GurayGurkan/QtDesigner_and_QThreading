"Hello World" application of QtDesigner and QThread module merging.

1) - "example.ui" file is created by QtDesigner via Main Window class and involves:
    - 3 pushButtons named as: work, eat and sleep
    - 3 progressBars named as: work_progressBar, eat_progressBar, sleep_progressBar
  
2) After example.ui file is created it should be converted to "*.py" file via:

    pyuic4 -x example_gui.ui -o example_gui.py
    
3) After gui file is finished, a new file named "example_main.py" is created. 

By the command 
    import example_gui
    
and by subclassing a new main window object via
  
  class Window_Name(QMainWindow,example_gui.Ui_MainWindow):
      def __init__(self,parent=None):
          super(Window_Name,self).__init__(parent)
          self.setupUi(self)
...

we initiate the class. This main window class should create the fonctionalaties of buttons and progress bars. 
