# KdvHesaplama
Android KDV hesaplama
package com.example.kdvhesaplama;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.text.Editable;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
EditText txtFiyat , txtKdv;
Button btnHesapla;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        txtFiyat = findViewById(R.id.txtFiyat);
        txtKdv = findViewById(R.id.txtKdv);
        btnHesapla = findViewById(R.id.btnHesapla);
    }
    public void calculate(View view){
        int kdv;
        kdv = Integer.parseInt(txtKdv.getText().toString());
        int fiyat;
        fiyat = Integer.parseInt(txtFiyat.getText().toString());
        int toplam;
        toplam = fiyat  + (fiyat*kdv/100);
        Toast.makeText(this , "Toplam : " + toplam + "₺ " , Toast.LENGTH_SHORT).show();
    }
}
