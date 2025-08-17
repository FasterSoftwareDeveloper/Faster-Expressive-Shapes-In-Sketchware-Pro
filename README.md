# 🎨 Faster Expressive Shapes

[![Watch the video](https://raw.githubusercontent.com/FasterSoftwareDeveloper/Faster-Expressive-Shapes-In-Sketchware-Pro/refs/heads/main/thumbnail.png)](https://youtu.be/sQeww8KHmU4)

> A Material 3–style **expressive shape morphing view** for Android.  
> Built with ❤️ by Faster Software Developer

---

## ✨ Key Features
- 🔄 Child view clipping & morphing between **35 built-in expressive shapes**  
- 🎬 Material 3–inspired some animation style
- 🎨 Customizable: color, stroke, fill, duration  
- 🛠️ Easy integration into any Android project  
- ⚡ Lightweight & dependency-free (only standard Android + Material library)  
- 📱 Works with Sketchware Pro, Android Studio, or any Gradle project  

---

## 📦 Setup

Add the class `FasterExpressiveShapes.java` to your project.  
No extra Gradle dependencies required beyond Material Components:

```

implementation "com.google.android.material\:material:1.14.0-alpha03"

```

---

## 🚀 Usage

### 1. Add in Layout XML
```

<yt.material3.faster.FasterExpressiveShapes
    android:id="@+id/expressiveShape"
    android:layout_width="200dp"
    android:layout_height="200dp"
    android:layout_gravity="center" />

```

### 2. Setup in Java
```

FasterExpressiveShapes shapeView = findViewById(R.id.expressiveShape);

// Fill color from theme
shapeView.setFillColorFromTheme();

// Set built-in shape
shapeView.setShapeByName("pill");

// Pulse animation
shapeView.setPulseAnimation(true, 0.85f, 0.95f, 1000);

// Rotation animation
shapeView.setRotationAnimation(45f);

// Register any custom shape and set it
shapeView.registerShape("cloud", "M19.35 10.04A7.49 7.49 0 0 0 12 4C9.11 4 6.6 5.64 5.35 8.04A5.994 5.994 0 0 0 0 14c0 3.31 2.69 6 6 6h13c2.76 0 5-2.24 5-5c0-2.64-2.05-4.78-4.65-4.96z");
shapeView.setShapeByName("cloud");

// Fill color manually
shapeView.setFillColor(0xFFFF5722);

// Animate fill color with theme attributes
shapeView.animateFillColorAttr(R.attr.colorPrimaryContainer, R.attr.colorSecondary, 800);

// Comfortable color animation
shapeView.animateColorsComfortably(
    Arrays.asList(R.attr.colorPrimaryContainer, R.attr.colorSecondary, R.attr.colorTertiary),
    2000,
    500,
    false
);

// Comfortable color animation with continuous looping
shapeView.animateColorsComfortably(
    Arrays.asList(R.attr.colorPrimaryContainer, R.attr.colorSecondary, R.attr.colorTertiary),
    2000,
    500,
    true
);

// Instantly morph to a shape
shapeView.morphToShape("cookie12", 0);

// Morph through a sequence of shapes
shapeView.startMorphSequence(
    Arrays.asList("cookie4", "cookie9", "pill", "triangle", "circle"),
    2000
);

```

---

## 🧩 Built-in Shapes (35)

`circle, square, slanted, arch, semicircle, oval, pill, triangle, arrow, fan, diamond, clamshell, pentagon, gem, verysunny, sunny, cookie4, cookie6, cookie7, cookie9, cookie12, clover4, clover8, burst, softburst, boom, softboom, flower, puffy, puffydiamond, ghost, pixelcircle, pixeltriangle, bun, heart`

---

## 📜 License

**Open & Free (No Restrictions):**  
This project is released as **CC0 1.0 Universal**.  
You are free to use, modify, and share it for any purpose, including commercial projects—no attribution required, no restrictions.

**Third-Party Libraries:**  
This project may include third-party libraries. Each library is subject to its own license. Please review their licenses if you plan to use them.

---
⭐ **If you like this project, please star the repo — it motivates me to build more!** 
