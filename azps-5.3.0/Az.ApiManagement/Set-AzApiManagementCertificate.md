---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: 3c31da297b47c5d35c7d7b4eea5c55ca87d9521d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423212"
---
# <span data-ttu-id="f5209-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f5209-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="f5209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5209-102">SYNOPSIS</span></span>
<span data-ttu-id="f5209-103">Изменяет сертификат управления API, настроенный для совместной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f5209-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="f5209-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5209-104">SYNTAX</span></span>

### <span data-ttu-id="f5209-105">LoadFromFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5209-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5209-106">Необработанные</span><span class="sxs-lookup"><span data-stu-id="f5209-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5209-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5209-107">DESCRIPTION</span></span>
<span data-ttu-id="f5209-108">**Set-AzApiManagementCertificate cmdlet** изменяет сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="f5209-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="f5209-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5209-109">EXAMPLES</span></span>

### <span data-ttu-id="f5209-110">Пример 1. Изменение сертификата</span><span class="sxs-lookup"><span data-stu-id="f5209-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="f5209-111">Эта команда изменяет указанный сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="f5209-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="f5209-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5209-112">PARAMETERS</span></span>

### <span data-ttu-id="f5209-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="f5209-113">-CertificateId</span></span>
<span data-ttu-id="f5209-114">Определяет код сертификата, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="f5209-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="f5209-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="f5209-115">-Context</span></span>
<span data-ttu-id="f5209-116">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="f5209-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f5209-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5209-117">-DefaultProfile</span></span>
<span data-ttu-id="f5209-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5209-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5209-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5209-119">-PassThru</span></span>
<span data-ttu-id="f5209-120">passthru</span><span class="sxs-lookup"><span data-stu-id="f5209-120">passthru</span></span>

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

### <span data-ttu-id="f5209-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="f5209-121">-PfxBytes</span></span>
<span data-ttu-id="f5209-122">Массив в формате PFX файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="f5209-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="f5209-123">Этот параметр является required, если параметр *PfxFilePath не указан.*</span><span class="sxs-lookup"><span data-stu-id="f5209-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="f5209-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="f5209-124">-PfxFilePath</span></span>
<span data-ttu-id="f5209-125">Путь к файлу сертификата в формате PFX, который нужно создать и отправить.</span><span class="sxs-lookup"><span data-stu-id="f5209-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="f5209-126">Этот параметр является required, если параметр *PfxBytes не указан.*</span><span class="sxs-lookup"><span data-stu-id="f5209-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="f5209-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="f5209-127">-PfxPassword</span></span>
<span data-ttu-id="f5209-128">Пароль сертификата.</span><span class="sxs-lookup"><span data-stu-id="f5209-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="f5209-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5209-129">CommonParameters</span></span>
<span data-ttu-id="f5209-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5209-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5209-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5209-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5209-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5209-132">INPUTS</span></span>

### <span data-ttu-id="f5209-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f5209-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f5209-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f5209-134">System.String</span></span>

### <span data-ttu-id="f5209-135">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="f5209-135">System.Byte[]</span></span>

### <span data-ttu-id="f5209-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f5209-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f5209-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5209-137">OUTPUTS</span></span>

### <span data-ttu-id="f5209-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f5209-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="f5209-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5209-139">NOTES</span></span>

## <span data-ttu-id="f5209-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5209-140">RELATED LINKS</span></span>

[<span data-ttu-id="f5209-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f5209-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="f5209-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f5209-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="f5209-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f5209-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


