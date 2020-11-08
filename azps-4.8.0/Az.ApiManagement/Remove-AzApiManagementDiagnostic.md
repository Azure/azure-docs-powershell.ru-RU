---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078555"
---
# <span data-ttu-id="256aa-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="256aa-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="256aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="256aa-102">SYNOPSIS</span></span>
<span data-ttu-id="256aa-103">Удалите объект диагностики из области Global или уровня API.</span><span class="sxs-lookup"><span data-stu-id="256aa-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="256aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="256aa-104">SYNTAX</span></span>

### <span data-ttu-id="256aa-105">ByResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="256aa-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="256aa-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="256aa-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="256aa-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="256aa-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="256aa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="256aa-108">DESCRIPTION</span></span>
<span data-ttu-id="256aa-109">Командлет **Remove-AzApiManagementDiagnostic** удаляет объект диагностики, указанный `DiagnosticId` в глобальной области или области. `ApiId`</span><span class="sxs-lookup"><span data-stu-id="256aa-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="256aa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="256aa-110">EXAMPLES</span></span>

### <span data-ttu-id="256aa-111">Пример 1: удаление объекта диагностики</span><span class="sxs-lookup"><span data-stu-id="256aa-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="256aa-112">В этом примере удаляется диагностика `applicationinsights` из службы управления API.</span><span class="sxs-lookup"><span data-stu-id="256aa-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="256aa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="256aa-113">PARAMETERS</span></span>

### <span data-ttu-id="256aa-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="256aa-114">-ApiId</span></span>
<span data-ttu-id="256aa-115">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="256aa-115">Identifier of the API.</span></span>
<span data-ttu-id="256aa-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="256aa-116">This parameter is required.</span></span>

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

### <span data-ttu-id="256aa-117">-Context</span><span class="sxs-lookup"><span data-stu-id="256aa-117">-Context</span></span>
<span data-ttu-id="256aa-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="256aa-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="256aa-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="256aa-119">This parameter is required.</span></span>

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

### <span data-ttu-id="256aa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="256aa-120">-DefaultProfile</span></span>
<span data-ttu-id="256aa-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="256aa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="256aa-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="256aa-122">-DiagnosticId</span></span>
<span data-ttu-id="256aa-123">Идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="256aa-123">Identifier of existing product.</span></span>
<span data-ttu-id="256aa-124">Если задано, будет возвращена политика области продукта.</span><span class="sxs-lookup"><span data-stu-id="256aa-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="256aa-125">Эти параметры являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="256aa-125">This parameters is optional.</span></span>

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

### <span data-ttu-id="256aa-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="256aa-126">-InputObject</span></span>
<span data-ttu-id="256aa-127">Экземпляр PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="256aa-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="256aa-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="256aa-128">This parameter is required.</span></span>

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

### <span data-ttu-id="256aa-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="256aa-129">-PassThru</span></span>
<span data-ttu-id="256aa-130">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="256aa-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="256aa-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="256aa-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="256aa-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="256aa-132">-ResourceId</span></span>
<span data-ttu-id="256aa-133">ResourceId (ИД) для диагностики.</span><span class="sxs-lookup"><span data-stu-id="256aa-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="256aa-134">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="256aa-134">This parameter is required.</span></span>

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

### <span data-ttu-id="256aa-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="256aa-135">-Confirm</span></span>
<span data-ttu-id="256aa-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="256aa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="256aa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="256aa-137">-WhatIf</span></span>
<span data-ttu-id="256aa-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="256aa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="256aa-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="256aa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="256aa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="256aa-140">CommonParameters</span></span>
<span data-ttu-id="256aa-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="256aa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="256aa-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="256aa-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="256aa-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="256aa-143">INPUTS</span></span>

### <span data-ttu-id="256aa-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="256aa-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="256aa-145">System. String</span><span class="sxs-lookup"><span data-stu-id="256aa-145">System.String</span></span>

### <span data-ttu-id="256aa-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="256aa-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="256aa-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="256aa-147">OUTPUTS</span></span>

### <span data-ttu-id="256aa-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="256aa-148">System.Boolean</span></span>

## <span data-ttu-id="256aa-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="256aa-149">NOTES</span></span>

## <span data-ttu-id="256aa-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="256aa-150">RELATED LINKS</span></span>

[<span data-ttu-id="256aa-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="256aa-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="256aa-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="256aa-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="256aa-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="256aa-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)