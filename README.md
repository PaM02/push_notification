tout d'abord aller sur ce site : https://firebase.flutter.dev/docs/messaging/overview/
ajouter les dependances suivant:
flutter pub add firebase_messaging
flutter pub add firebase_core
# Install the CLI if not already done so
dart pub global activate flutterfire_cli
# Run the `configure` command, select a Firebase project and platforms
flutterfire configure ;choisi le ptojet corespondand

lib/main.dart
import 'package:firebase_core/firebase_core.dart';
import 'firebase_options.dart';

lib/main.dart
void main() async {
WidgetsFlutterBinding.ensureInitialized();
await Firebase.initializeApp(
options: DefaultFirebaseOptions.currentPlatform,
);
runApp(MyApp());
}
