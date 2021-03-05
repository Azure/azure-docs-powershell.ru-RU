---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 1885f8b4f3c72ace4bad55b355e1d16013228611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972264"
---
# <span data-ttu-id="a730a-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a730a-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="a730a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a730a-102">SYNOPSIS</span></span>
<span data-ttu-id="a730a-103">Получает сертификаты управления API, настроенные для mutual Authentication с backend в службе.</span><span class="sxs-lookup"><span data-stu-id="a730a-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="a730a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a730a-104">SYNTAX</span></span>

### <span data-ttu-id="a730a-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a730a-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a730a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a730a-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a730a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a730a-107">DESCRIPTION</span></span>
<span data-ttu-id="a730a-108">Для получения всех задаваемого сертификата управления API Azure вы получаете все сертификаты **Get-AzApiManagementCertificate.**</span><span class="sxs-lookup"><span data-stu-id="a730a-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="a730a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a730a-109">EXAMPLES</span></span>

### <span data-ttu-id="a730a-110">Пример 1. Получить все сертификаты</span><span class="sxs-lookup"><span data-stu-id="a730a-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="a730a-111">Эта команда получает все сертификаты управления API.</span><span class="sxs-lookup"><span data-stu-id="a730a-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="a730a-112">Пример 2. Получить сертификат по его ИД</span><span class="sxs-lookup"><span data-stu-id="a730a-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="a730a-113">Эта команда получает сертификат управления API с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="a730a-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="a730a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a730a-114">PARAMETERS</span></span>

### <span data-ttu-id="a730a-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="a730a-115">-CertificateId</span></span>
<span data-ttu-id="a730a-116">Определяет ИД сертификата, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="a730a-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="a730a-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="a730a-117">-Context</span></span>
<span data-ttu-id="a730a-118">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="a730a-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a730a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a730a-119">-DefaultProfile</span></span>
<span data-ttu-id="a730a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a730a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a730a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a730a-121">-ResourceId</span></span>
<span data-ttu-id="a730a-122">Идентификатор ресурса Arm сертификата.</span><span class="sxs-lookup"><span data-stu-id="a730a-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="a730a-123">Если он указан, будет пытаться найти сертификат по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="a730a-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="a730a-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="a730a-124">This parameter is required.</span></span>

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

### <span data-ttu-id="a730a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a730a-125">-Confirm</span></span>
<span data-ttu-id="a730a-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a730a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a730a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a730a-127">-WhatIf</span></span>
<span data-ttu-id="a730a-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a730a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a730a-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a730a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a730a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a730a-130">CommonParameters</span></span>
<span data-ttu-id="a730a-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a730a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a730a-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a730a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a730a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a730a-133">INPUTS</span></span>

### <span data-ttu-id="a730a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a730a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a730a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a730a-135">System.String</span></span>

## <span data-ttu-id="a730a-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a730a-136">OUTPUTS</span></span>

### <span data-ttu-id="a730a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a730a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="a730a-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a730a-138">NOTES</span></span>

## <span data-ttu-id="a730a-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a730a-139">RELATED LINKS</span></span>

[<span data-ttu-id="a730a-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a730a-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="a730a-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a730a-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="a730a-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a730a-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


