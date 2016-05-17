# EasyTimer
A JavaScript setTimeout and setInterval implementation in C#. More details - http://dailycoding.com/Posts/easytimer__javascript_style_settimeout_and_setinterval_in_c.aspx

##Usage

To use setTimeout this you can simply do -

    EasyTimer.SetTimeout(() =>
    {
        // --- You code here ---
        // This piece of code will once after 1000 ms delay
    
    }, 1000);
    
The code will run after 1000 ms delay similarly like JavaScript setTimeout. The function also returns a handle. If you want clearTimeout like functionality, then the simply dispose off the handle. 

    var stopHandle = EasyTimer.SetTimeout(() =>
    {
        // --- You code here ---
        // This piece of code will once after 1000 ms
    
    }, 1000);
    
    // In case you want to clear the timeout
    stopHandle.Dispose();

Similarly you can use setInterval as -

    EasyTimer.SetInterval(() =>
    {
        // --- You code here ---
        // This piece of code will run after every 1000 ms
    
    }, 1000);

and SetInterval also returns a stop handle which you can use for clearInterval like functionality. Just dispose off the handle -

    var stopHandle = EasyTimer.SetInterval(() =>
        {
            // --- You code here ---
            // This piece of code will run after every 1000 ms
            // To stop the timer, just dispose off the stop handle
    
        }, 1000);
    
    // In case you want to clear the interval
    stopHandle.Dispose();
