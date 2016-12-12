# WinForms Questions

`C#` と `VB` で回答が可能です。

かなり難しそうと思われる問題でも、既存のコントロールを有効活用することで解決できる問題が大半になっております。

よろしければ挑戦してみてください。

## 問題例および回答例

### 問題例
フォームにボタンを配置し、そのボタンをクリックしたらメッセージボックスで`Hello, World!`と表示するプログラムを作成せよ。


### 回答例　（C#）
```csharp
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WinFormsQuestions {
  public partial class test : Form {
    public test() {
      InitializeComponent();
    }

    private void button1_Click(object sender, EventArgs e) {
      MessageBox.Show("Hello, World!");
    }
  }
}
```

```csharp
namespace WinFormsQuestions {
  partial class test {
    /// <summary>
    /// Required designer variable.
    /// </summary>
    private System.ComponentModel.IContainer components = null;

    /// <summary>
    /// Clean up any resources being used.
    /// </summary>
    /// <param name="disposing">true if managed resources should be disposed; otherwise, false.</param>
    protected override void Dispose(bool disposing) {
      if (disposing && (components != null)) {
        components.Dispose();
      }
      base.Dispose(disposing);
    }

    #region Windows Form Designer generated code

    /// <summary>
    /// Required method for Designer support - do not modify
    /// the contents of this method with the code editor.
    /// </summary>
    private void InitializeComponent() {
      this.button1 = new System.Windows.Forms.Button();
      this.SuspendLayout();
      // 
      // button1
      // 
      this.button1.Location = new System.Drawing.Point(92, 68);
      this.button1.Name = "button1";
      this.button1.Size = new System.Drawing.Size(75, 23);
      this.button1.TabIndex = 0;
      this.button1.Text = "button1";
      this.button1.UseVisualStyleBackColor = true;
      this.button1.Click += new System.EventHandler(this.button1_Click);
      // 
      // test
      // 
      this.AutoScaleDimensions = new System.Drawing.SizeF(6F, 12F);
      this.AutoScaleMode = System.Windows.Forms.AutoScaleMode.Font;
      this.ClientSize = new System.Drawing.Size(284, 261);
      this.Controls.Add(this.button1);
      this.Name = "test";
      this.Text = "test";
      this.ResumeLayout(false);

    }

    #endregion

    private System.Windows.Forms.Button button1;
  }
}
```

ファイル名・フォーム名を自分のユーザー名にし、`クラス名.cs`・`クラス名.Designer.cs`の２つのファイルをご提出ください。