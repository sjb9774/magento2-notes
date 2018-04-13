# Magento 2 Framework

This primarily PHP software framework is organized into logical groups called libraries, which all modules can call.
* Controls how application components interact, including
*	Request flow
*	Routing
*	Indexing
*	Caching
*	Exception Handling
*	Most of the framework code sits under the domain layer or encloses the presentation, service, and domain layers.
*	Contains no business logic,
*	Does contain code to help implement resource models.
*	You should not modify framework code
*	Modules you create will typically inherit from classes and interfaces defined in the Framework directives
*	Provides libraries that help reduce the effort of creating modules that contain business logic, including
*	handling HTTP protocols
*	interacting with the database and filesystem
*	rendering content
## Structure
*	`/vendor/magento/framework`
*	Libraries of code & the application entry point that routes requests to modules.
*	Contains only PHP.
*	`/lib/internal`
*	Contains some PHP and some LESS/CSS & JavaScript framework libraries.
*	`/lib/web/`
*	Contains JavaScript & LESS/CSS files.
*	These files are accessible from a web browser.
*	Any code that a web browser must access should be under web, everything under internal.
*	`/vendor/magento/framework` maps to the Magento\Framework namespace

## Highlights
The Magento Framework (lib/internal/Magento/Framework) provides a number of namespaces that may be of interest to an extension developer.
*	`Magento\Framework\DataObject`
    * Provides standard functionality for storing and retrieving data through magic methods.
    *	Base class for many Magento classes.
*	`Magento\Framework\DataObject\Model`
    *	Contains base model classes that almost all Magento Model classes extend from.
*	`Magento\Framework\DataObject\AbstractModel`
*	`Magento\Framework\DataObject\Controller`
    *	Contains classes to help return different types of results (JSON, redirects, etc).
*	`Magento\Framework\DataObject\View`
    *	Contains code to render pages and layouts.
*	`Magento\Framework\DataObject\Data`
    *	Contains additional classes that handle forms.
*	`Magento\Framework\DataObject\URL`
    *	Contains code to look up other pages in Magento.
*	`Magento\Framework\ObjectManager`
    *	Provides dependency injection.
*	`Magento\Framework\App`
    *	`Contains bootsrap, CLI, webapp, and cron code.`
    *	Routes requests while providing deployment context.
*	`Magento\Framework\Api`
    *	Contains base classes for objects that can be extended to add new data through extensions.
*	`Magento\Framework\Config`
    *	Contains the generic configuration reader which is extended into a specialized reader for each config file.
*	`Magento\Framework\Filesystem`
    *	Contains classes that handle file I/O.
*	`Magento\Framework\HTTP\PhpEnvironment`
*	`Magento\Framework\Session`
*	`Magento\Framework\Stdlib\Cookie`
    *	Code to handle the HTTP requests & responses.
    *	Session & cookie code lives here.
*	`Magento\Framework\Exception`
    *	Contains basic exceptions that are thrown throughout the Magento codebase.
*	`Magento\Framework\Event`
    *	Contains the code that publishes synchronous events and that handles observers for any Magento event is handled here.
*	`Magento\Framework\Validator`
    *	Contains code that validates data (currencies, not empty) and that handles observers for any Magento event.
