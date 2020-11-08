---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: 3c31da297b47c5d35c7d7b4eea5c55ca87d9521d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246277"
---
# <span data-ttu-id="6aada-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6aada-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="6aada-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6aada-102">SYNOPSIS</span></span>
<span data-ttu-id="6aada-103">Изменение сертификата управления API, настроенного для взаимной проверки подлинности на внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="6aada-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="6aada-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6aada-104">SYNTAX</span></span>

### <span data-ttu-id="6aada-105">LoadFromFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6aada-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6aada-106">Сырь</span><span class="sxs-lookup"><span data-stu-id="6aada-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aada-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aada-107">DESCRIPTION</span></span>
<span data-ttu-id="6aada-108">Командлет **Set-AzApiManagementCertificate** изменяет сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="6aada-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="6aada-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6aada-109">EXAMPLES</span></span>

### <span data-ttu-id="6aada-110">Пример 1: изменение сертификата</span><span class="sxs-lookup"><span data-stu-id="6aada-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="6aada-111">Эта команда изменяет указанный сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="6aada-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="6aada-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6aada-112">PARAMETERS</span></span>

### <span data-ttu-id="6aada-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="6aada-113">-CertificateId</span></span>
<span data-ttu-id="6aada-114">Указывает ИД сертификата, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="6aada-114">Specifies the ID of the certificate to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aada-115">-Context</span><span class="sxs-lookup"><span data-stu-id="6aada-115">-Context</span></span>
<span data-ttu-id="6aada-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6aada-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6aada-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aada-117">-DefaultProfile</span></span>
<span data-ttu-id="6aada-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6aada-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aada-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6aada-119">-PassThru</span></span>
<span data-ttu-id="6aada-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="6aada-120">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aada-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="6aada-121">-PfxBytes</span></span>
<span data-ttu-id="6aada-122">Задает массив байтов из файла сертификата в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="6aada-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="6aada-123">Этот параметр является обязательным, если не указан параметр *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="6aada-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aada-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="6aada-124">-PfxFilePath</span></span>
<span data-ttu-id="6aada-125">Задает путь к файлу сертификата в формате PFX для создания и отправки.</span><span class="sxs-lookup"><span data-stu-id="6aada-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="6aada-126">Этот параметр является обязательным, если не указан параметр *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="6aada-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aada-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="6aada-127">-PfxPassword</span></span>
<span data-ttu-id="6aada-128">Указывает пароль для сертификата.</span><span class="sxs-lookup"><span data-stu-id="6aada-128">Specifies the password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aada-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aada-129">CommonParameters</span></span>
<span data-ttu-id="6aada-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6aada-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aada-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6aada-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aada-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6aada-132">INPUTS</span></span>

### <span data-ttu-id="6aada-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6aada-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6aada-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6aada-134">System.String</span></span>

### <span data-ttu-id="6aada-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="6aada-135">System.Byte[]</span></span>

### <span data-ttu-id="6aada-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6aada-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6aada-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aada-137">OUTPUTS</span></span>

### <span data-ttu-id="6aada-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6aada-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="6aada-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="6aada-139">NOTES</span></span>

## <span data-ttu-id="6aada-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6aada-140">RELATED LINKS</span></span>

[<span data-ttu-id="6aada-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6aada-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="6aada-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6aada-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="6aada-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6aada-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


