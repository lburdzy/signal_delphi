unit Unit1;

{$mode objfpc}{$H+}

interface

uses
  Classes, SysUtils, FileUtil, Forms, Controls, Graphics, Dialogs, StdCtrls,
  ExtCtrls;

type

  { TForm1 }

  TForm1 = class(TForm)
    Button1: TButton;
    Edit1: TEdit;
    Label1: TLabel;
    Shape1: TShape;
    Shape2: TShape;
    Shape3: TShape;
    Shape4: TShape;
    Timer1: TTimer;
    Timer2: TTimer;
    procedure Button1Click(Sender: TObject);
    procedure Timer1Timer(Sender: TObject);
    procedure Timer2Timer(Sender: TObject);
    procedure zapal;
  private
    { private declarations }
  public
    { public declarations }
    var state:Integer;
  end;

var
  Form1: TForm1;

implementation

{$R *.lfm}

{ TForm1 }

procedure TForm1.Button1Click(Sender: TObject);
begin

  {state:=(state+1)mod 4;
  Edit1.Text:=IntToStr(state);
  zapal;  }
  Timer1.Enabled:=True;


end;


procedure TForm1.Timer1Timer(Sender: TObject);
begin
  zapal;
  Edit1.Text:=IntToStr(state);
  state:=(state+1)mod 4;
  Timer1.Enabled:=False;
  Timer2.Enabled:=True;
end;



procedure TForm1.Timer2Timer(Sender: TObject);
begin
  zapal;
  Edit1.Text:=IntToStr(state);
  state:=(state+1)mod 4;
  Timer2.Enabled:=False;
  Timer1.Enabled:=True;
end;

procedure TForm1.zapal;
begin
  case state of
    0:
      begin
        Shape1.Brush.Color:=clRed;
        Shape2.Brush.Color:=$00333333;
      end;
    1:
      begin
        Shape2.Brush.Color:=clYellow;
      end;
    2:
      begin
        Shape1.Brush.Color:=$00333333;
        Shape2.Brush.Color:=$00333333;
        Shape3.Brush.Color:=clGreen;
      end;
    3:
      begin
        Shape3.Brush.Color:=$00333333;
        Shape2.Brush.Color:=clYellow;
      end;



end;
end;

end.

