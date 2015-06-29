A fully featured gantt chart component built entirely in Javascript, CSS and AJAX. No images required.

You can view a live example at http://jsganttimproved.x10host.com/

Features include:
  * Tasks & Collapsible Task Groups
  * Dependencies
  * Task Completion
  * Task Styling
  * Milestones
  * Resources
  * Dynamic Loading of Tasks
  * Dynamic change of format (hour/day/week/month/quarter)
  * Load Gantt from XML
    * From external files (including experimental support for MS Project XML files)
    * From JavaScript Strings
  * Support for Internationalisation (all hard coded strings can be overridden)

Project forked as I was unable to contact the original maintainers.  This work was done to support a personal project that didn't warrant a more heavyweight system (e.g. the dojo toolkit gantt chart features).

**Changes in v1.7.4 ([r59](https://code.google.com/p/jsgantt-improved/source/detail?r=59))**
  * Instantiating a new JSGantt.TaskItem will now also accept Date objects for start and end dates
  * Fixed old Internet Explorer compatibility broken by v1.7
  * Fixed bug in Iso week date format
  * Changed to solid arrows on dependency lines to be more printer friendly
  * Code refactoring and clean up

**Changes in v1.7 ([r49](https://code.google.com/p/jsgantt-improved/source/detail?r=49))**
  * Fixed nasty long-standing bug where the first Gantt chart created must be stored in a javascript variable named "g"
    * NOTE: This required a change in the method to instantiate a JSGantt.TaskItem object to pass the related chart
    * A temporary fix is included that still assumes the use of "g" for the chart if the chart object is not passed, this will be removed in v1.8

  * Altered XML export functionality so that dates are output in the specified input format for the chart
  * Added method to read XML directly from an input string
  * Prevented creation of a task with a duplicate "unique" ID
  * Fixed bug where attempting to remove the first task defined would prevent the chart from redrawing
  * Some general code clean up

**Changes in v1.6 ([r42](https://code.google.com/p/jsgantt-improved/source/detail?r=42))**
  * Allow use of internationalised strings in custom date formats
  * Modified how tooltip is hidden and revealed to make it more compatible with CSS transitions
  * Added experimental support for importing Microsoft Project XML files
  * Added methods to generate JGI XML from current task list

**Changes in v1.5 ([r36](https://code.google.com/p/jsgantt-improved/source/detail?r=36))**
  * Added support for Internationalisation
  * Task duration now calculated using the same method as is used to size and position task bars
  * Milestones owned by combined group items are now ignored completely rather than hidden
  * Fixed positioning bug in day format when calculating a period that spanned an odd number of DST clock changes which would result in a position 1hr out of place - approximately 4% of a single column width.
  * Fixed a number of minor bugs
    * Dependencies on the first task displayed were not shown
    * Combined group task rows are now styled like standard tasks
    * Disabling the tool tip caused problems with scrolling

**Changes in v1.4 ([r24](https://code.google.com/p/jsgantt-improved/source/detail?r=24))**
  * Reintroduced Hour format view

**Changes in v1.3 ([r22](https://code.google.com/p/jsgantt-improved/source/detail?r=22))**
  * Added new "combined groups" task type that shows all child task information on one row.
  * Tooltip DIV restructured to use styles rather than line breaks for layout
  * Code refactored for ease of future development
  * See [r21](https://code.google.com/p/jsgantt-improved/source/detail?r=21) for details of CSS changes

**Changes in v1.2 ([r18](https://code.google.com/p/jsgantt-improved/source/detail?r=18))**
  * Multiple gantt charts per page are now supported
  * Charts are now more printer friendly (see [Issue 6](https://code.google.com/p/jsgantt-improved/issues/detail?id=6) for a discussion of the limitations)
  * See [r18](https://code.google.com/p/jsgantt-improved/source/detail?r=18) for details of CSS structural changes

**Changes in v1.1 ([r11](https://code.google.com/p/jsgantt-improved/source/detail?r=11))**
  * Added support for additional dependency types
  * Altered date parsing to handle specifying time more consistently
  * Updated CSS to prevent growing DIV bug in IE9

**Significant changes from the original jsgantt project: ([r4](https://code.google.com/p/jsgantt-improved/source/detail?r=4))**
  * Vast majority of look and feel now controllable via CSS
  * Optimised chart structure to reduce number of elements required / ensure positioning match
  * Chart pane width will change dynamically with containing element
  * Tool tips added to gantt chart bars to display full task details
  * Hour/Minute format removed
  * Various bug fixes