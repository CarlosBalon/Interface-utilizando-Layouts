import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.scene.Scene;
import javafx.scene.control.Label;
import javafx.scene.control.ListView;
import javafx.scene.control.ScrollPane;
import javafx.scene.control.TextField;
import javafx.scene.image.Image;
import javafx.scene.image.ImageView;
import javafx.scene.layout.AnchorPane;
import javafx.scene.layout.BorderPane;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class InterfazGrafica extends Application {

    @Override
    public void start(Stage primaryStage) {
        BorderPane root = new BorderPane();
        root.setPadding(new Insets(10));

        // VBox para el lado izquierdo
        VBox leftBox = new VBox(10);
        leftBox.setPadding(new Insets(10));

        // Agregar las imágenes con etiquetas y campos de texto
        for (int i = 1; i <= 5; i++) {
            ImageView imageView = new ImageView(new Image("imagen" + i + ".png"));
            Label nameLabel = new Label("Nombre:");
            Label lastNameLabel = new Label("Apellido:");
            TextField nameTextField = new TextField();
            TextField lastNameTextField = new TextField();

            leftBox.getChildren().addAll(imageView, nameLabel, nameTextField, lastNameLabel, lastNameTextField);
        }

        // ScrollPane para el VBox izquierdo (opcional)
        ScrollPane scrollPane = new ScrollPane(leftBox);
        scrollPane.setFitToWidth(true);

        // ListView en el lado derecho
        ListView<String> listView = new ListView<>();

        // TextField debajo de la ListView
        TextField textField = new TextField();

        // AnchorPane alrededor del TextField
        AnchorPane anchorPane = new AnchorPane();
        anchorPane.setStyle("-fx-background-color: yellow;");
        AnchorPane.setTopAnchor(textField, 10.0);
        AnchorPane.setRightAnchor(textField, 10.0);
        AnchorPane.setBottomAnchor(textField, 10.0);
        AnchorPane.setLeftAnchor(textField, 10.0);
        anchorPane.getChildren().add(textField);

        // Agregar los componentes al BorderPane
        root.setLeft(scrollPane);
        root.setRight(listView);
        root.setBottom(anchorPane);

        Scene scene = new Scene(root, 800, 600);
        primaryStage.setScene(scene);
        primaryStage.setTitle("Interfaz Gráfica");
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
