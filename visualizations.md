# Visualization Policies and Guidlines
## Definitions

A composite dashboard brings in multiple panels of metrics over a common timeframe into a single view.

A unit of measure (UOM) is a standardized quantity used to express and compare numerical properties, values, or magnitudes. There are different types of UOMs. A UOM may be a simple absolute value. For example, "bytes" is a UOM with an absolute (plain) value. Other UOMs may be more complex and have a denominator. 

A Unit of Time (UOT) is a UOM that designates a span of time, such as milliseconds, seconds, days, etc. 

Some UOMs are complex and have a denominator and numerator. Often a UOT is used as the denominator. For example, "bytes per second." 

UOMs have a scale that indicates the magnitude of a UOM. For example bytes may be measured in bytes, kilobyte gigabytes, etc. UOTs have a scale, too, nanoseconds, microseconds, milliseconds, etc. 

Some UOMs are dimensionless. Percents are dimensionless UOMs that are the ratio of two UOMs withthe same dimensions. For example used CPU over available CPU, is known as "percent CPU." In this case the base UOM of the denominiator and numerator is implied and not even stated. 

Counts are also dimensionless as they do not have a particular measure - they are just a tally.

An axis title is the alphabetic label placed next to an axis that descibes the measures plotted with the same scale as the axis. 

Tick labels are the quantitative values that indicate the level of the metric at that height of the tick. 

A time series, or series for short, is a plot of measures of a metric over time. The scale of the measures is indicated by the tick marks on one of the vertical axis.  

# Statements
1. A composite dashboard should display two columns of panels
1 Two-column dashboards must use the same width for the left and right panels 
1.1 If there is are an odd number of panels, the last (odd left) panel must have the same width as the other panels

## Panels
1. A panel must have a left axis
1. A panel may have a right axis
1. A series plotted against the left vertical axis must use solid graph lines
1. A series plotted against the right veritcal axis must have dotted graph lines
1. Every axis must have a title that indicates the unit of measure
1. Axis titles must state the unit of measure of the metrics on displayed on the axis 
1.1 Developers must scale the the UOMs of metrics on the same axis so they all have the same UOM and possibly UOT
1.1. Developers must only scale metrics on an axis so tht they have the same UOM
1. Tick labels must be labels with just numeric values
1. Developers must scale a series so that tick labels are up to 3 digits or two digits with one signifcant (fractional) digit

