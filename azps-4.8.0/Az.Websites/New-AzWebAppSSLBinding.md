---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243122"
---
# <span data-ttu-id="49d5b-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="49d5b-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="49d5b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="49d5b-103">Создание привязки сертификата SSL для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="49d5b-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="49d5b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49d5b-104">SYNTAX</span></span>

### <span data-ttu-id="49d5b-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="49d5b-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49d5b-106">S2</span><span class="sxs-lookup"><span data-stu-id="49d5b-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49d5b-107">Режима</span><span class="sxs-lookup"><span data-stu-id="49d5b-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49d5b-108">Режим</span><span class="sxs-lookup"><span data-stu-id="49d5b-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49d5b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49d5b-109">DESCRIPTION</span></span>
<span data-ttu-id="49d5b-110">Командлет **New-AzWebAppSSLBinding** создает для веб-приложения Azure Связывание сертификата Secure Socket Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="49d5b-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="49d5b-111">Командлет создает привязку SSL двумя способами:</span><span class="sxs-lookup"><span data-stu-id="49d5b-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="49d5b-112">Вы можете привязать веб-приложение к существующему сертификату.</span><span class="sxs-lookup"><span data-stu-id="49d5b-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="49d5b-113">Вы можете добавить новый сертификат и затем привязать веб-приложение к этому новому сертификату.</span><span class="sxs-lookup"><span data-stu-id="49d5b-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="49d5b-114">Независимо от того, какой подход вы используете, сертификат и веб-приложение должны быть связаны с одной и той же группой ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="49d5b-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="49d5b-115">Если у вас есть веб-приложение в группе ресурсов а и вы хотите привязать это веб-приложение к сертификату в группе ресурсов B, единственным способом является Отправка копии сертификата в группу ресурсов A. Если вы загрузили новый сертификат, имейте в виду следующие требования для SSL-сертификата Azure:</span><span class="sxs-lookup"><span data-stu-id="49d5b-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="49d5b-116">Сертификат должен содержать закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="49d5b-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="49d5b-117">Сертификат должен использовать формат почтового обмена личной информацией (PFX).</span><span class="sxs-lookup"><span data-stu-id="49d5b-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="49d5b-118">Имя субъекта сертификата должно соответствовать домену, который используется для доступа к веб-приложению.</span><span class="sxs-lookup"><span data-stu-id="49d5b-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="49d5b-119">Сертификат должен использовать не менее 2048-битного шифрования.</span><span class="sxs-lookup"><span data-stu-id="49d5b-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="49d5b-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49d5b-120">EXAMPLES</span></span>

### <span data-ttu-id="49d5b-121">Пример 1: привязка сертификата к веб-приложению</span><span class="sxs-lookup"><span data-stu-id="49d5b-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="49d5b-122">Эта команда привязывает существующий сертификат Azure (сертификат с отпечатным E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) к веб-приложению с именем ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="49d5b-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="49d5b-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="49d5b-123">Example 2</span></span>

<span data-ttu-id="49d5b-124">Создание привязки сертификата SSL для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="49d5b-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="49d5b-125">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="49d5b-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="49d5b-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49d5b-126">PARAMETERS</span></span>

### <span data-ttu-id="49d5b-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="49d5b-127">-CertificateFilePath</span></span>
<span data-ttu-id="49d5b-128">Задает путь к файлу для сертификата, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="49d5b-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="49d5b-129">Параметр *CertificateFilePath* требуется только в том случае, если сертификат еще не был загружен в Azure.</span><span class="sxs-lookup"><span data-stu-id="49d5b-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d5b-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="49d5b-130">-CertificatePassword</span></span>
<span data-ttu-id="49d5b-131">Задает пароль для расшифровки сертификата.</span><span class="sxs-lookup"><span data-stu-id="49d5b-131">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d5b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d5b-132">-DefaultProfile</span></span>
<span data-ttu-id="49d5b-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49d5b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d5b-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49d5b-134">-Name</span></span>
<span data-ttu-id="49d5b-135">Указывает имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="49d5b-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d5b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49d5b-136">-ResourceGroupName</span></span>
<span data-ttu-id="49d5b-137">Указывает имя группы ресурсов, которой назначен сертификат.</span><span class="sxs-lookup"><span data-stu-id="49d5b-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="49d5b-138">В одной команде нельзя использовать параметры *ResourceGroupName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="49d5b-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d5b-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="49d5b-139">-Slot</span></span>
<span data-ttu-id="49d5b-140">Указывает имя слота развертывания веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="49d5b-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="49d5b-141">Вы можете использовать командлет Get-AzWebAppSlot, чтобы получить доступ к ячейкам.</span><span class="sxs-lookup"><span data-stu-id="49d5b-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="49d5b-142">Слоты развертывания предоставляют способ для размещения и проверки веб-приложений без доступа к этим приложениям через Интернет.</span><span class="sxs-lookup"><span data-stu-id="49d5b-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="49d5b-143">Обычно изменения развертываются на промежуточный сайт, проверяют эти изменения, а затем развертываются на рабочем сайте (доступ к Интернету).</span><span class="sxs-lookup"><span data-stu-id="49d5b-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d5b-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="49d5b-144">-SslState</span></span>
<span data-ttu-id="49d5b-145">Указывает, включен ли сертификат.</span><span class="sxs-lookup"><span data-stu-id="49d5b-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="49d5b-146">Установите для параметра *SSLState* значение 1, чтобы включить сертификат, или установите для *SSLState* значение 0, чтобы отключить сертификат.</span><span class="sxs-lookup"><span data-stu-id="49d5b-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d5b-147">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="49d5b-147">-Thumbprint</span></span>
<span data-ttu-id="49d5b-148">Указывает уникальный идентификатор сертификата.</span><span class="sxs-lookup"><span data-stu-id="49d5b-148">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d5b-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="49d5b-149">-WebApp</span></span>
<span data-ttu-id="49d5b-150">Указывает веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="49d5b-150">Specifies a Web App.</span></span>
<span data-ttu-id="49d5b-151">Чтобы получить веб-приложение, используйте командлет Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="49d5b-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="49d5b-152">Параметр *webapp* нельзя использовать в той же команде, что и параметр *ResourceGroupName* , и (или) *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="49d5b-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49d5b-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="49d5b-153">-WebAppName</span></span>
<span data-ttu-id="49d5b-154">Указывает имя веб-приложения, для которого создается новая привязка SSL.</span><span class="sxs-lookup"><span data-stu-id="49d5b-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="49d5b-155">В одной команде нельзя использовать параметры *WebAppName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="49d5b-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d5b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d5b-156">CommonParameters</span></span>
<span data-ttu-id="49d5b-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49d5b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d5b-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49d5b-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d5b-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49d5b-159">INPUTS</span></span>

### <span data-ttu-id="49d5b-160">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="49d5b-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="49d5b-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49d5b-161">OUTPUTS</span></span>

### <span data-ttu-id="49d5b-162">Microsoft. Azure. Management. website. Models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="49d5b-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="49d5b-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="49d5b-163">NOTES</span></span>

## <span data-ttu-id="49d5b-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49d5b-164">RELATED LINKS</span></span>

[<span data-ttu-id="49d5b-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="49d5b-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="49d5b-166">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="49d5b-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="49d5b-167">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="49d5b-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="49d5b-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49d5b-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


