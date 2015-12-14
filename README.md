// company login
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="CompanyLoginPage.aspx.cs" Inherits="MeetApplication.CompanyPages.CompanyLoginPage" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
   <style>
        .text{
            color:#f1ad7c;
        }
        .login{     /******bu bir div; bu divi ortala!!! ve kutulayıp arkasını beyaz yap!!!*/
            display:block;
            width: 600px;
            height: 300px;
            padding: 20px;
            background-color: white;
        }
        body {
            background-color:#f8e3e3;
    font-family: Verdana, monospace, sans-serif;
    font-size: 12px;
    font-weight: bold;
    
}
        .pic img{
            width:100px;
            height:300px;
        }
    </style>
</head>
<body>
    <form id="form1" runat="server">
    <div  >
     <table id="login">
         <tr>
             <td>
                 <img src="/ForUser/pictures/beyazlogo.png" style="height: 133px; width: 154px;" />
             </td>             
         </tr>
         <tr><td colspan="3" id="text"> Restoran Kontrol Sayfası - Kullanıcı Girişi</td></tr>
 

            <tr>
                <td>Email Adresi</td>
                <td> : </td>
                <td>
                    <asp:TextBox ID="txtEmailAdres" runat="server" />
                </td>
               
            </tr>
            <tr>
                <td>Şifre</td>
                <td> : </td>
                <td>
                    <asp:TextBox ID="txtSifre" runat="server" />
                </td>
               
            </tr>
         <tr>
             <td colspan="4">
                 <asp:Button Text="Giriş Yap" ID="btnGiris" onclick="btnGiris_Click" runat="server" />
             </td>
         </tr>
         
           
         
         </table>
    </div>
    </form>
</body>
</html>>

//company Home page
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="CompanyHomePage.aspx.cs" Inherits="MeetApplication.ForCompany.CompanyHomePage" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
</head>
<body>
    <form id="form1" runat="server">
             <div>
                 <img src="/ForUser/pictures/beyazlogo.png" style="height: 133px; width: 154px;" />
             </div>
     
            <div>
               <div>
                        <table style="width:100%">
                            <tr>
                              
                                <td>Kategori  ID</td>
                                <td>Kategori Adı</td>
                                <td>Ürün Adı</td>
                                <td>Ürün Boyutu</td>
                                <td>Ürün Fiyatı</td>
                            </tr>
                            <asp:Repeater ID="rptUrunler" runat="server">
                                <ItemTemplate>
                            <tr>

                    
                   
                     </tr>
                                      </ItemTemplate>
                            </asp:Repeater>        
                   

               </table>
            </div>
            </div>
           
            <div id="dvIletisim">
                <table>
                    <tr>
                        <td colspan="2" > <h2>Mail Formu</h2> </td>
                    </tr>
                    <tr>
                        <td>Email : </td>

                        <td>
                            <asp:TextBox runat="server" Width="200" ID="txtEmail" />  
                        </td>
                    </tr>
                    <tr>
                        <td>Konu : </td>

                        <td>
                            <asp:TextBox runat="server" Width="200" ID="txtKonu" />  
                        </td>
                    </tr>
                    <tr>
                        <td>Mesajınız : </td>


                        <td>
                            <asp:TextBox  Width="200" runat="server"  ID="txtMesaj" />  
                        </td>
                    </tr>
                    <tr>
                        <td>
                            <asp:Button Text="Gönder " Width="150" ID="btnGonder" OnClick="btnGonder_Click" runat="server" />
                        </td>
                        &nbsp &nbsp &nbsp
                        <td>
                            <asp:Button Text="Temizle" Width="150" ID="btnTemizle" OnClick="btnTemizle_Click" runat="server" />
                        </td>
                    </tr>
                </table>
            </div>
        
     
        

        


         
    </form>
</body>
</html>
     
  
    
        //admin login
        <%@ Page Language="C#" AutoEventWireup="true" CodeBehind="AdminLogin.aspx.cs" Inherits="MeetApplication.ForAdmin.AdminLogin" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
<style>
        .text{
            color:#f1ad7c;
        }
        .login{     /******bu bir div; bu divi ortala!!! ve kutulayıp arkasını beyaz yap!!!*/
            display:block;
            width: 600px;
            height: 300px;
            padding: 20px;
            background-color: white;
        }
        body {
            background-color:#f8e3e3;
    font-family: Verdana, monospace, sans-serif;
    font-size: 12px;
    font-weight: bold;
    
}
        .pic img{
            width:100px;
            height:300px;
        }
    </style>
