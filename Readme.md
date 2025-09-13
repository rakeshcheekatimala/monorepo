Using Symlinks for Local Development


 A symlink (symbolic link) is a special type of file that points to another file or directory. In Node.js projects, symlinks are commonly used to resolve local node_modules dependencies, allowing you to test and develop packages in a monorepo or across multiple projects without publishing them to a registry.

Benefits
Local Testing: Instantly test changes in shared modules without reinstalling or publishing.
Efficient Development: Streamline workflows by linking packages directly, reducing duplication and versioning issues.
Easy Collaboration: Share code between projects in a monorepo setup.

# How to Create a Symlink

You can use the npm link or yarn link command to create symlinks for local packages:

```
# In the package directory you want to link
npm link

# In the project where you want to use the linked package
npm link <package-name>
```

This will create a symbolic link in your node_modules folder, pointing to the local package.

# Example Workflow

Navigate to the package you want to share (e.g., module-a).
Run npm link to make it globally available.
In your main project or another module, run npm link module-a to use the local version.


![Symlink Example](symlink.png)

Takeaway: Symlink is system shortcut to file or directory (Symbolic link)