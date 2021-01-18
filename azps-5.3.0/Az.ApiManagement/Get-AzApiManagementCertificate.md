---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516630"
---
# <span data-ttu-id="a6047-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a6047-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="a6047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6047-102">SYNOPSIS</span></span>
<span data-ttu-id="a6047-103">Получает сертификаты управления API, настроенные для mutual Authentication с backend в службе.</span><span class="sxs-lookup"><span data-stu-id="a6047-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="a6047-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6047-104">SYNTAX</span></span>

### <span data-ttu-id="a6047-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6047-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6047-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6047-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6047-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6047-107">DESCRIPTION</span></span>
<span data-ttu-id="a6047-108">Для **этого необходимо** получить все сертификаты управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="a6047-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="a6047-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6047-109">EXAMPLES</span></span>

### <span data-ttu-id="a6047-110">Пример 1. Получить все сертификаты</span><span class="sxs-lookup"><span data-stu-id="a6047-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="a6047-111">Эта команда получает все сертификаты управления API.</span><span class="sxs-lookup"><span data-stu-id="a6047-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="a6047-112">Пример 2. Получить сертификат по его ИД</span><span class="sxs-lookup"><span data-stu-id="a6047-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="a6047-113">Эта команда получает сертификат управления API с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="a6047-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="a6047-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6047-114">PARAMETERS</span></span>

### <span data-ttu-id="a6047-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="a6047-115">-CertificateId</span></span>
<span data-ttu-id="a6047-116">Определяет ИД сертификата, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="a6047-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6047-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="a6047-117">-Context</span></span>
<span data-ttu-id="a6047-118">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="a6047-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6047-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6047-119">-DefaultProfile</span></span>
<span data-ttu-id="a6047-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6047-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6047-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6047-121">-ResourceId</span></span>
<span data-ttu-id="a6047-122">Идентификатор ресурса Arm сертификата.</span><span class="sxs-lookup"><span data-stu-id="a6047-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="a6047-123">Если он указан, будет пытаться найти сертификат по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="a6047-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="a6047-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="a6047-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6047-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6047-125">-Confirm</span></span>
<span data-ttu-id="a6047-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a6047-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6047-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6047-127">-WhatIf</span></span>
<span data-ttu-id="a6047-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6047-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6047-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a6047-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6047-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6047-130">CommonParameters</span></span>
<span data-ttu-id="a6047-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6047-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6047-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6047-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6047-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6047-133">INPUTS</span></span>

### <span data-ttu-id="a6047-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a6047-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a6047-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a6047-135">System.String</span></span>

## <span data-ttu-id="a6047-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6047-136">OUTPUTS</span></span>

### <span data-ttu-id="a6047-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a6047-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="a6047-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6047-138">NOTES</span></span>

## <span data-ttu-id="a6047-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6047-139">RELATED LINKS</span></span>

[<span data-ttu-id="a6047-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a6047-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="a6047-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a6047-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="a6047-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a6047-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


