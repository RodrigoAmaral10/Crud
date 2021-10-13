object Form1: TForm1
  Left = 245
  Top = 192
  Width = 802
  Height = 462
  Caption = 'Form1'
  Color = clBtnFace
  Font.Charset = DEFAULT_CHARSET
  Font.Color = clWindowText
  Font.Height = -11
  Font.Name = 'MS Sans Serif'
  Font.Style = []
  OldCreateOrder = False
  PixelsPerInch = 96
  TextHeight = 13
  object grpInsert: TGroupBox
    Left = 0
    Top = 0
    Width = 786
    Height = 105
    Align = alTop
    Caption = 'Inserir pessoa'
    TabOrder = 0
    object lblNome: TLabel
      Left = 30
      Top = 23
      Width = 28
      Height = 13
      Caption = 'Nome'
    end
    object lblIdade: TLabel
      Left = 158
      Top = 26
      Width = 27
      Height = 13
      Caption = 'Idade'
    end
    object edtNome: TEdit
      Left = 29
      Top = 41
      Width = 121
      Height = 21
      TabOrder = 0
    end
    object btnInserir: TButton
      Left = 289
      Top = 36
      Width = 75
      Height = 25
      Caption = 'Inserir'
      TabOrder = 2
      OnClick = btnInserirClick
    end
    object edtIdade: TEdit
      Left = 158
      Top = 41
      Width = 121
      Height = 21
      TabOrder = 1
    end
  end
  object GroupBox1: TGroupBox
    Left = 0
    Top = 111
    Width = 786
    Height = 312
    Align = alBottom
    Caption = 'Select/Delete'
    TabOrder = 1
    object lblIdade2: TLabel
      Left = 491
      Top = 29
      Width = 27
      Height = 13
      Caption = 'Idade'
    end
    object DBGrid1: TDBGrid
      Left = 0
      Top = 75
      Width = 695
      Height = 235
      Align = alCustom
      DataSource = DataSource1
      TabOrder = 0
      TitleFont.Charset = DEFAULT_CHARSET
      TitleFont.Color = clWindowText
      TitleFont.Height = -11
      TitleFont.Name = 'MS Sans Serif'
      TitleFont.Style = []
    end
    object btnDeletar: TBitBtn
      Left = 698
      Top = 78
      Width = 75
      Height = 25
      Caption = 'Deletar'
      TabOrder = 1
      OnClick = btnDeletarClick
    end
    object btnTodos: TBitBtn
      Left = 14
      Top = 29
      Width = 109
      Height = 25
      Caption = 'Selecionar Todos'
      TabOrder = 2
      OnClick = btnTodosClick
    end
    object edtIdadeFiltro: TEdit
      Left = 525
      Top = 26
      Width = 121
      Height = 21
      TabOrder = 3
    end
    object btnSelecionarComFiltro: TButton
      Left = 652
      Top = 23
      Width = 126
      Height = 25
      Caption = 'btnSelecionarComFiltro'
      TabOrder = 4
      OnClick = btnSelecionarComFiltroClick
    end
    object BitBtn1: TBitBtn
      Left = 700
      Top = 113
      Width = 75
      Height = 25
      Caption = 'Limpar Filtro'
      TabOrder = 5
      OnClick = BitBtn1Click
    end
  end
  object UniConnection1: TUniConnection
    ProviderName = 'PostgreSQL'
    Port = 5432
    Database = 'BANCOHORA'
    Username = 'postgres'
    Password = '#abc123#'
    Server = 'localhost'
    LoginPrompt = False
    Left = 751
    Top = 20
  end
  object UniQuery1: TUniQuery
    Connection = UniConnection1
    UniDirectional = True
    Left = 721
    Top = 19
  end
  object PostgreSQLUniProvider1: TPostgreSQLUniProvider
    Left = 691
    Top = 19
  end
  object DataSource1: TDataSource
    DataSet = UniQuery1
    Left = 178
    Top = 193
  end
end
