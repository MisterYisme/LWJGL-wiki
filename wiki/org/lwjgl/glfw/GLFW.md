# GLFW - Graphics Library FrameWork
```java
import org.lwjgl.glfw.*;
```
## Window Management

### glfwInit()
Initializes GLFW
#### Example
```java
if (!glfwInit()) {
    // Handle initialization failure
    throw new IllegalStateException("Unable to initialize GLFW");
}
```
#### Usage
To Initialize the majority of the GLFW Library. for example glfwCreateWindow needs it to work
#### Relations
calls [glfwTerminate()](#glfwterminate) on fail
#### [Original Documentation](https://www.glfw.org/docs/latest/group__init.html#ga317aac130a235ab08c6db0834907d85e)

### glfwTerminate()
[!WARNING] Missing Description
#### Example
```java
{
    // Your window code
} finally {
    glfwTerminate();
}
```
#### Usage
To close and destroy the GLFW session
#### [Original Documentation](https://www.glfw.org/docs/latest/group__init.html#gaaae48c0a18607ea4a4ba951d939f0901)

### glfwDefaultWindowHints()
This function resets all window hints to their default values. 

Overrides all earlier [glfwWindowHint](#glfwwindowhintint-hint-int-value) calls
#### Example
```java
glfwDefaultWindowHints();
// Window Creation
```
#### Usage
To reset or initially set the window hints to their default values
#### [Original Documentation](https://www.glfw.org/docs/latest/group__window.html#gaa77c4898dfb83344a6b4f76aa16b9a4a)

### glfwWindowHint(int hint, int value)
[!WARNING] Missing Description
#### Example
```java
glfwWindowHint(GLFW_VISIBLE, GLFW_TRUE);
// Window Creation
```
#### Usage
glfwWindowHint() configures how the next window will be created. Use it before calling glfwCreateWindow() to specify properties such as visibility, resizability, OpenGL version and fullscreen-related behavior.
#### [Original Ducumentation](https://www.glfw.org/docs/latest/group__window.html#ga7d9c8c62384b1e2821c4dc48952d2033)

### glfwCreateWindow(int width, int height, String title, long monitorHandle, )
Creates a window and its OpenGL or OpenGL ES context, and returns a handle to the created window object.
#### Example
This creates a 640 by 480 windowed mode window:
```java
// Try to make a MemoryStack for the title of the screen
try (MemoryStack stack = MemoryStack.stackPush()) {
    // Convert the title from UTF8 to ByteBuffer
    ByteBuffer title = stack.UTF8("Title");
    // Create window at size 640*280 (width * height) with the title: "Title" in windowed mode (1st 0L), without shared resources (2nd 0L)
    long window = glfwCreateWindow(640, 280, title, 0L, 0L);

    // Your code
}
```
#### Usage
To create a window that an application can render graphics into and recieve user imput through
#### [Orginal Documentation](https://www.glfw.org/docs/latest/group__window.html#ga3555a418df92ad53f917597fe2f64aeb)

### glfwDestroyWindow(long windowHandle)
[!WARNING] TODO: fill out Example, Usage
### glfwWindowShouldClose(long windowHandle)
[!WARNING] TODO: fill out Example, Usage
### glfwSetWindowShouldClose(long windowHandle, boolean value)
[!WARNING] TODO: fill out Example, Usage
### glfwPollEvents()
[!WARNING] TODO: fill out Example, Usage
### glfwWaitEvents()
[!WARNING] TODO: fill out Example, Usage
### glfwSwapBuffers(long windowHandle)
[!WARNING] TODO: fill out Example, Usage
### glfwMakeContextCurrent(long windowHandle)
[!WARNING] TODO: fill out Example, Usage
### glfwSwapInterval(int interval)
[!WARNING] TODO: fill out Example, Usage
### glfwSetWindowTitle(long windowHandle, CharSequence title)
[!WARNING] TODO: fill out Example, Usage
### glfwGetWindowSize(...)
[!WARNING] TODO: fill out Example, Usage
### glfwSetWindowSize(...)
[!WARNING] TODO: fill out Example, Usage
### glfwGetFramebufferSize(...)
[!WARNING] TODO: fill out Example, Usage
### glfwGetWindowPos(...)
[!WARNING] TODO: fill out Example, Usage
### glfwSetWindowPos(...)
[!WARNING] TODO: fill out Example, Usage
### glfwMaximizeWindow(long windowHandle)
[!WARNING] TODO: fill out Example, Usage
### glfwIconifyWindow(long windowHandle)
[!WARNING] TODO: fill out Example, Usage
### glfwRestoreWindow(long windowHandle)
[!WARNING] TODO: fill out Example, Usage
### glfwSetWindowMonitor(...)
[!WARNING] TODO: fill out Example, Usage
### glfwGetPrimaryMonitor()
[!WARNING] TODO: fill out Example, Usage
### glfwGetVideoMode(long monitorHandle)
[!WARNING] TODO: fill out Example, Usage
### glfwSetWindowSizeCallback(...)
[!WARNING] TODO: fill out Example, Usage
### glfwSetFramebufferSizeCallback(...)
[!WARNING] TODO: fill out Example, Usage
### glfwSetWindowCloseCallback(...)
[!WARNING] TODO: fill out Example, Usage
### glfwSetWindowFocusCallback(...)
[!WARNING] TODO: fill out Example, Usage
### glfwSetWindowPosCallback(...)
[!WARNING] TODO: fill out Example, Usage

---