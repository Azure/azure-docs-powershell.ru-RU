---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239680"
---
# <span data-ttu-id="20df0-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20df0-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="20df0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20df0-102">SYNOPSIS</span></span>
<span data-ttu-id="20df0-103">Обновляет набор версий API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="20df0-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="20df0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="20df0-104">SYNTAX</span></span>

### <span data-ttu-id="20df0-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20df0-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20df0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="20df0-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20df0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20df0-107">DESCRIPTION</span></span>

<span data-ttu-id="20df0-108">Набор версий API управления Azure API изменяется с использованием команды **Set-AzApiManagementApiVersionSet.**</span><span class="sxs-lookup"><span data-stu-id="20df0-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="20df0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="20df0-109">EXAMPLES</span></span>

### <span data-ttu-id="20df0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20df0-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="20df0-111">Эта команда обновляет существующий набор версий API с помощью схемы управления версиями `Header` и параметра Header. `api-version`</span><span class="sxs-lookup"><span data-stu-id="20df0-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="20df0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20df0-112">PARAMETERS</span></span>

### <span data-ttu-id="20df0-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="20df0-113">-ApiVersionSetId</span></span>
<span data-ttu-id="20df0-114">Идентификатор нового набора версий API.</span><span class="sxs-lookup"><span data-stu-id="20df0-114">Identifier for new API Version Set.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20df0-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="20df0-115">-Context</span></span>
<span data-ttu-id="20df0-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="20df0-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="20df0-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="20df0-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20df0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20df0-118">-DefaultProfile</span></span>
<span data-ttu-id="20df0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20df0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20df0-120">-Description</span><span class="sxs-lookup"><span data-stu-id="20df0-120">-Description</span></span>
<span data-ttu-id="20df0-121">Описание набора версий Api.</span><span class="sxs-lookup"><span data-stu-id="20df0-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="20df0-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="20df0-122">-HeaderName</span></span>
<span data-ttu-id="20df0-123">Значение в заглавной области, которое будет содержать сведения об управления версиями.</span><span class="sxs-lookup"><span data-stu-id="20df0-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="20df0-124">Если выбран ЗАГЛАВНАЯ СХЕМА управления версиями, это значение должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="20df0-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="20df0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20df0-125">-InputObject</span></span>
<span data-ttu-id="20df0-126">Экземпляр PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="20df0-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="20df0-127">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="20df0-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20df0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="20df0-128">-Name</span></span>
<span data-ttu-id="20df0-129">Имя набора ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="20df0-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="20df0-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="20df0-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="20df0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20df0-131">-PassThru</span></span>
<span data-ttu-id="20df0-132">Если задан этот экземпляр, экземпляр Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet, представляющий измененный apiVersionSet, будет записан для вывода.</span><span class="sxs-lookup"><span data-stu-id="20df0-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20df0-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="20df0-133">-QueryName</span></span>
<span data-ttu-id="20df0-134">Значение запроса, которое будет содержать сведения об версиях.</span><span class="sxs-lookup"><span data-stu-id="20df0-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="20df0-135">Если выбран запрос схемы управления версиями, это значение должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="20df0-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="20df0-136">-Scheme</span><span class="sxs-lookup"><span data-stu-id="20df0-136">-Scheme</span></span>
<span data-ttu-id="20df0-137">Схема управления версиями для выбора набора версий Api.</span><span class="sxs-lookup"><span data-stu-id="20df0-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="20df0-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="20df0-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20df0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20df0-139">-Confirm</span></span>
<span data-ttu-id="20df0-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="20df0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20df0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20df0-141">-WhatIf</span></span>
<span data-ttu-id="20df0-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20df0-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20df0-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="20df0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20df0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20df0-144">CommonParameters</span></span>
<span data-ttu-id="20df0-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20df0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20df0-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20df0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20df0-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20df0-147">INPUTS</span></span>

### <span data-ttu-id="20df0-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="20df0-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20df0-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20df0-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="20df0-150">System.String</span><span class="sxs-lookup"><span data-stu-id="20df0-150">System.String</span></span>

### <span data-ttu-id="20df0-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="20df0-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="20df0-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="20df0-152">OUTPUTS</span></span>

### <span data-ttu-id="20df0-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20df0-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="20df0-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="20df0-154">NOTES</span></span>

## <span data-ttu-id="20df0-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20df0-155">RELATED LINKS</span></span>

[<span data-ttu-id="20df0-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20df0-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="20df0-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20df0-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="20df0-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="20df0-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
