using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;
namespace Century_Plywood
{
 public partial class Loading_Page : Form
 {
 public Loading_Page()
 {
 InitializeComponent();
 }
 private void timer1_Tick(object sender, EventArgs e)
 {
 if (progressBar1.Value < 100)
 {
 progressBar1.Value = progressBar1.Value + 1;
label1.Text = "Loading... " + progressBar1.Value.ToString() 
+ " % ";
 }
 else
 {
 Loading_Page.ActiveForm.Hide();
 timer1.Enabled = false;
Welcome_Page frm = new Welcome_Page();
 frm.Show();
 }
 }
 
 }
}
