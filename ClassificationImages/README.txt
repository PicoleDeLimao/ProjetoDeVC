Este programa tem a finalidade de receber o recorte de uma imagem retornar um número que identifica a classe de expressão (0- Tristeza, 1-Alegria, 2-Raiva) que a imagem de face foi  classificada.

Para retornar o número da classe, é preciso apenas chamar o método getClassLabelImage(Mat, model) da classe ClassifiesFacialExpression(Mat) passando o recorte de face carregada em um Mat. Este model, refere-se ao modelo que já está carregado, então no início da aplicação, o método
 loadsFile() deve ser chamado, ele retorna uma estrutura que guarda o modelo carregado.

Para utilizar o modelo cv_lbp_model_1_4_4_4.yaml, gerado após realizar validação cruzada, as imagens devem ser redimensionadas para 48 x 48 (Ver parâmetros no construtor da classe ClassifiesFacialExpression).
Para utilizar o modelo sem validação cruzada: t4_lbp_model_2_8_8_8.yaml, as imagens devem ser redimensionadas para 96x96 (Ver parâmero no construtor da classe ClassifiesFacialExpression).

Observação: Não esquecer de preprocessar a imagem, no método getClassLabelImage tem alguns comentários. 
