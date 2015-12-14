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


-Ecem

//product for company

<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Categoryy.aspx.cs" Inherits="MeetApplication.ForAdmin.Categoryy" %>

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
                <td>Restoran ID </td>
                <td> Kategori Adi</td>
            </tr>
            <tr>
                <td>
                    <asp:TextBox ID="txtRestID" runat="server" />  </td>
               
                <td>
                    <asp:TextBox runat="server" ID="txtKatAdi" /></td>
            </tr>
            <tr > <td>
                <asp:Button Text="Ekle" id="btnEkle" OnClick="btnEkle_Click" runat="server" />
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
                <td>Katogori ID</td>
                <td>Restoran ID </td>
                <td> Kategori Adı</td>
            </tr>
            <tr>
                <td>
                    <asp:TextBox runat="server" ID="txtGuncKatID" />  </td>
                <td>
                    <asp:TextBox ID="txtGuncRestID" runat="server" />  </td>
               
                <td>
                    <asp:TextBox runat="server" ID="txtGuncKatAdi" /></td>
            </tr>
            <tr > <td>
                <asp:Button Text="Güncelle" ID="btnGuncelle" onclick="btnGuncelle_Click" runat="server" />
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
                <td>Kategori ID</td>
                
            </tr>
            <tr>
                <td>
                    <asp:TextBox runat="server" ID="txtSilKatID" />  </td>
              
            <td>
                <asp:Button Text="Sİl" ID="btnSil" onclick="btnSil_Click" runat="server" />
                  </td>
                
                   
            </tr>
        </table>
    
    </div>
    </form>
</body>
</html>

//user login
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Login.aspx.cs" Inherits="MeetApplication.ForUser.Login" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
    <style> #body{
           margin-left:20%;
           margin-top:10%;
       
        }</style>
</head>
<body>
    <form id="form1" runat="server">
        <div style="height:50px"></div>
       <div style="background-color:black;color:black; width:1347px ; height:125px">   <img  src="/ForUser/pictures/siyahlogo.png" style="float:left;height: 125px; width: 217px; margin-left: 35px;" />
        </div>
        
        <div id="body" style="text-align:left; margin-bottom: 1px;">
       &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <div>
     <table>
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
             <td colspan="3">
                 <asp:Button ID="btnGirisYap" Text="Giriş Yap" OnClick="btnGirisYap_Click" runat="server" /></td>
         </tr>
         </table>
    </div>
    </form>
</body>
</html>


//user register
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Register.aspx.cs" Inherits="MeetApplication.ForUser.Register" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
    <style>  #body{
           margin-left:20%;
           margin-top:10%;
       
        }</style>
</head>
<body>
    <form id="form1" runat="server">
        <div style="height:50px"></div>
       <div style="background-color:black;color:black; width:1347px ; height:125px">   <img  src="/ForUser/pictures/siyahlogo.png" style="float:left;height: 125px; width: 217px; margin-left: 35px;" />
        </div>
        
        <div id="body" style="text-align:left; margin-bottom: 1px;">
       &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <div>
     <table>
            <tr>
                <td>Email Adresi</td>
                <td> : </td>
                <td>
                    <asp:TextBox Width="300" ID="txtEmailAdres" runat="server" />
                </td>
            </tr>
            <tr>
                <td>Şifre</td>
                <td> : </td>
                <td>
                    <asp:TextBox Width="300" ID="txtSifre" runat="server" />
                </td>
            </tr>
            <tr>
                <td>Şifre Tekrar</td>
                <td> : </td>
                <td>
                    <asp:TextBox Width="300" ID="txtSifreTekrar" runat="server" />
                </td>
            </tr>
             <tr>
                <td>Ad </td>
                <td> : </td>
                <td>
                    <asp:TextBox Width="300" ID="txtKullaniciAdi" runat="server"></asp:TextBox>
                </td>
              
            </tr>
             <tr>
                <td>Soyad </td>
                <td> : </td>
                <td >
                    <asp:TextBox Width="300" ID="txtSoyad" runat="server"></asp:TextBox>
                </td>
            </tr>
            <tr>
                <td>Doğum Tarihi <i>(gün/ay/yıl)</i> </td>
                <td> : </td>
                <td >
                    <asp:TextBox Width="95" ID="txtGun" runat="server"></asp:TextBox>
               
                    <asp:TextBox Width="95" ID="txtAy" runat="server" />  
                
                    <asp:TextBox Width="95" ID="txtYil" runat="server" />   </td>
            </tr>
         <tr>   <td colspan="3"> 
            <asp:CheckBox ID="CheckBox1" runat="server" />Yemeksepeti'nin sunduğu kampanyalar, indirimler ve haberler ile ilgili e-posta almak istiyorum. </td>
            
                </tr>
           
            <tr>
                <td colspan="3">
                    <asp:Button id="btnKayitOl" Text="Kayıt Ol" OnClick="btnKayitOl_Click"  runat="server" />
                </td>
            </tr>
            
        </table>
    </div>
    </form>
