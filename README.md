# login

package com.example.jane.loginregister;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;

public class Login extends AppCompatActivity implements View.OnClickListener {

    android.widget.Button bLogin;
    android.widget.EditText etUsername, etPassword;
    android.widget.TextView tvRegisterlink;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_login);

        etUsername = (android.widget.EditText) findViewById(R.id.etUsername);
        etPassword = (android.widget.EditText) findViewById(R.id.etPassword);
        bLogin = (android.widget.Button) findViewById(R.id.bLogin);
        tvRegisterlink = (android.widget.TextView) findViewById(R.id.tvRegisterlink);

        bLogin.setOnClickListener(this);
        tvRegisterlink.setOnClickListener(this);
    }

    @Override
    public void onClick(View v) {
        switch(v.getId()){
            case R.id.bLogin:



                break;

            case R.id.tvRegisterlink:

                startActivity(new android.content.Intent(this, Register.class));

                break;
        }
    }
}
