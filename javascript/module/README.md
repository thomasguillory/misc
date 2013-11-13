@module helper
===============
This is helper that helps you to manage your namespaces while working in JS.

Install
------------
Import module.js.coffee or module.js at the top of your assets pipeline

Usage
------------

    # In this scope @ is your root element like `document`
    @module 'MyApp.Controller', ->

      # In this scope @ is MyApp.Controller
      #
      # MyApp = {
      #   Controller: {}
      # }
      # 
      

      # So if define something like
      class @HomeCtrl
        ...

      # This is define as MyApp.Controller.HomeCtrl !


    # You can also use @module in a nested way
    @module 'MyApp', ->
      @module 'Controller', ->
        ...
