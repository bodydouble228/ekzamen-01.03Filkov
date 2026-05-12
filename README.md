# ekzamen-01.03Filkov
экзамен 01.03 филков варик 8
Вариант №8
Задание: Кнопка «Сгенерировать» и текст, отображающий случайное число от 1 до 100. При каждом нажатии число меняется. Добавьте кнопку «Сброс», которая возвращает текст в состояние «Нажмите кнопку».  
  
    package com.example.Filkov
    import android.os.Bundle
    import androidx.activity.ComponentActivity
    import androidx.activity.compose.setContent
    import androidx.compose.foundation.layout.*
    import androidx.compose.material3.*
    import androidx.compose.runtime.*
    import androidx.compose.ui.Alignment
    import androidx.compose.ui.Modifier
    import androidx.compose.ui.unit.dp
    import kotlin.random.Random

    class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        setContent {
            var text by remember { mutableStateOf("Нажмите кнопку") }

            Column(
                modifier = Modifier.fillMaxSize(),
                verticalArrangement = Arrangement.Center,
                horizontalAlignment = Alignment.CenterHorizontally
            ) {

                Text(text = text)

                Spacer(modifier = Modifier.height(16.dp))

                Button(onClick = {
                    text = Random.nextInt(1, 101).toString()
                }) {
                    Text("Сгенерировать")
                }

                Spacer(modifier = Modifier.height(8.dp))

                Button(onClick = {
                    text = "Нажмите кнопку"
                }) {
                    Text("Сброс")
                }
            }
        }
    }
    }
<img width="404" height="876" alt="global_menu" src="https://github.com/user-attachments/assets/c83d8dbc-813e-4a3c-aa0d-2fdfc3a070e6" />
 <img width="382" height="834" alt="ekz2" src="https://github.com/user-attachments/assets/90c966fe-f401-4577-9d1f-ea486ebdba8b" />
 <img width="378" height="828" alt="second_generate3" src="https://github.com/user-attachments/assets/b60035c3-2913-4141-8a92-9b318fa498f5" />
<img width="383" height="831" alt="Reset4" src="https://github.com/user-attachments/assets/8740c1fd-c939-4350-b521-5b064273098d" />