</body>
</html>

//user main page
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="MainPage.aspx.cs" Inherits="MeetApplication.ForUser.MainPage" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
    <script src="../jquery-1.11.3.js"></script>
    <style> 
        .txt{
            float:right;
            margin-right:0%;
        }
        #arama{
            background-color:red;
            background:RED;
            height:37px;
        }
        #arm1{
            padding-top:25px;
        }
     
        #rst{
            background-color:#f2ebeb;
            width:100%;
        }
       

        #adv{
            width:200px;
            height:230px;
            bottom:5px;
            right:5px;
        }
        #hmb{
            float:right;
        }
            #Header
        {
            width: auto;
            height: 100px;
           
            position: relative;
            top: 0px;
            left: 0px;
        }

        #Logo
        {
            width: 240px;
            height: 100px;
            font-size: 28px;
            font-weight: bold;
            color: #f8f8f8;
            text-align: center;
            line-height: 100px;
            float: left;
        }

        #Sepet
        {
            float: left;
            position: absolute;
            right: 200px;
            top: 40px;
        }

            #Sepet a
            {
                color: #f8f8f8;
                font-size: 16px;
            }

                #Sepet a:hover
                {
                    color: #f00;
                }

                #restPic{
                    float:right;
                    width:150px;
                    height:150px;
                }

        #AcilirSepet
        {
            width: 200px;
            height: 300px;
            background-color: #fff;
            overflow-y: scroll;
            display: none;
            position: absolute;
            border: 1px solid #808080;
        }

        #Content
        {
            padding: 0 20px;
        }
        body{
            padding:0px;
            margin:0px;
        }
 </style>
    <script src="jquery-1.11.3.js"></script>
 
    </head>
<body>
    <form id="form1" runat="server">
     <div id="Header">
       <div style="background-color:black;color:black; width:1347px ; height:100px">   <img  src="/ForUser/pictures/siyahlogo.png" style="float:left;height: 96px; width: 217px; margin-left: 35px; margin-top: 2px;" />
       
            </div>
           
        </div>   
           
       

        
    <div>

        <br />

    </div>        
        <div >           
            <div>
           
       

        
    <div id="arama">
        <table>
            <tr id="arm1">
                <td >
                    <asp:DropDownList ID="ddlRestaurants" runat="server" Width="400px" Height="30px" style="margin-left: 111px; margin-top: 0px;"></asp:DropDownList>
                    <asp:Button ID="Button1" runat="server" Text="Ara" style= Height="30" Width="251px" BackColor="#FF6600" OnClick="Button1_Click" />
                </td>
           
                <td>
                    &nbsp;</td>
            </tr>
            
        </table>       
    </div>    
                <asp:Repeater ID="rptRestaurants" runat="server">
                    <ItemTemplate> 
                        <table id="rst" >
                            <tr >
                                <td>
                                                                     
                                </td>
                                <td>
                                   
                                    <img id="hmb" src="/ForUser/pictures/hmb.png" alt="Alternate Text" />
                                </td>
                            </tr>
                        </table>                       
                        
                        
                    </ItemTemplate>                    
                </asp:Repeater>
            </div>
            
            <div>
               <div>
                        <table style="width:100%">
                            <tr>
                                <td>Ürün Adedi</td>
                                <td>Ürün Fotoğrafı</td>
                                <td>Ürün Kategorisi</td>
                                <td>Ürün Adı</td>
                                <td>Ürün Boyutu</td>
                                <td>Ürün Fiyatı</td>
                            </tr>
                          
        <div id="Content">
            <asp:Repeater ID="rptUrunler" OnItemCommand="rptUrunler_ItemCommand" runat="server">
                <ItemTemplate> 
                    <tr> 
                                <td>
                                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                                    
                                </td>
                                <td>
                                   
                                </td>
                                <td>
                                  
                                </td>
                                <td>
                                  
                                  </td>
                                <td>
                                  ;
                                </td>
                                <td>
                                   
                                    
                                </td>
                                  </tr>
                </ItemTemplate>
            </asp:Repeater>
        </div>
              

               </table>
            </div>
            </div>
       
       
    </form>
