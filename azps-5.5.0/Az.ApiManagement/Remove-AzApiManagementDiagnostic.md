---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212121"
---
# <span data-ttu-id="9f6f6-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9f6f6-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="9f6f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6f6-103">Удалите сущность диагностики из глобальной области или уровня API.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="9f6f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f6f6-104">SYNTAX</span></span>

### <span data-ttu-id="9f6f6-105">ByResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f6f6-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f6f6-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9f6f6-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f6f6-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f6f6-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f6f6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f6f6-108">DESCRIPTION</span></span>
<span data-ttu-id="9f6f6-109">С помощью cmdlet **Remove-AzApiManagementDiagnostic** удаляет указанную диагностическую сущность из глобальной области `DiagnosticId` или `ApiId` области.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="9f6f6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f6f6-110">EXAMPLES</span></span>

### <span data-ttu-id="9f6f6-111">Пример 1. Удаление сущности диагностики</span><span class="sxs-lookup"><span data-stu-id="9f6f6-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="9f6f6-112">В этом примере `applicationinsights` диагностика удаляется из службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="9f6f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f6f6-113">PARAMETERS</span></span>

### <span data-ttu-id="9f6f6-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9f6f6-114">-ApiId</span></span>
<span data-ttu-id="9f6f6-115">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-115">Identifier of the API.</span></span>
<span data-ttu-id="9f6f6-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9f6f6-116">This parameter is required.</span></span>

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

### <span data-ttu-id="9f6f6-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="9f6f6-117">-Context</span></span>
<span data-ttu-id="9f6f6-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9f6f6-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9f6f6-119">This parameter is required.</span></span>

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

### <span data-ttu-id="9f6f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6f6-120">-DefaultProfile</span></span>
<span data-ttu-id="9f6f6-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f6f6-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="9f6f6-122">-DiagnosticId</span></span>
<span data-ttu-id="9f6f6-123">Идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-123">Identifier of existing product.</span></span>
<span data-ttu-id="9f6f6-124">Если указано, возвращается политика области продукта.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="9f6f6-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-125">This parameters is optional.</span></span>

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

### <span data-ttu-id="9f6f6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f6f6-126">-InputObject</span></span>
<span data-ttu-id="9f6f6-127">Экземпляр PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="9f6f6-128">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9f6f6-128">This parameter is required.</span></span>

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

### <span data-ttu-id="9f6f6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f6f6-129">-PassThru</span></span>
<span data-ttu-id="9f6f6-130">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9f6f6-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f6f6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f6f6-132">-ResourceId</span></span>
<span data-ttu-id="9f6f6-133">Arm ResourceId диагностики.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="9f6f6-134">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9f6f6-134">This parameter is required.</span></span>

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

### <span data-ttu-id="9f6f6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f6f6-135">-Confirm</span></span>
<span data-ttu-id="9f6f6-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f6f6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6f6-137">-WhatIf</span></span>
<span data-ttu-id="9f6f6-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f6f6-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f6f6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6f6-140">CommonParameters</span></span>
<span data-ttu-id="9f6f6-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6f6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6f6-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f6f6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6f6-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f6f6-143">INPUTS</span></span>

### <span data-ttu-id="9f6f6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9f6f6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9f6f6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9f6f6-145">System.String</span></span>

### <span data-ttu-id="9f6f6-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9f6f6-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9f6f6-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f6f6-147">OUTPUTS</span></span>

### <span data-ttu-id="9f6f6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f6f6-148">System.Boolean</span></span>

## <span data-ttu-id="9f6f6-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f6f6-149">NOTES</span></span>

## <span data-ttu-id="9f6f6-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f6f6-150">RELATED LINKS</span></span>

[<span data-ttu-id="9f6f6-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9f6f6-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9f6f6-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9f6f6-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9f6f6-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9f6f6-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)