</head>
<body>
    <form id="form1" runat="server">
    <div  >
     <table id="login">
         <tr><td id="pic" colspan="4"> <img  src="pictures/logo.jpg" /> </td>
             
             </tr>
         <tr><td colspan="3" id="text"> Admin Kontrol Sayfası - Kullanıcı Girişi</td></tr>
 

            <tr>
                <td>Admin Adı</td>
                <td> : </td>
                <td>
                    <asp:TextBox ID="txtAdminAdi" runat="server" />
                </td>
                <td >
                   
 <asp:RequiredFieldValidator ID="RequiredFieldValidator5" runat="server" ControlToValidate="txtAdminAdi" ErrorMessage="Bu kısım boş geçilemez." ForeColor="Red"></asp:RequiredFieldValidator>                </td>
            </tr>
            <tr>
                <td>Şifre</td>
                <td> : </td>
                <td>
                    <asp:TextBox ID="txtSifre" runat="server" />
                </td>
                <td >
                    <asp:RequiredFieldValidator ID="RequiredFieldValidator2" runat="server" ControlToValidate="txtSifre" ErrorMessage="Şifre boş geçilemez." ForeColor="Red"></asp:RequiredFieldValidator>
                </td>
            </tr>
         <tr>
             <td colspan="4">
                 <asp:Button Text="Giriş Yap" ID="btnGiris" onclick="btnGiris_Click" runat="server" />
             </td>
         </tr>
         
           
         
         </table>
    </div>
    </form>
</body>
</html>


//admin home page
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="HomePage.aspx.cs" Inherits="MeetApplication.ForAdmin.HomePage" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
</head>
<body>
    <form id="form1" runat="server">
    <div>
        <asp:Button Width="260" Height="500" Text="Restoran" ID="btnRest" OnClick="btnRest_Click" runat="server" />
        <asp:Button Width="260" Height="500" Text="Kategori" ID="btnKat" onclick="btnKat_Click" runat="server" />
        <asp:Button Width="260" Height="500" Text="Urun" ID="btnUrun" onclick="btnUrun_Click" runat="server" />
        <asp:Button Width="260" Height="500" Text="Reklam" ID="btnReklam" OnClick="btnReklam_Click"  runat="server" />
    
    </div>
    </form>
</body>
</html>


//advertisement page for admin
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Advertisementt.aspx.cs" Inherits="MeetApplication.ForAdmin.Advertisementt" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
</head>
<body>
    <form id="form1" runat="server">
    
  <div>
 <table id="tablo">
            <tr>
                <td>Şirket Adı </td>
                
                <td> Süresi(Gün)</td>
                
               <td> Ürün Fotoğrafı</td>
            </tr>
            <tr>
                <td>
                    <asp:TextBox ID="txtCompName" runat="server" />  </td>
               
                
                <td>
                    <asp:TextBox runat="server" ID="txtTime" />  
                </td>
              
                </tr>
        <tr>
               <td colspan="4">
                <asp:Button Text="Ekle" ID="btnEkle" onclick="btnEkle_Click"runat="server" />
                  </td>
                
                   
            </tr>
        </table>
       
        <br />
        <br />
        <br />
        <br />
        <br />
         
        
         <table id="tablo3">
            <tr>
                <td>Reklam ID</td>
                
            </tr>
            <tr>
                <td>
                    <asp:TextBox runat="server" ID="txtSilAdvID" />  </td>
              
            <td>
                <asp:Button Text="Sİl" ID="btnSil" onclick="btnSil_Click" runat="server" />
                  </td>
                
                   
            </tr>
        </table>
        </div>
        </form>
    </body>
    </html>

//comoany page for admin
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Restaurant.aspx.cs" Inherits="MeetApplication.ForAdmin.Restaurant" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
<style>
        body{
            background-color:#fef3f3
        }
        .tablom{

            margin-left:300px;

            
           
        }
    </style>
