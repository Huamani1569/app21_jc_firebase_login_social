# App21 · Login con correo, Google, Facebook y GitHub (Firebase Auth)

**Desarrollo de Aplicaciones Móviles · Semana 10 · Universidad Continental**  
Autor: Jean Piero Huamani Rodriguez

Inicio de sesión con **correo y contraseña** (registro, verificación de correo y recuperación de contraseña) y con **Google** (Credential Manager), **Facebook** (SDK de Meta) y **GitHub** (OAuth de Firebase), con pantalla de perfil. Arquitectura **MVVM** en Jetpack Compose.

## Estructura
| Capa | Archivos |
|---|---|
| Model | `Usuario.kt`, `AuthRepository.kt` (Firebase Auth + Credential Manager + Meta + OAuthProvider, `AuthStateListener` con `callbackFlow`) |
| ViewModel | `AuthUiState.kt`, `AuthViewModel.kt` (validación y traducción de errores) |
| View | `NavegacionApp`, `LoginScreen`, `FormularioCorreo`, `BotonProveedor`, `FacebookLogin`, `Mensaje`, `HomeScreen` |

## Configuración
- Firebase Authentication: Correo/contraseña, Google, Facebook y GitHub activados.
- Huella **SHA-1** del certificado de depuración registrada en Firebase.
- App de Meta for Developers (ID y token de cliente en `strings.xml`, key hash registrado).
- OAuth App de GitHub con la URL de devolución de Firebase.
- `app/google-services.json` descargado después de activar Google.
