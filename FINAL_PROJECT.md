###Final Project Breakdown (Phases)
__TODO__
  * Phase 1: Read in a hardcoded JSON file (as text) and output the raw contents to STDOUT
  * Test Phase 1: How could we test this? - Class discussion - Suggestion create a ``generateReceipt`` method  which takes an ``InputStream`` and an ``OutputStream`` performs the task and write a test for that
  
  * Phase 2: Update the app to write the contents of the input file to a hard coded receipt file
  * Test Phase 2: How could we test this? - Class discussion
  
  * Phase 3: Update the app to extract the file names from the command line invokeation and display an usage / error message if the usage is incorrect
  * Test Phase 3: How could we test this? - Suggestion: Refactor code into a ``CommandLineParser`` to populate a ``JobConfigurationBean`` with ``orderFilename`` and ``recieptFilename`` and write tests for that.
  
  * Phase 4: Update the app to display error messages if the relevant files cannot be written or read
  * Test Phase 4: How could we test this? - Suggestion: Code a  ``Logger`` interface and ``SimpleLogger`` class implementation that writes to STDOUT or STDERR. Refactor ``generateReceipt`` to get the logger to use from teh ``JobConfigurationBean`` and write tests which invoke ``generateReceipt`` with various ``JobConfigurationBean`` 
  
  * Phase 5: Update the app to parse the JSON into ``org.json.JSONObject``s and output the results for toString on these objects to the output file
  * Test Phase 5: How can we test this? - Suggestion: Refactor code into a ``OrderFileParser`` which has the single responsibility of converting a json text ``InputStream`` into ``JSONObject``s.
  
  * Phase 6: Create JavaBean Classes to represent each of ``Order``, ``Customer``, ``StoreInfo``, ``LineItem``, ``Product``
  * Test Phase 6: How can we test this? - Suggestion: Write tests for the to ensure they have working getters and setters for all the fields we want to read from the JSON. For example ``Order`` should have fields for ``customer``, ``storeInfo``, ``lineItems``. ``LineItem`` should have ``product`` and ``quantity``
  
  * Phase 7: Create an ``OrderFactory`` with a method which takes a populated  ``JSONObject`` as a parameter and returns a correctly populated instance of the ``Order`` JavaBean defined in the previous phase. The JSON objects in the sample file 
  * Test Phase 7: How can we test this?