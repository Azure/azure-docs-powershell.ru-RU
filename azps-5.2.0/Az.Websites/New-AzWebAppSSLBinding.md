---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414836"
---
# <span data-ttu-id="a1e11-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a1e11-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="a1e11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1e11-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e11-103">Создает привязку SSL-сертификата для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a1e11-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="a1e11-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1e11-104">SYNTAX</span></span>

### <span data-ttu-id="a1e11-105">S1</span><span class="sxs-lookup"><span data-stu-id="a1e11-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1e11-106">S2</span><span class="sxs-lookup"><span data-stu-id="a1e11-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1e11-107">S3</span><span class="sxs-lookup"><span data-stu-id="a1e11-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1e11-108">S4</span><span class="sxs-lookup"><span data-stu-id="a1e11-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1e11-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1e11-109">DESCRIPTION</span></span>
<span data-ttu-id="a1e11-110">Для azure Web App создается привязка SSL-сертификата **New-AzWebAppSSLBinding.**</span><span class="sxs-lookup"><span data-stu-id="a1e11-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="a1e11-111">С его выполнения можно создать привязку SSL двумя способами:</span><span class="sxs-lookup"><span data-stu-id="a1e11-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="a1e11-112">Веб-приложение можно привязать к существующему сертификату.</span><span class="sxs-lookup"><span data-stu-id="a1e11-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="a1e11-113">Вы можете добавить новый сертификат, а затем привязать к этому новому сертификату веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="a1e11-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="a1e11-114">Независимо от используемого подхода сертификат и веб-приложение должны быть связаны с одной и той же группой ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e11-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="a1e11-115">Если у вас есть веб-приложение в группе ресурсов А и вы хотите привязать его к сертификату в группе ресурсов Б, единственный способ сделать это — отправить копию сертификата в группу ресурсов А. При отправке нового сертификата следует помнить о следующих требованиях к SSL-сертификату Azure:</span><span class="sxs-lookup"><span data-stu-id="a1e11-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="a1e11-116">Сертификат должен содержать закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="a1e11-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="a1e11-117">Сертификат должен иметь формат PFX.</span><span class="sxs-lookup"><span data-stu-id="a1e11-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="a1e11-118">Имя субъекта сертификата должно совпадать с доменом, используемым для доступа к Web App.</span><span class="sxs-lookup"><span data-stu-id="a1e11-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="a1e11-119">Сертификат должен иметь не менее 2048-битного шифрования.</span><span class="sxs-lookup"><span data-stu-id="a1e11-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="a1e11-120">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1e11-120">EXAMPLES</span></span>

### <span data-ttu-id="a1e11-121">Пример 1. Привязка сертификата к веб-приложению</span><span class="sxs-lookup"><span data-stu-id="a1e11-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="a1e11-122">Эта команда связывает существующий сертификат Azure (сертификат с thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) с веб-приложением ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="a1e11-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="a1e11-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a1e11-123">Example 2</span></span>

<span data-ttu-id="a1e11-124">Создает привязку SSL-сертификата для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a1e11-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="a1e11-125">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="a1e11-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="a1e11-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1e11-126">PARAMETERS</span></span>

### <span data-ttu-id="a1e11-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a1e11-127">-CertificateFilePath</span></span>
<span data-ttu-id="a1e11-128">Путь к файлу для отправки сертификата.</span><span class="sxs-lookup"><span data-stu-id="a1e11-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="a1e11-129">Параметр *CertificateFilePath* требуется только в том случае, если сертификат еще не загружен в Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e11-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="a1e11-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a1e11-130">-CertificatePassword</span></span>
<span data-ttu-id="a1e11-131">Указывает пароль для расшифровки сертификата.</span><span class="sxs-lookup"><span data-stu-id="a1e11-131">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="a1e11-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e11-132">-DefaultProfile</span></span>
<span data-ttu-id="a1e11-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e11-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1e11-134">-Name</span><span class="sxs-lookup"><span data-stu-id="a1e11-134">-Name</span></span>
<span data-ttu-id="a1e11-135">Указывает имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="a1e11-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="a1e11-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e11-136">-ResourceGroupName</span></span>
<span data-ttu-id="a1e11-137">Имя группы ресурсов, которая назначена сертификату.</span><span class="sxs-lookup"><span data-stu-id="a1e11-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="a1e11-138">В одной команде нельзя использовать параметр *ResourceGroupName* и *параметр WebApp.*</span><span class="sxs-lookup"><span data-stu-id="a1e11-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="a1e11-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="a1e11-139">-Slot</span></span>
<span data-ttu-id="a1e11-140">Указывает имя слота развертывания Web App.</span><span class="sxs-lookup"><span data-stu-id="a1e11-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="a1e11-141">Для получения отрезка можно использовать Get-AzWebAppSlot-код.</span><span class="sxs-lookup"><span data-stu-id="a1e11-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="a1e11-142">Слоты развертывания обеспечивают возможность поэтапной проверки и проверки веб-приложений без доступа к этим приложениям через Интернет.</span><span class="sxs-lookup"><span data-stu-id="a1e11-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="a1e11-143">Обычно изменения развертываются на промежуточном сайте, проверяются, а затем развертываются на производственном (доступном через Интернет) сайте.</span><span class="sxs-lookup"><span data-stu-id="a1e11-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="a1e11-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="a1e11-144">-SslState</span></span>
<span data-ttu-id="a1e11-145">Указывает, включен ли сертификат.</span><span class="sxs-lookup"><span data-stu-id="a1e11-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="a1e11-146">Установите для *параметра SSLState* 1 параметр 1, чтобы включить сертификат, или *для параметра SSLState* 0, чтобы отключить сертификат.</span><span class="sxs-lookup"><span data-stu-id="a1e11-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="a1e11-147">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="a1e11-147">-Thumbprint</span></span>
<span data-ttu-id="a1e11-148">Указывает уникальный идентификатор сертификата.</span><span class="sxs-lookup"><span data-stu-id="a1e11-148">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="a1e11-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a1e11-149">-WebApp</span></span>
<span data-ttu-id="a1e11-150">Определяет веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="a1e11-150">Specifies a Web App.</span></span>
<span data-ttu-id="a1e11-151">Чтобы получить веб-приложение, воспользуйтесь Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="a1e11-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="a1e11-152">Нельзя использовать параметр *WebApp* в той же команде, что и параметр *ResourceGroupName* или *WebAppName.*</span><span class="sxs-lookup"><span data-stu-id="a1e11-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="a1e11-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a1e11-153">-WebAppName</span></span>
<span data-ttu-id="a1e11-154">Указывает имя веб-приложения, для которого создается новая привязка SSL.</span><span class="sxs-lookup"><span data-stu-id="a1e11-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="a1e11-155">В одной команде нельзя использовать *параметры WebAppName* и *WebApp.*</span><span class="sxs-lookup"><span data-stu-id="a1e11-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="a1e11-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e11-156">CommonParameters</span></span>
<span data-ttu-id="a1e11-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e11-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e11-158">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1e11-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e11-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1e11-159">INPUTS</span></span>

### <span data-ttu-id="a1e11-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a1e11-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a1e11-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1e11-161">OUTPUTS</span></span>

### <span data-ttu-id="a1e11-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="a1e11-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="a1e11-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1e11-163">NOTES</span></span>

## <span data-ttu-id="a1e11-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1e11-164">RELATED LINKS</span></span>

[<span data-ttu-id="a1e11-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a1e11-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="a1e11-166">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a1e11-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="a1e11-167">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1e11-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="a1e11-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a1e11-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


