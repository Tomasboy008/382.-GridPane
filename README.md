# 382.-GridPane
Construção de um grid, legal para fazer um campo minado.
public class TesteGridPane extends GridPane {
	
	public TesteGridPane() {
	
		Caixa c1 = new Caixa().comTexto("1");
		Caixa c2 = new Caixa().comTexto("2");
		Caixa c3 = new Caixa().comTexto("3");
		Caixa c4 = new Caixa().comTexto("4");
		Caixa c5 = new Caixa().comTexto("5");
		Caixa c6 = new Caixa().comTexto("6");
		
		setGridLinesVisible(true); // comando q faz aparecer as linhas pretas
		
		getColumnConstraints().addAll(cc(), cc(), cc(), cc(), cc());
		getRowConstraints().addAll(rc(), rc(), rc(), rc(), rc());
		
		setVgap(10);//espacamento entre as linhas pretas
		setHgap(10);
		
		add(c1, 0, 0, 2, 2);
		add(c2, 1, 1, 2, 2);
		add(c3, 4, 2, 1, 3);
		add(c4, 3, 1);
		add(c5, 0, 4, 2, 1);
		add(c6, 3, 3);
	}
	public ColumnConstraints cc() {
		ColumnConstraints cc = new ColumnConstraints();
		cc.setPercentWidth(20);
		cc.setFillWidth(true);
		return cc;		
	}
	public RowConstraints rc() {
		RowConstraints cc = new RowConstraints();
		cc.setPercentHeight(20);
		cc.setFillHeight(true);
		return cc;	
	}
}

![image](https://user-images.githubusercontent.com/95525963/153512065-367bcfce-6532-4388-a170-686a900babda.png)

