.. EN-Revision: none
.. _zend.json.basics:

Utilisation de base
===================

L'utilisation de ``Zend_Json`` implique l'emploi des deux méthodes statiques publiques disponibles :
``Zend\Json\Json::encode()`` et ``Zend\Json\Json::decode()``.

   .. code-block:: php
      :linenos:

      // Obtention d'une valeur
      $phpNatif = Zend\Json\Json::decode($valeurCodee);

      // Codage pour renvoi au client :
      $json = Zend\Json\Json::encode($phpNatif);



.. _zend.json.basics.prettyprint:

Pretty-printing JSON
--------------------

Sometimes, it may be hard to explore *JSON* data generated by ``Zend\Json\Json::encode()``, since it has no spacing or
indentation. In order to make it easier, ``Zend_Json`` allows you to pretty-print *JSON* data in the human-readable
format with ``Zend\Json\Json::prettyPrint()``.

.. code-block:: php
   :linenos:

   // Encode it to return to the client:
   $json = Zend\Json\Json::encode($phpNative);
   if($debug) {
   echo Zend\Json\Json::prettyPrint($json, array("indent" => " "));
   }

Second optional argument of ``Zend\Json\Json::prettyPrint()`` is an option array. Option *indent* allows to set
indentation string - by default it's a single tab character.


