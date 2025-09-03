# Exp02-RollABall
### Name : SUDHIR KUMAR. R
### Reg No. : 212223230221
## Aim:
 To develop a 3D application to roll a ball in unity

## Algorithm:
1. File -> Scene -> Select the scene -> Save as-> New folder(Scenes)-> File name (MiniGame)
2. Heirarchy -> 3D Object-> Plane [ Right side-> Inspector-> Change the name of plane (Name: Ground) ,Transform -> Reset ,Edit -> FrameSelected ]
3. Scale the ground by giving the scaling value as x=4 y=1 z=4
4. Heirarchy -> 3D Object-> Sphere [ Right side-> Inspector-> Change the name of plane (Name: Player) Transform -> Reset , Edit -> FrameSelected, Transform -> Position -> y=0.5]
5. Hierarchy -> DirectionalLight [ Inspector -> Change the color to white (255,255,255)]
6. Create a folder in project and name as Materials [Material folder -> Create -> Material (Name: Background) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Metallic map-> 0, Smoothness -> 0.25, Drag the Background to the plane and release the mouseMaterial folder -> Create -> Material (Name: Sphere) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Metallic map-> 0,Smoothness -> 0.75,Drag the Sphere material to the ball and release the mouse
7. Hierarchy -> Player-> Inspector ->Add component-> Rigidbody
8. Create a new script -> Create a folder in project (Name: Scripts) Hierarchy -> Player -> Inspector-> AddComponent-> NewScripts-> PlayerController( Click create and Add), Copy the PlayerController and drag to Script folder, Double click the PlayerController file and type the coding

## Program:
```
using UnityEngine;
using System.Collections;
using System.Security.Cryptography.X509Certificates;
using UnityEditor.SceneManagement;

public class NewMonoBehaviourScript : MonoBehaviour
{
    public float xForce = 5.0f;
    public float yForce = 100.0f;
    public float zForce = 5.0f;
    void Start()
    {
        
    }
    void Update()
    {
        float x=0.0f , y=0.0f ,z=0.0f;
        if (Input.GetKey(KeyCode.A))
        {
            x = x - xForce;
        }
        if (Input.GetKey(KeyCode.D))
        {
            x += xForce;
        }
        if (Input.GetKey(KeyCode.W))
        {
            z = z - zForce;
        }
        if (Input.GetKey(KeyCode.S))
        {
            y += zForce;
        }
        if (Input.GetKey(KeyCode.Space))
        {
            y = yForce;
        }
        GetComponent<Rigidbody>().AddForce(x, y, z);
    }
}
```
## Output:

<img width="1919" height="1079" alt="Screenshot 2025-09-03 110225" src="https://github.com/user-attachments/assets/25a542ea-a7b7-4785-8fc1-1d0468715b20" />

## Result:
Thus the 3D application to roll a ball in unity was successfully executed. 