</body>
</html>

//user choose city page
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="ChooseCity.aspx.cs" Inherits="MeetApplication.ForUser.ChooseCity" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
 <style>
       #body{
           margin-left:20%;
           margin-top:10%;
       
        }
       #cities{
           width:100px;
           margin-left:350px;
       }
      
    </style>
</head>
<body style="width: 956px; margin-right: 98px; margin-bottom: 300px;">
      
    <form id="form1"  runat="server" style="width: 932px; text-align:center; height: 517px;">
        <div style="height:50px"></div>
       <div style="background-color:black;color:black; width:1347px ; height:125px">   <img  src="/ForUser/pictures/siyahlogo.png" style="float:left;height: 125px; width: 217px; margin-left: 35px;" />
        </div>
        
        <div id="body" style="text-align:left; margin-bottom: 1px;">
       &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
       <asp:Label ID="Label13" runat="server" Text="Dünyanın en büyük mutfağına hoş geldiniz. Bulunduğunuz şehri seçiniz..." Font-Size="Large"></asp:Label>
        </div>
        <div style="margin-left:-15%">
        </div>
        <div>

            <br />

        </div>
        <div style="text-align:center; width: 930px;">
        &nbsp;&nbsp;&nbsp;
        <table id="cities" " >
        <tr>
            <td>

            </td>
            <td>
                <asp:Button ID="Button1" runat="server" Text="1" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button1_Click" />
            </td>
            <td>

            </td>
            <td>
                <asp:Button ID="Button6" runat="server" Text="6" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button6_Click" />
            </td>
            <td>

            </td>
            <td>
                <asp:Button ID="Button7" runat="server" Text="7" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button17_Click" />
            </td>
            <td>

            </td>
            <td>
                <asp:Button ID="Button10" runat="server" Text="10" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button10_Click" />
            </td>
            <td>

            </td>
            <td>
                <asp:Button ID="Button14" runat="server" Text="14" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button14_Click" />
            </td>
            <td>

            </td>
            <td>
                <asp:Button ID="Button16" runat="server" Text="16" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button16_Click" />
            </td>
            <td>

            </td>
            
        </tr>
      
        <tr>
            <td>

            </td>
            <td >
                <asp:Label ID="Label1" runat="server" Text="Adana"></asp:Label>
            </td>
            <td>

            </td>
            <td >
                <asp:Label ID="Label2" runat="server" Text="Ankara"></asp:Label>
            </td>
            <td >

            </td>
            <td>
                <asp:Label ID="Label3" runat="server" Text="Antalya"></asp:Label>
            </td>
            <td >

            </td>
            <td >
                <asp:Label ID="Label4" runat="server" Text="Balıkesir"></asp:Label>
            </td>
            <td >

            </td>
            <td >
                <asp:Label ID="Label5" runat="server" Text="Bolu"></asp:Label>
            </td>
            <td >

              

            </td>
            <td >
                <asp:Label ID="Label6" runat="server" Text="Bursa"></asp:Label>
            </td>
            <td>

            </td>
            
        </tr>
   
        <tr>
            <td>

            </td>
            <td>
                <asp:Button ID="Button17" runat="server" Text="17" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button17_Click" />
            </td>
            <td>

            </td>
            <td>
                <asp:Button ID="Button22" runat="server" Text="22" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button22_Click" />
            </td>
            <td>

            </td>
            <td>
                <asp:Button ID="Button26" runat="server" Text="26" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button26_Click"  />
            </td>
            <td>

            </td>
            <td>
                <asp:Button ID="Button34" runat="server" Text="34" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button34_Click" />
            </td>
            <td>

            </td>
            <td>
                <asp:Button ID="Button59" runat="server" Text="59" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button59_Click" />
            </td>
            <td>

            </td>
            <td>
                <asp:Button ID="Button61" runat="server" Text="61" BackColor="#FF6600" Height="80px" Width="80px" OnClick="Button61_Click" />
            </td>
            <td>

            </td>
        </tr>
      
        <tr>
            <td>

            </td>
            <td>
                <asp:Label ID="Label7" runat="server" Text="Çanakkale"></asp:Label>
            </td>
            <td>

            </td>
            <td>
                <asp:Label ID="Label8" runat="server" Text="Edirne"></asp:Label>
            </td>
            <td>

            </td>
            <td class="auto-style5">
                <asp:Label ID="Label9" runat="server" Text="Eskişehir"></asp:Label>
            </td>
            <td class="auto-style6">

            </td>
            <td class="auto-style4">
                <asp:Label ID="Label10" runat="server" Text="İstanbul"></asp:Label>
            </td>
            <td>

            </td>
            <td>
                <asp:Label ID="Label11" runat="server" Text="Tekirdağ"></asp:Label>
            </td>
            <td>

            </td>
            <td>
                <asp:Label ID="Label12" runat="server" Text="Trabzon"></asp:Label>
            </td>
            <td>

            </td>
            </tr>
            </table>
            </div>
    </form>
    
