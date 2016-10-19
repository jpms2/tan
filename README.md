# tan

Tool made for finding possible controllers inside .erb views.
Ruby version : 2.3.1

Run it by running: (don't forget to bundle install!)
  ruby Grab_controller_from_erb_file.rb
  
Architecture:
  
  [Grab_controller_from_erb_file.rb](https://github.com/jpms2/tan/blob/master/ErbFileAnalyser/Grab_controller_from_erb_file.rb) is the main file, receiving all methods and calling them together to create an output folder on the    directory.
  [Erb_tags_remover.rb](https://github.com/jpms2/tan/blob/master/ErbFileAnalyser/Erb_tags_remover.rb) gets the raw input and finds erb chunks of code, transforming them into pure ruby code
  [method_controller_visitor.rb](https://github.com/jpms2/tan/blob/master/Visitors/method_controller_visitor.rb) walks through the parse tree looking for method calls that might be made by a controller and output them as an array of output_model
