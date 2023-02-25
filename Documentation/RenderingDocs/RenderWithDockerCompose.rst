.. include:: /Includes.rst.txt
.. highlight:: bash
.. Index:: Rendering; Docker Compose
.. _render-with-docker-compose:

===============================================
Rendering the documentation with Docker Compose
===============================================

This workflow is very similar to :ref:`render-documentation-with-docker`,
it uses the same Docker image, but the commands for running it are slightly
different.

This workflow is especially recommended for platforms
where the source / run command may not work, but should
work fine on all platforms.

.. important::

   The workflow with Docker Compose is still being tested and optimized.
   Please help to improve our description by:

   *  Testing the workflow. Report your results in this
      `issue <https://github.com/t3docs/docker-render-documentation/issues/26>`__
   *  Improving this page if you can

.. rst-class:: bignums-xxl


#. Install Docker and Docker Compose

   *  https://docs.docker.com/install/
   *  https://docs.docker.com/compose/install/

#. Create a docker-compose.yml file

   .. tip::

      Some of our repositories already contain
      this, for example the :ref:`t3contribute:start`
      or this guide.

   You can create the file in the project directory.

   .. code-block:: yaml

      version: '3'
      services:
        t3docmake:
          image: t3docs/render-documentation:latest
          command: makehtml
          volumes:
            - ./:/PROJECT:ro
            - ./Documentation-GENERATED-temp:/RESULT

#. Run docker-compose

   .. code-block:: bash

      docker-compose run --rm t3docmake

#. See output of command for generated HTML start file

   You can use one of these commands to open the generated
   file in the browser:

   .. tabs::

      .. group-tab:: Linux

         .. code-block:: bash

            xdg-open "Documentation-GENERATED-temp/Result/project/0.0.0/Index.html"

      .. group-tab:: MacOS

         .. code-block:: bash

            open "Documentation-GENERATED-temp/Result/project/0.0.0/Index.html"

      .. group-tab:: Windows

         .. code-block:: powershell

            start "Documentation-GENERATED-temp/Result/project/0.0.0/Index.html"