</body>

</html>

//user order page
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="OrderPage.aspx.cs" Inherits="MeetApplication.ForUser.OrderPage" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
    <style>
        #card{
            margin-top:10%;
            margin-left:30%;
        }
        .auto-style1 {
            width: 160px;
        }
    </style>
</head>
<body>
    <form id="form1" runat="server">
        <div style="background-color:black;color:black; width:1347px ; height:100px">   <img  src="/ForUser/pictures/siyahlogo.png" style="float:left;height: 96px; width: 217px; margin-left: 35px; margin-top: 2px;" />
       
            </div>
    <div id="card">
        <table>
            <tr>
                <td class="auto-style1">
                    Kart Sahibinin Adı:
                </td>
                <td>
                    <asp:TextBox ID="TextBox1" runat="server"></asp:TextBox>
                </td>
            </tr>
            <tr>
                <td class="auto-style1">
                    Kart Numarası:
                </td>
                <td>
                    <asp:TextBox ID="TextBox5" runat="server"></asp:TextBox>
                </td>
                </tr>
            <tr>
                <td class="auto-style1">
                    Son Kullanma Tarihi:
                </td>
                <td>
                    <asp:TextBox ID="TextBox6" runat="server"></asp:TextBox>
                </td>
             </tr>
            <tr>
                <td class="auto-style1">
                    Güvenlik Kodu:
                </td>
                <td>
                    <asp:TextBox ID="TextBox7" runat="server"></asp:TextBox>
                </td>
            </tr>
          <tr>
                
              <td colspan="2">
                  <asp:Button ID="Button1" runat="server" OnClick="Button1_Click" style="background-color:green; margin-left: 95px;" Text="Sipariş Ver" Width="139px" />
                    
              </td>
            </tr>
            <tr><td  colspan="2">
                    <asp:Label Text="" ID="lblBilgi" runat="server" />
                </td></tr>
        </table>
    
    </div>
    </form>
</body>
</html>