</head>
<body>
    <form id="form1" runat="server">
    <div id="tablom">
        <table id="tablo">
            <tr>
                <td>Restoran Adı </td>
                <td> Şube</td>
            </tr>
            <tr>
                <td>
                    <asp:TextBox ID="txtRestAdi" runat="server" />  </td>
               
                <td>
                    <asp:TextBox runat="server" ID="txtSube" /></td>
            </tr>
            <tr > <td>
                <asp:Button Text="Ekle" id="ekle" OnClick="ekle_Click" runat="server" />
                  </td>
                
                   
            </tr>
        </table>
       
        <br />
        <br />
        <br />
        <br />
        <br />
         <table id="tabl2">
            <tr>
                <td>Restoran ID</td>
                <td>Restoran Adı </td>
                <td> Şube</td>
            </tr>
            <tr>
                <td>
                    <asp:TextBox runat="server" ID="txtID" />  </td>
                <td>
                    <asp:TextBox ID="txtGuncRestAdi" runat="server" />  </td>
               
                <td>
                    <asp:TextBox runat="server" ID="txtGuncSube" /></td>
            </tr>
            <tr > <td>
                <asp:Button Text="Güncelle" ID="guncelle" onclick="guncelle_Click" runat="server" />
                  </td>
                
                   
            </tr>
        </table>
        <br />
        <br />
        <br />
        <br />
        <br />
         <table id="tablo3">
            <tr>
                <td>Restoran ID</td>
                
            </tr>
            <tr>
                <td>
                    <asp:TextBox runat="server" ID="txtSilRestID" />  </td>
              
            <td>
                <asp:Button Text="Sİl" ID="sil" onclick="sil_Click" runat="server" />
                  </td>
                
                   
            </tr>
        </table>
    
    </div>
    </form>
</body>
</html>

//product page for admin
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Productt.aspx.cs" Inherits="MeetApplication.ForAdmin.Productt" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
 <style>
        body{
            background-color:#fef3f3
        }
        .tablom{

            margin-left:300px;

            
           
        }
    </style>
</head>
<body>
    <form id="form1" runat="server">
    <div>
    <table id="tablo">
            <tr>
                <td>Kategori ID </td>
                <td> Ürün Adı</td>
                <td> Ürün Fiyatı</td>
                <td> Ürün Boyutu</td>
                <td>Kategori Adı</td>
               <%-- <td> Ürün Fotoğrafı</td>--%>
            </tr>
            <tr>
                <td>
                    <asp:TextBox ID="txtCatID" runat="server" />  </td>
               
                <td>
                    <asp:TextBox runat="server" ID="txtProdName" /></td>
                <td>
                    <asp:TextBox runat="server" ID="txtProdPrice" />  
                </td>
                <td>
                    <asp:TextBox runat="server" ID="txtProdSize" />      
                </td>
                <td><asp:TextBox runat="server" Id="txtCatName" />  </td>
                
                <%-- <td>   <asp:FileUpload ID="FileUpload1" runat="server" />
                     <asp:Image ID="Image2" runat="server" />
                 </td>--%>
                </tr>
        <tr>
               <td colspan="5">
                <asp:Button Text="Ekle" ID="btnEkle" OnClick="btnEkle_Click" runat="server" />
                  </td>
                
                   
            </tr>
        </table>
       
        <br />
        <br />
        <br />
        <br />
        <br />
           <table id="tablo2">
            <tr>
                <td>Ürün ID</td>
                <td>Kategori ID </td>
                <td> Ürün Adı</td>
                <td> Ürün Fiyatı</td>
                <td> Ürün Boyutu</td>
                <td>Kategori Adı</td>
               <%-- <td > Ürün Fotoğrafı</td>--%>
            </tr>
            <tr>
                <td>
                    <asp:TextBox ID="txtGuncProID" runat="server" />  </td>
                 <td>
                    <asp:TextBox ID="txtGuncCatID" runat="server" />  </td>
               
                <td>
                    <asp:TextBox runat="server" ID="txtGuncProAdi" /></td>
                <td>
                    <asp:TextBox runat="server" ID="txtGuncProPrice" />  
                </td>
                <td>
                    <asp:TextBox runat="server" ID="txtGuncProSize" />      
                </td>
                <td><asp:TextBox runat="server" Id="txtGuncCatName" />  </td>
                
                 <%--<td>   <asp:FileUpload ID="FileUpload2" runat="server" />
               
                <asp:Image ID="Image1" runat="server" />  </td>--%>
               
                   </tr>
                  
               
                <tr>
                    <td colspan="7" > <asp:Button  Text="Güncelle" ID="btnGuncelle" onClick="btnGuncelle_Click" runat="server" /></td>
                </tr>
                
            
                
                   
            
        </table>
        <br />
        <br />
        <br />
        <br />
        <br />
         <table id="tablo3">
            <tr>
                <td>Ürün ID</td>
                
            </tr>
            <tr>
                <td>
                    <asp:TextBox runat="server" ID="txtSilProID" />  </td>
              
            <td>
                <asp:Button Text="Sİl" ID="btnSil" onclick="btnSil_Click" runat="server" />
                  </td>
                
                   
            </tr>
        </table>
        </div>
        </form>
    </body>


