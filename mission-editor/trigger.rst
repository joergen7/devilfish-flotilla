Triggers
========

Syntax
------

Number
^^^^^^

::

  n ::= [number]

Platform
^^^^^^^^

::

  p ::= [unit]

Dynamic Group
^^^^^^^^^^^^^

::

  g ::= [group]

Side
^^^^

::

  s ::= SIDE-0
      | SIDE-1
      ...
      | SIDE-8
      | ANY-SIDE

Sensor
^^^^^^

::

  o ::= ACTIVE-INTERCEPT
      | AI-688I-TA
      | AI 688I-TAD
      | ...

Numerical Operators
^^^^^^^^^^^^^^^^^^^

::

  op ::= ==
       | !=
       | <
       | >

Boolean Expressions
^^^^^^^^^^^^^^^^^^^

::

  e ::= Attack p By p
      | Attack-Side s By p
      | Completed-Trigger i
      | Detect p By p With o
      | Detect-All-In-Group g By p With o
      | Detect-Any-In-Group g By p With o
      | Detect-Side p By s
      | First-Failed-Criteria i
      | First-Met-Criteria i
      | Group-Was-Created g
      | Is-Current-Controllable p
      | Is-Detection-Held-Now p
      | Kill-All-In-Group g
      | Kill-Any-In-Group g
      | Landing p On p
      | Landing-Of-Class c On p
      | Launch-DSRV
      | Launch-Seals
      | Launch-UUV
      | Lost-Detection p On p
      | Met-Criteria-Duration i op n Sec
      | Ownship-Detect p With o
      | Ownship-Detect-Side s
      | Platform-Damage p op n %
      | Platform-Exists p
      | Range p To p op n Nmi
      | Take-Off p From p
      | Take-Off-Of-Class c
      | Take-Photo-Of p
      | Take-Photo-Of-Object-Of-Class c
      | Time-Since-Trigger-Fired i op n Sec
      | Trigger-Refire-Count i op n
      | NOT e
      | (e AND e)
      | (e OR e)

The in-game doctrine editor does not show the parentheses around conjunction (``and``) and disjunction (``or``). Implicitly, conjunction and disjunction  are left-associative and have the same precedence.

This means, for example, that::

  e1 and e2 or e3    means    ((e1 AND e2) OR e3)

and also::

  e1 or e2 and e3    means    ((e1 OR e2) AND e3)

Trigger
^^^^^^^

::

  i ::= IF e THEN TRIGGERFIRED END.


Composing Triggers
------------------