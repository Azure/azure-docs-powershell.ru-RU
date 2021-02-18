---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 0e007634659d842b0c59712a2ee191a79e1aeb58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224452"
---
# <span data-ttu-id="ae8dc-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ae8dc-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ae8dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ae8dc-103">Создает набор версий API.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="ae8dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae8dc-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae8dc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae8dc-105">DESCRIPTION</span></span>
<span data-ttu-id="ae8dc-106">Cmdlet **New-AzApiManagementApiVersionSet** создает сущность набора версий API в контексте управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="ae8dc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae8dc-107">EXAMPLES</span></span>

### <span data-ttu-id="ae8dc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae8dc-108">Example 1</span></span>
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

<span data-ttu-id="ae8dc-109">Эта команда создает набор версий API, схему управления версиями `Query` и параметр `api-version` Query.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="ae8dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae8dc-110">PARAMETERS</span></span>

### <span data-ttu-id="ae8dc-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="ae8dc-111">-ApiVersionSetId</span></span>
<span data-ttu-id="ae8dc-112">Идентификатор нового набора версий API.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="ae8dc-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-113">This parameter is optional.</span></span>
<span data-ttu-id="ae8dc-114">Если идентификатор не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="ae8dc-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="ae8dc-115">-Context</span></span>
<span data-ttu-id="ae8dc-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ae8dc-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="ae8dc-117">This parameter is required.</span></span>

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

### <span data-ttu-id="ae8dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae8dc-118">-DefaultProfile</span></span>
<span data-ttu-id="ae8dc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae8dc-120">-Description</span><span class="sxs-lookup"><span data-stu-id="ae8dc-120">-Description</span></span>
<span data-ttu-id="ae8dc-121">Описание набора версий Api.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="ae8dc-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="ae8dc-122">-HeaderName</span></span>
<span data-ttu-id="ae8dc-123">Значение в заглавной области, которое будет содержать сведения об управления версиями.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="ae8dc-124">Если выбран ЗАГЛАВНАЯ СХЕМА управления версиями, это значение должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="ae8dc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ae8dc-125">-Name</span></span>
<span data-ttu-id="ae8dc-126">Имя набора ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="ae8dc-127">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="ae8dc-127">This parameter is required.</span></span>

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

### <span data-ttu-id="ae8dc-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="ae8dc-128">-QueryName</span></span>
<span data-ttu-id="ae8dc-129">Значение запроса, которое будет содержать сведения об версиях.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="ae8dc-130">Если выбран запрос схемы управления версиями, это значение должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="ae8dc-131">-Scheme</span><span class="sxs-lookup"><span data-stu-id="ae8dc-131">-Scheme</span></span>
<span data-ttu-id="ae8dc-132">Схема управления версиями для выбора набора версий Api.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="ae8dc-133">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="ae8dc-133">This parameter is required.</span></span>

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

### <span data-ttu-id="ae8dc-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae8dc-134">-Confirm</span></span>
<span data-ttu-id="ae8dc-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae8dc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae8dc-136">-WhatIf</span></span>
<span data-ttu-id="ae8dc-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae8dc-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae8dc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae8dc-139">CommonParameters</span></span>
<span data-ttu-id="ae8dc-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae8dc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae8dc-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae8dc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae8dc-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae8dc-142">INPUTS</span></span>

### <span data-ttu-id="ae8dc-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ae8dc-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ae8dc-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ae8dc-144">System.String</span></span>

### <span data-ttu-id="ae8dc-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="ae8dc-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="ae8dc-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae8dc-146">OUTPUTS</span></span>

### <span data-ttu-id="ae8dc-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ae8dc-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ae8dc-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae8dc-148">NOTES</span></span>

## <span data-ttu-id="ae8dc-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae8dc-149">RELATED LINKS</span></span>

[<span data-ttu-id="ae8dc-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ae8dc-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="ae8dc-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ae8dc-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="ae8dc-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ae8dc-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)