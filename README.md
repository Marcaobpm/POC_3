# POC_3
#POC_3

#Explicação MediaQueries
1.
Para aplicar estilos específicos quando o documento é impresso, usamos a media query @media print. Isso é útil para ocultar elementos que não são necessários em uma impressão, como menus e outros elementos de navegação.

@media print {
    header, footer {
        display: none;
    }
    main {
        -webkit-print-color-adjust: exact;
    }
}
2. Larguras de Dispositivos Diferentes
As media queries podem ser utilizadas para adaptar o layout com base na largura da tela do dispositivo. Vamos definir três faixas: smartphones, tablets e desktops.
@media (max-width: 600px) {
    nav ul {
        text-align: center;
        display: block;
    }

    .image-grid {
        grid-template-columns: 1fr;
    }

    .content {
        font-size: 0.9rem;
    }
}
@media (min-width: 601px) and (max-width: 900px) {
    .image-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .content {
        font-size: 1rem;
    }
}

@media (min-width: 901px) {
    .image-grid {
        grid-template-columns: repeat(4, 1fr);
    }

    .content {
        font-size: 1.1rem;
        column-count: 2;
    }

3. Disposição dos Dispositivos (Landscape e Portrait)
A orientação da tela pode ser verificada usando orientation. Isso é útil para aplicar estilos específicos dependendo se o dispositivo está em modo retrato (portrait) ou paisagem (landscape).

@media (orientation: landscape) {
    header {
        font-size: 1.5rem;
    }
}

![image](https://github.com/user-attachments/assets/74fe9e04-9443-43af-a8c0-0f5054304364)
![image](https://github.com/user-attachments/assets/326638e8-7945-467a-9c42-0dd5c47b0320)

[CodePoc3.zip](https://github.com/user-attachments/files/17167403/CodePoc3.zip)
