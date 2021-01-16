---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398764"
---
# <span data-ttu-id="11671-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11671-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="11671-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11671-102">SYNOPSIS</span></span>
<span data-ttu-id="11671-103">Удалите сущность диагностики из глобальной области или уровня API.</span><span class="sxs-lookup"><span data-stu-id="11671-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="11671-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11671-104">SYNTAX</span></span>

### <span data-ttu-id="11671-105">ByResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11671-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11671-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="11671-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11671-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11671-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11671-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11671-108">DESCRIPTION</span></span>
<span data-ttu-id="11671-109">С помощью cmdlet **Remove-AzApiManagementDiagnostic** удаляет диагностическую сущность, указанную в глобальной области `DiagnosticId` или области `ApiId`</span><span class="sxs-lookup"><span data-stu-id="11671-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="11671-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11671-110">EXAMPLES</span></span>

### <span data-ttu-id="11671-111">Пример 1. Удаление сущности диагностики</span><span class="sxs-lookup"><span data-stu-id="11671-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="11671-112">В этом примере `applicationinsights` диагностика удаляется из службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="11671-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="11671-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11671-113">PARAMETERS</span></span>

### <span data-ttu-id="11671-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="11671-114">-ApiId</span></span>
<span data-ttu-id="11671-115">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="11671-115">Identifier of the API.</span></span>
<span data-ttu-id="11671-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="11671-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11671-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="11671-117">-Context</span></span>
<span data-ttu-id="11671-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="11671-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="11671-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="11671-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11671-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11671-120">-DefaultProfile</span></span>
<span data-ttu-id="11671-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11671-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11671-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="11671-122">-DiagnosticId</span></span>
<span data-ttu-id="11671-123">Идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="11671-123">Identifier of existing product.</span></span>
<span data-ttu-id="11671-124">Если указано, возвращается политика области продукта.</span><span class="sxs-lookup"><span data-stu-id="11671-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="11671-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="11671-125">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11671-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11671-126">-InputObject</span></span>
<span data-ttu-id="11671-127">Экземпляр PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="11671-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="11671-128">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="11671-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11671-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11671-129">-PassThru</span></span>
<span data-ttu-id="11671-130">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="11671-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="11671-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="11671-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="11671-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11671-132">-ResourceId</span></span>
<span data-ttu-id="11671-133">Arm ResourceId диагностики.</span><span class="sxs-lookup"><span data-stu-id="11671-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="11671-134">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="11671-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11671-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11671-135">-Confirm</span></span>
<span data-ttu-id="11671-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="11671-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11671-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11671-137">-WhatIf</span></span>
<span data-ttu-id="11671-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11671-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11671-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="11671-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11671-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11671-140">CommonParameters</span></span>
<span data-ttu-id="11671-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11671-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11671-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11671-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11671-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11671-143">INPUTS</span></span>

### <span data-ttu-id="11671-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="11671-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="11671-145">System.String</span><span class="sxs-lookup"><span data-stu-id="11671-145">System.String</span></span>

### <span data-ttu-id="11671-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="11671-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="11671-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11671-147">OUTPUTS</span></span>

### <span data-ttu-id="11671-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11671-148">System.Boolean</span></span>

## <span data-ttu-id="11671-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11671-149">NOTES</span></span>

## <span data-ttu-id="11671-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11671-150">RELATED LINKS</span></span>

[<span data-ttu-id="11671-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11671-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="11671-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11671-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="11671-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11671-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)