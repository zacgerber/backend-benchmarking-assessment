<img height="120px" src="https://hackernoon.com/hn-images/1*U8AZbgD9wqF1IgVbOWlocg.png">

# Benchmarking (aka "I don't have time for this")

Imagine that you've been working on this program on a team of developers. You've
done all the right things up until now, including writing [unittests](tests/test_anagrams.py).

Unfortunately, a previous teammate not only committed code that made the benchmarking tests fail, but they force-pushed to master after rewriting history, so you can't simply go back in the git history to fix things. Especially since, in the process of ruining the timings, the developer _did_ manage to implement features that weren't there before.

Your task is to modify [anagrams.py](anagrams.py) such that the tests pass again. If the problem isn't obvious to you by visually examining the `anagrams.py` module, consider using the profiling techniques that you learned about in the lesson to pin down the problem. Using a debugger may also help you to get a handle on exactly _why_ things are slow.

## Skipped unit test
If you look at the test case, you'll notice that the `test_long` unit test is currently being skipped. That's because if it were to run with the current implementation of `find_anagrams` it would take several minutes to complete. We suggest that you try and get the `test_short` to pass first, then remove the `@unittest.skip` line and ensure that the tests still pass.

## Testing
You can run the tests from the command line with the unittest framework. From the top level directory of the assignment, use the following command:
```console
$ python -m unittest discover
```

VSCode also has a built-in test discovery feature, but it requires you to enable test discovery in the settings.  Read this article for more information about how to configure VSCode for automatic test discovery.

https://code.visualstudio.com/docs/python/testing#_test-discovery

Be sure to select the configuration for `unittest`, not nosetest or pytest because these are third-party libraries that you would have to install.  The file discovery pattern to configure is `test_*.py`


## PR (Pull Request) Workflow for this Assignment
1. *Fork* this repository into your own personal github account.
2. Then *Clone* your own repo to your local development machine.
3. Create a separate branch named `dev`, and checkout the branch.
5. Commit your changes, then `git push` the branch back to your own github account.
5. From your own Github repo, create a pull request (PR) from your `dev` branch back to your own master.
6. Copy/Paste the URL **link to your PR** as your assignment submission.
7. Your grader will post code review comments inline with your code, in your github account. Be sure to respond to any comments and make requested changes. **RESUBMIT** a new link to your PR after making changes.  This is the code review iteration cycle.
