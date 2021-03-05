---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 126f30e732bc9c55c78c94d6c802b05a18ce29db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993093"
---
# <span data-ttu-id="e0cf9-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e0cf9-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="e0cf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="e0cf9-103">Создание набора версий API.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="e0cf9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0cf9-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0cf9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="e0cf9-106">Cmdlet **New-AzApiManagementApiVersionSet** создает сущность набора версий API в контексте управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="e0cf9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0cf9-107">EXAMPLES</span></span>

### <span data-ttu-id="e0cf9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0cf9-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="e0cf9-109">Эта команда создает набор версий API, схему управления версиями `Query` и параметр `api-version` Query.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="e0cf9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0cf9-110">PARAMETERS</span></span>

### <span data-ttu-id="e0cf9-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="e0cf9-111">-ApiVersionSetId</span></span>
<span data-ttu-id="e0cf9-112">Идентификатор нового набора версий API.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="e0cf9-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-113">This parameter is optional.</span></span>
<span data-ttu-id="e0cf9-114">Если идентификатор не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="e0cf9-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="e0cf9-115">-Context</span></span>
<span data-ttu-id="e0cf9-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e0cf9-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="e0cf9-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0cf9-118">-DefaultProfile</span></span>
<span data-ttu-id="e0cf9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0cf9-120">-Description</span><span class="sxs-lookup"><span data-stu-id="e0cf9-120">-Description</span></span>
<span data-ttu-id="e0cf9-121">Описание набора версий Api.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="e0cf9-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="e0cf9-122">-HeaderName</span></span>
<span data-ttu-id="e0cf9-123">Значение в заглавной области, которое будет содержать сведения об управления версиями.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="e0cf9-124">Если выбран ЗАГЛАВНАЯ СХЕМА управления версиями, это значение должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="e0cf9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e0cf9-125">-Name</span></span>
<span data-ttu-id="e0cf9-126">Имя набора ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="e0cf9-127">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="e0cf9-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e0cf9-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="e0cf9-128">-QueryName</span></span>
<span data-ttu-id="e0cf9-129">Значение запроса, которое будет содержать сведения об версиях.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="e0cf9-130">Если выбран запрос схемы управления версиями, это значение должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="e0cf9-131">-Scheme</span><span class="sxs-lookup"><span data-stu-id="e0cf9-131">-Scheme</span></span>
<span data-ttu-id="e0cf9-132">Схема управления версиями для выбора набора версий Api.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="e0cf9-133">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="e0cf9-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0cf9-134">-Confirm</span></span>
<span data-ttu-id="e0cf9-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0cf9-136">-WhatIf</span></span>
<span data-ttu-id="e0cf9-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0cf9-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0cf9-139">CommonParameters</span></span>
<span data-ttu-id="e0cf9-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0cf9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0cf9-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0cf9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0cf9-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0cf9-142">INPUTS</span></span>

### <span data-ttu-id="e0cf9-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e0cf9-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e0cf9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e0cf9-144">System.String</span></span>

### <span data-ttu-id="e0cf9-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="e0cf9-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="e0cf9-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0cf9-146">OUTPUTS</span></span>

### <span data-ttu-id="e0cf9-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e0cf9-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="e0cf9-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0cf9-148">NOTES</span></span>

## <span data-ttu-id="e0cf9-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0cf9-149">RELATED LINKS</span></span>

[<span data-ttu-id="e0cf9-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e0cf9-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="e0cf9-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e0cf9-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="e0cf9-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e0cf9-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)