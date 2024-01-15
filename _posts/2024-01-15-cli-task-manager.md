---
title: "CLI Task Manager using Go"
date: 2024-01-15
---

Today I decided to get my feet wet and try Go programming language. I took the idea from [Gophercises](https://github.com/gophercises/task) and decided to implement a CLI Task Manager App in Go. My hands on experience are with JavaScript, Python and C++, so I barely knew anything about Golang before I started.

All this app needs to do is insert a task into a database and delete a task from the database using CLI. As with anything new, I referred to the programming language's [documentation](https://go.dev/doc/) to start implementing.

To implement this app, I needed a database. I used sqlite3 since it is extremely easy to use. Fortunately all packages that Go provides can be found [here](https://pkg.go.dev/). I searched for "database", it returned packages for SQLite3, Postgres, MySQL etc. The second requirement was to find a package that helps with implementing a CLI app. The package that is used is [urfave/cli](https://pkg.go.dev/github.com/urfave/cli/v3). This package again provided with documentation that was super easy to read and understand.

With all this at hand I implemented the [CLI Task Manager](https://github.com/greeshma1196/cli-task-manager). This program does the following:

1. Creates a connection to the database
2. Once connection is established, it shows the user 3 options:
   1. Insert into the database
   2. Delete from the database
   3. Show the database

Et voila! It took me about 3 hours to implement and now I think I can program in Go!
