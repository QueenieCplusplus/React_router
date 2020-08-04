# React_router
SPA 需要路由器將 url path 導向正確的元件，其他框架則是導向函數

# {withRouter}

    (to be continued...)

# {NavLink}

    (to be continued...)

# react-router

      //2020, 7/11, am 11:20- 12:20 (Duration: 20 mins)
      // React Router Component



      // react-router Framework
      // <Router/> is a component
      // func is also a component
      // url: /abc -> render AppComponent which is the handlerComponent
      // Routes 元件內包覆很多 Route 元件 指向 path url 和指定處理器（又稱為函數）


      var Route = require("react-router").Route;

      var ksAppRouter = (
          <Routes>
              <Route name="home" path="/" handler={homeHandler}>
              <Route name="abc" path="/abc" handler={abcHandler}/>
              <Route name="query" path="/query/:queryId" handler={queryHandler}/>
              <NotFound title="page not found" handler={noPageHandler}/>
          </Routes>
      );

      // top level component renderer
      React.renderComponent(
          ksAppRouter,
          document.querySelector('body')
      )

# BackBone Router

      // BackBone Framework 運作方式很像 Django 或是 CI in PHP
      // url: /abc -> execute func -> load data from server to browser and render on <abc/> component
      var KRouter = Backbone.Router.extend({

          routes:{

             // "/url": "func name"
             "abc": "funcall"

          },
          funcall: function(){

              React.renderComponent(
                  <abc/>,
                  document.querySelector('body')
              );

          }

      });


