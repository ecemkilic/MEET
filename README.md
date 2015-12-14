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
