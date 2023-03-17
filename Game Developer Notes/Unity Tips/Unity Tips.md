# Unity Tips

### Unity Layouts:

* Layout of scene/game/ect can be saved as a **Layer** that can be used to change the layout at any time.
  
  ![](C:\Users\chest\OneDrive\Desktop\Unity%20Tips\Screenshots\2022-12-06-20-26-40-image.png)

* 

* 

* 

* 

* 

* 

## Grid

* **Zed Fighting:** The text and object trying to access the same coordinates, so when the camera attempts to render at certain angles one will hover the other (partially or fully) due to indecesive priority.
  
  * When working with TextMeshPro, adding the "Distance Field Overlay". This causes the text not to be obscured by other objects; it's essentially "always visible".

## Prefab

* Variant: Is essentially a "child prefab". Any changes made in the parent applies to the child unless explicitly overwritten by the child.
  
  * It is shown in Unity that a property is overwritten if it's in **bold**.

## Particle System:

* Collision:
  
  * Type
    
    * World - Affects world elements
      
      * Lifetime Loss: When collided, it will lose a give fraction of it's start lifetime. (Set to 1, it will die automatically)
    
    * Plane - Affects planes elements only 
  
  * Send Collision Messages
    
    * If left unchecked, the OnParticleCollision will not get the particle game object reference.

* Renderer:
  
  * Renderer Alignment:
    
    * Velocity: Particles face the direction they are moving.
