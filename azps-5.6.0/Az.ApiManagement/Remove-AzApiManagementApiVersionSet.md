---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 8f505496bc94d7cd0fc4ca69e6a81324a82871d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001955"
---
# <span data-ttu-id="734ff-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="734ff-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="734ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="734ff-102">SYNOPSIS</span></span>
<span data-ttu-id="734ff-103">Удаление определенного набора версий API</span><span class="sxs-lookup"><span data-stu-id="734ff-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="734ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="734ff-104">SYNTAX</span></span>

### <span data-ttu-id="734ff-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="734ff-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="734ff-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="734ff-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="734ff-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="734ff-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="734ff-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="734ff-108">DESCRIPTION</span></span>

<span data-ttu-id="734ff-109">Для **удаления существующего** набора версий API удаляется существующий набор версий API.</span><span class="sxs-lookup"><span data-stu-id="734ff-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="734ff-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="734ff-110">EXAMPLES</span></span>

### <span data-ttu-id="734ff-111">Пример 1. Удаление набора версий API</span><span class="sxs-lookup"><span data-stu-id="734ff-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="734ff-112">Эта команда удаляет набор версий API с указанным ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="734ff-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="734ff-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="734ff-113">PARAMETERS</span></span>

### <span data-ttu-id="734ff-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="734ff-114">-ApiVersionSetId</span></span>
<span data-ttu-id="734ff-115">Идентификатор набора версий API.</span><span class="sxs-lookup"><span data-stu-id="734ff-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="734ff-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="734ff-116">This parameter is required.</span></span>

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

### <span data-ttu-id="734ff-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="734ff-117">-Context</span></span>
<span data-ttu-id="734ff-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="734ff-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="734ff-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="734ff-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="734ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734ff-120">-DefaultProfile</span></span>
<span data-ttu-id="734ff-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="734ff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="734ff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="734ff-122">-InputObject</span></span>
<span data-ttu-id="734ff-123">Экземпляр PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="734ff-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="734ff-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="734ff-124">This parameter is required.</span></span>

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

### <span data-ttu-id="734ff-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="734ff-125">-PassThru</span></span>
<span data-ttu-id="734ff-126">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="734ff-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="734ff-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="734ff-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="734ff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="734ff-128">-ResourceId</span></span>
<span data-ttu-id="734ff-129">Arm ResourceId of ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="734ff-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="734ff-130">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="734ff-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="734ff-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="734ff-131">-Confirm</span></span>
<span data-ttu-id="734ff-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="734ff-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="734ff-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="734ff-133">-WhatIf</span></span>
<span data-ttu-id="734ff-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="734ff-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="734ff-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="734ff-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="734ff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734ff-136">CommonParameters</span></span>
<span data-ttu-id="734ff-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="734ff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734ff-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="734ff-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734ff-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="734ff-139">INPUTS</span></span>

### <span data-ttu-id="734ff-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="734ff-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="734ff-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="734ff-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="734ff-142">System.String</span><span class="sxs-lookup"><span data-stu-id="734ff-142">System.String</span></span>

## <span data-ttu-id="734ff-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="734ff-143">OUTPUTS</span></span>

### <span data-ttu-id="734ff-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="734ff-144">System.Boolean</span></span>

## <span data-ttu-id="734ff-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="734ff-145">NOTES</span></span>

## <span data-ttu-id="734ff-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="734ff-146">RELATED LINKS</span></span>

[<span data-ttu-id="734ff-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="734ff-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="734ff-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="734ff-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="734ff-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="734ff-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)