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
- Facebook: el código está implementado (`FacebookLogin.kt`, `AuthRepository.loginConFacebook`). Para activarlo se registra la app en Meta for Developers y se reemplazan `facebook_app_id`, `fb_login_protocol_scheme` y `facebook_client_token` en `strings.xml` (key hash de depuración: `ni2c12PrEqqeUKJydIR7JkSVpXU=`).
- OAuth App de GitHub con la URL de devolución de Firebase.
- `app/google-services.json` descargado después de activar Google.
