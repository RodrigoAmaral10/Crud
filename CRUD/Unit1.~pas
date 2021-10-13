unit Unit1;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, StdCtrls, Buttons, Grids, DBGrids, DB, MemDS, DBAccess, Uni,
  UniProvider, PostgreSQLUniProvider;

type
  TForm1 = class(TForm)
    btnInserir: TButton;
    edtNome: TEdit;
    edtIdade: TEdit;
    lblNome: TLabel;
    lblIdade: TLabel;
    grpInsert: TGroupBox;
    GroupBox1: TGroupBox;
    DBGrid1: TDBGrid;
    btnDeletar: TBitBtn;
    btnTodos: TBitBtn;
    edtIdadeFiltro: TEdit;
    btnSelecionarComFiltro: TButton;
    lblIdade2: TLabel;
    BitBtn1: TBitBtn;
    UniConnection1: TUniConnection;
    UniQuery1: TUniQuery;
    PostgreSQLUniProvider1: TPostgreSQLUniProvider;
    DataSource1: TDataSource;
    
    procedure btnInserirClick(Sender: TObject);
    procedure btnTodosClick(Sender: TObject);
    procedure btnSelecionarComFiltroClick(Sender: TObject);
    procedure BitBtn1Click(Sender: TObject);
    procedure btnDeletarClick(Sender: TObject);
  private
    procedure LimpaGrid;
    procedure SelecionarTodos;
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form1: TForm1;

implementation

{$R *.dfm}

procedure TForm1.btnInserirClick(Sender: TObject);
begin
  LimpaGrid();

  UniQuery1.SQL.ADD(Format('insert into public."Pessoa" ("Nome", "Idade") values (%s, %s)', [QuotedStr(edtNome.Text), edtIdade.Text]));
  UniQuery1.ExecSQL;

  if UniQuery1.active then
    showmessage('ativo!!!');

  if edtNome.CanFocus then
    edtNome.SetFocus;  
end;

procedure TForm1.SelecionarTodos();
begin
  LimpaGrid();

  UniQuery1.SQL.ADD('select * from public."Pessoa"');
  UniQuery1.Open;
end;

procedure TForm1.btnTodosClick(Sender: TObject);
begin
  SelecionarTodos();
end;

procedure TForm1.btnSelecionarComFiltroClick(Sender: TObject);
begin
  LimpaGrid();

  UniQuery1.SQL.ADD(Format('select * from public."Pessoa" where "Idade" = %s', [edtIdadeFiltro.Text]));
  UniQuery1.Open;
end;

procedure TForm1.BitBtn1Click(Sender: TObject);
begin
  LimpaGrid();
end;

procedure TForm1.LimpaGrid();
begin
  UniQuery1.SQL.Text := '';

  if UniQuery1.Active then
    UniQuery1.Close;
end;

procedure TForm1.btnDeletarClick(Sender: TObject);
var
  lQuery: TUniQuery;
begin
  lQuery := TUniQuery.Create(nil);
  lQuery.Connection := UniConnection1;

  lQuery.SQL.ADD(Format('delete from public."Pessoa" where "Id" = %d', [UniQuery1.Fields.FieldByName('id').AsInteger]));
  lQuery.ExecSQL;

  lQuery.Free;

  SelecionarTodos();
end;

end.
