WHAT THIS FOLDER IS

The reference solution for this task (solution/solve.sh) starts by unpacking
solution/regress_restore.tar.b64, a base64-encoded tar archive, over /app. Only after that
does it apply the actual fix. This folder shows what that first step does, decoded:

  restore.diff   what the archive changes, as a diff from the starting code the
                 models were given (codebase/ in this zip) to the files it writes
  files/         the files in the archive, as they are written under /app

The archive is empty: this step changes nothing.

The restore is not part of the fix. It puts back the version of the starting code
that the rest of the reference solution was written against; the task's starting
code (what the models saw) differs from it. The models were not given this archive.
