# FloatSliderCtrl
Custom wxSlider widget that handles floats. Widget also displays labels as floats

Please read docstrings for further instruction

    FloatSliderCtrl.FloatSliderCtrl(
        self,
        parent,
        id=wx.ID_ANY,
        value=None,
        minValue=0.0,
        maxValue=100.0,
        increment=None,
        pos=wx.DefaultPosition,
        size=wx.DefaultSize,
        style=wx.SL_HORIZONTAL,
        name=wx.SliderNameStr
    )
    
    parent    - parent wxWindow instance
    id        - wxID or defaults to wxID_ANY to obtain a new wxID
    value     - starting position of the slider
    minValue  - the lowest the slider can be set to
    maxValue  - the highest the slider can be set to
    increment - the distance to traven when the slider is moved
    pos       - where to display the widget
    size      - the display size of the widget
    style     - wx.SL_HORIZONTAL: Displays the slider horizontally.
                wx.SL_VERTICAL: Displays the slider vertically.
                wx.SL_AUTOTICKS: Displays tick marks. Windows only.
                wx.SL_MIN_MAX_LABELS: Displays minimum, maximum labels.
                wx.SL_VALUE_LABEL: Displays value label.
                wx.SL_LABELS: Displays minimum, maximum and value labels.
                wx.SL_LEFT: Displays ticks on the left and forces the slider to be vertical.
                wx.SL_RIGHT: Displays ticks on the right and forces the slider to be vertical.
                wx.SL_TOP: Displays ticks on the top and forces slider to be horizontal.
                wx.SL_BOTTOM: Displays ticks on the bottom and forces the slider to be horizontal.
                wx.SL_SELRANGE: Allows the user to select a range on the slider. Windows only.
                wx.SL_INVERSE: Inverses the minimum and maximum endpoints on the slider.
                               Not compatible with wx.SL_SELRANGE.

                Notice:
                    SL_LEFT , SL_TOP , SL_RIGHT and SL_BOTTOM specify the position of the
                    slider ticks in MSW implementation and that the min/max labels,
                    if any, are positioned on the opposite side. So, to have a label on
                    the left side of a vertical slider, wx.SL_RIGHT must be used.

                Warning
                    If using SL_AUTOTICKS as an example if you have an increment
                    set at 0.001 and a min of 0.0 and a max of 10000.00 this will cause the
                    widget to hang due to trying to draw 10,000,000 tick marks.
    name      - people friendly name to associate to the widget


    public methods:
        IsMinMaxLabel() - returns bool(): if the min/max labels are displayed
        IsValueLabel() - returns bool(): if the value label is displayed
        IsInverse() - returns bool(): if wxSL_INVERSE has been set
        GetValue() - returns float(): current thumb position
        GetMin() - returns float(): current min value
        GetMax() - returns float(): current max value
        GetIncrement() - returns float(): current increment
        GetSelStart() - returns float() or None: current selection start position, None if one has not been set
        GetSelEnd() - returns float() of None:current selection stop point, None if one has not been set
        SetSelection(min, max) - returns None: str() a float() or an int() the start and stop points for a selection
        SetMinMaxLabel(flag=True) - returns None: bool() to turn on the min/max labels
        SetValueLabel(flag=True) - returns None:bool() to turn on the value label
        SetValue(value) - returns None:  str() a float() or an int() sets the thumb position
        SetMin(minValue) - returns None: str() a float() or an int() sets the minimum the slider can be set to
        SetMax(maxValue) - returns None: str() a float() or an int() sets the maximum the slider can be set to
        SetIncrement(increment) - returns None: str() a float() or an int() sets the distance to travel when the thumb is moved
        SetRange(minValue, maxValue) - returns None: str() a float() or an int() set the minimum and maximum slider values
        


this control inherits all the methods from a wxSlider instance please see documentation on wxSlider for the remainder of vailable methods
