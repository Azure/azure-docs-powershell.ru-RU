---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412135"
---
# <span data-ttu-id="acc3d-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="acc3d-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="acc3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acc3d-102">SYNOPSIS</span></span>
<span data-ttu-id="acc3d-103">Обновляет набор версий API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="acc3d-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="acc3d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="acc3d-104">SYNTAX</span></span>

### <span data-ttu-id="acc3d-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acc3d-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acc3d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="acc3d-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acc3d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acc3d-107">DESCRIPTION</span></span>

<span data-ttu-id="acc3d-108">Набор версий API управления Azure API изменяется с использованием команды **Set-AzApiManagementApiVersionSet.**</span><span class="sxs-lookup"><span data-stu-id="acc3d-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="acc3d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="acc3d-109">EXAMPLES</span></span>

### <span data-ttu-id="acc3d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="acc3d-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="acc3d-111">Эта команда обновляет существующий набор версий API с помощью схемы управления версиями `Header` и параметра Header. `api-version`</span><span class="sxs-lookup"><span data-stu-id="acc3d-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="acc3d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acc3d-112">PARAMETERS</span></span>

### <span data-ttu-id="acc3d-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="acc3d-113">-ApiVersionSetId</span></span>
<span data-ttu-id="acc3d-114">Идентификатор нового набора версий API.</span><span class="sxs-lookup"><span data-stu-id="acc3d-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="acc3d-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="acc3d-115">-Context</span></span>
<span data-ttu-id="acc3d-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="acc3d-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="acc3d-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="acc3d-117">This parameter is required.</span></span>

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

### <span data-ttu-id="acc3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc3d-118">-DefaultProfile</span></span>
<span data-ttu-id="acc3d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acc3d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc3d-120">-Description</span><span class="sxs-lookup"><span data-stu-id="acc3d-120">-Description</span></span>
<span data-ttu-id="acc3d-121">Описание набора версий Api.</span><span class="sxs-lookup"><span data-stu-id="acc3d-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="acc3d-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="acc3d-122">-HeaderName</span></span>
<span data-ttu-id="acc3d-123">Значение в заглавной области, которое будет содержать сведения об управления версиями.</span><span class="sxs-lookup"><span data-stu-id="acc3d-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="acc3d-124">Если выбран ЗАГЛАВНАЯ СХЕМА управления версиями, это значение должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="acc3d-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="acc3d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acc3d-125">-InputObject</span></span>
<span data-ttu-id="acc3d-126">Экземпляр PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="acc3d-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="acc3d-127">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="acc3d-127">This parameter is required.</span></span>

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

### <span data-ttu-id="acc3d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="acc3d-128">-Name</span></span>
<span data-ttu-id="acc3d-129">Имя набора ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="acc3d-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="acc3d-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="acc3d-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="acc3d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acc3d-131">-PassThru</span></span>
<span data-ttu-id="acc3d-132">Если задан этот экземпляр, экземпляр Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet, представляющий измененный apiVersionSet, будет записан для вывода.</span><span class="sxs-lookup"><span data-stu-id="acc3d-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="acc3d-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="acc3d-133">-QueryName</span></span>
<span data-ttu-id="acc3d-134">Значение запроса, которое будет содержать сведения об версиях.</span><span class="sxs-lookup"><span data-stu-id="acc3d-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="acc3d-135">Если выбран запрос схемы управления версиями, это значение должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="acc3d-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="acc3d-136">-Scheme</span><span class="sxs-lookup"><span data-stu-id="acc3d-136">-Scheme</span></span>
<span data-ttu-id="acc3d-137">Схема управления версиями для выбора набора версий Api.</span><span class="sxs-lookup"><span data-stu-id="acc3d-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="acc3d-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="acc3d-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="acc3d-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acc3d-139">-Confirm</span></span>
<span data-ttu-id="acc3d-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="acc3d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acc3d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acc3d-141">-WhatIf</span></span>
<span data-ttu-id="acc3d-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acc3d-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acc3d-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="acc3d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acc3d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc3d-144">CommonParameters</span></span>
<span data-ttu-id="acc3d-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc3d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc3d-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acc3d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc3d-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acc3d-147">INPUTS</span></span>

### <span data-ttu-id="acc3d-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="acc3d-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="acc3d-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="acc3d-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="acc3d-150">System.String</span><span class="sxs-lookup"><span data-stu-id="acc3d-150">System.String</span></span>

### <span data-ttu-id="acc3d-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="acc3d-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="acc3d-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acc3d-152">OUTPUTS</span></span>

### <span data-ttu-id="acc3d-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="acc3d-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="acc3d-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="acc3d-154">NOTES</span></span>

## <span data-ttu-id="acc3d-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acc3d-155">RELATED LINKS</span></span>

[<span data-ttu-id="acc3d-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="acc3d-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="acc3d-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="acc3d-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="acc3d-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="acc3d-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
