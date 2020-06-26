/*===========================Flex-Box=======================================*/




First of all let's understand that what is flex-box?.So,for the question we have an quick answer that is Flex-Bos is an CSS Flexible Box module or one dimensional  layout module which makes to design flexible and efficient layouts,to distribute space among items and to control items alignments in the container.

  Upto now we were bored and spent much time to align items to left and right and centering items and for most things.But with this flexbox we can make it as simple as that.

  We are going to have two terminology in this flex-box,those are flex container and the flex items. 
  Let's see with an example here:
          
          <div class="container">
              <div>item 1</div>
              <div>item 2</div>
              <div>item 3</div>
          </div>
  
      In the above example the parent container class will be the flex container and the items nested inside of it called as flex items.
 Flexbox Axis:
 While working with the flex-box we are going to have two axes,those are Main axis and the Cross axis.
 By default the main axis will runs from left to right while the cross axis will runs perpenducular to main axis i.e, top to bottom.

 The default and the staring of the main axis will call as main start and the end point termed as main-end and the length from the main-start to the main-end is called as main-size.
 So,we can say that flex items will flow from main start to main end and takes up the size of main size.Similarly for cross axis we have cross start and the cross end and the lenght would be the cross size.


 So,in this entire flex-box we are going to deal with flex containers and the flex items by using flex properties to make our layout more flexible and responsive.


 The Properties assosciated with the flex-containers:

 1) Display property:Which defines the flex container and its manditory to work with flexbox.
 2) Flex-direction: It defines the direction in which the flex items are placed in the container.
 3) Flex-Wrap:It is used to control the wrapping of the items within the container.
 4) Flex-flow:It is shorthand combination for flex-direction and the flex-wrap.
 5) Justify-content: It defines the alignment of items along the main-axis.
 6) align-items: It defines the alignment of items along the cross axis.
 7) align-content:This is just similar to justify content which difference between this will align along the cross axis where justify content aligns on main axis.And this will work only when there are multiple rows of flexitems in the container.



 Let's learn the properties in detail:

 1) Display Property:

 To create a flex container we make use of display property and set it to a value of flex

   In the CSS
      .container{
          display:flex;
      }
 
 Then our container flex container,we can see the changes that the items will align into main axis from left to right.
  By default the flex container is an block level container,if we dont want our container to be block level,we can make it to inline-flex which acts as inline container.

  So,with the display property we can use two values: flex and inline-flex



  2) Flex-Direction:
     Flex-direction interms the main axis how the flex items are placed inside the container.By default the main axis flows from left to right so that our items will place from left to right.

     The following are the values for flex-direction property
      flex-direction: row;                === which is the default alignment in flex direction.
                      row-reverse;        === Which makes the items to align reversly in the row.
                      column;             === Which makes the items to align column.
                      column-reverse      === which makes the items to align column but items reversly.

  3) Flex-wrap:

    flex-wrap: nowrap;   === which is default value
               wrap;      === to make the items to wrap within the container( Mainly used to wrap when it display in small width devices)
             
               wrap-reverse; ===which makes same as wrap value but in reverse order of item.

   4) Flex-flow: // which is a combination of flex-direction and flex-wrap property //
                row nowrap:
                row wrap;
                row wrap-reverse;
                column wrap;
                column wrap-reverse;

    flex-flow: <flex-direction> <flex-wrap>

 Alignment properties:

 5) justify-content:flex-start;       === by default the items will start from flex-start
                   : flex-end;     === Which makes the items to place at the end of the axis i.e,    right side
                   :center;        === which aligns the content to the center of the axix.
                   : space-between; === which provied space between the items.
                   :space-around;   === which provides space around the items, both left and right ( Not top anf bottom)
                   :space-evenly;    === which provides space evenly .


 6) align-items: This property defines how items to aline along the corss axis.

                align-items:stretch;  === By default the value is stretch,which stretc the entire lenght of the cross axis from top to the bottom.(Mentioned height)
                   
                           :flex-start;  === all the items to be pushed to cross-start.(top)
                           :flex-end;    === all the items to be pushed to cross-end (to bottom)
                           :center:      === centered items to the cross axis.
                           :baseline;   === align items all to its baseline regarding the size of the items.

7) align-content: its distibutes additional space but along cross axis.Condition to use is to exist mutiple rows otherwise no effect can seen.

         align-content:stretch;     ===default value
                      :flex-start;  
                      :flex-end;
                      :space-between;
                      :space-around;
                      :center;


  FLEX-ITEM PROPERTIES:
    
    order       === Control the order of an item in the flex-container (It accepts integer value)



    flex-grow   === Its relative and dedicates what amount of the available space inside the flex container the item should takeup.
              : Relative to the other items in the container.
              :default value is 0-items do not grow.
              : flex-grow value of 1-flex items grow evenly.
    



    flex-shrink:It dictates the shrink factor of the flex-items when the default size of the flex-items is larger than the flex-container.
               : Relative to the other items in the container.
               : Default value is 1.


    flex-basis:Set the initial size of a flex-item.
              : It accepts in pixels,percentages,or relative units.
              : Default value is auto.





    flex:shorthand for flex-grow,flex shrink and flex-basis.

       : one value,unitless value:Then it will take as flex-grow
        flex:2;

        : one value,width/height:Then have to consider  as flex-basis
          flex:10em;
          flem:30px;

          Two values: flex-grow   | flex-basis
           flex: 1 30px;

           Two values: flex-grow | flex-shrink
            flex: 2 2;

             Three values: flex-grow | flex-shrink | flex-basis
             flex: 2 2 10%;




    align-self:It is used to align items individually.
              : values like auto,flex-start,flex-end,center and stretch.
              : overrides the align-items vakye of the flex container.
