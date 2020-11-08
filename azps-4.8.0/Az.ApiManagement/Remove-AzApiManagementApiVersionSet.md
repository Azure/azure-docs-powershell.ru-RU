---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079874"
---
# <span data-ttu-id="b475c-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b475c-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b475c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b475c-102">SYNOPSIS</span></span>
<span data-ttu-id="b475c-103">Удаляет определенный набор версий API</span><span class="sxs-lookup"><span data-stu-id="b475c-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="b475c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b475c-104">SYNTAX</span></span>

### <span data-ttu-id="b475c-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b475c-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b475c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b475c-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b475c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b475c-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b475c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b475c-108">DESCRIPTION</span></span>

<span data-ttu-id="b475c-109">Командлет **Remove-AzAzureRmApiManagementApiVersionSet** удаляет существующий наборы API.</span><span class="sxs-lookup"><span data-stu-id="b475c-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="b475c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b475c-110">EXAMPLES</span></span>

### <span data-ttu-id="b475c-111">Пример 1: Удаление множества версий API</span><span class="sxs-lookup"><span data-stu-id="b475c-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="b475c-112">Эта команда удаляет версию API, установленную с указанным ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="b475c-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="b475c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b475c-113">PARAMETERS</span></span>

### <span data-ttu-id="b475c-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="b475c-114">-ApiVersionSetId</span></span>
<span data-ttu-id="b475c-115">Идентификатор набора версий API.</span><span class="sxs-lookup"><span data-stu-id="b475c-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="b475c-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b475c-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b475c-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b475c-117">-Context</span></span>
<span data-ttu-id="b475c-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b475c-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b475c-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b475c-119">This parameter is required.</span></span>

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

### <span data-ttu-id="b475c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b475c-120">-DefaultProfile</span></span>
<span data-ttu-id="b475c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b475c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b475c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b475c-122">-InputObject</span></span>
<span data-ttu-id="b475c-123">Экземпляр PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="b475c-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="b475c-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b475c-124">This parameter is required.</span></span>

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

### <span data-ttu-id="b475c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b475c-125">-PassThru</span></span>
<span data-ttu-id="b475c-126">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="b475c-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b475c-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b475c-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="b475c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b475c-128">-ResourceId</span></span>
<span data-ttu-id="b475c-129">ИД ResourceId для ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="b475c-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="b475c-130">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b475c-130">This parameter is required.</span></span>

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

### <span data-ttu-id="b475c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b475c-131">-Confirm</span></span>
<span data-ttu-id="b475c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b475c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b475c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b475c-133">-WhatIf</span></span>
<span data-ttu-id="b475c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b475c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b475c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b475c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b475c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b475c-136">CommonParameters</span></span>
<span data-ttu-id="b475c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b475c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b475c-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b475c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b475c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b475c-139">INPUTS</span></span>

### <span data-ttu-id="b475c-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b475c-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b475c-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b475c-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="b475c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b475c-142">System.String</span></span>

## <span data-ttu-id="b475c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b475c-143">OUTPUTS</span></span>

### <span data-ttu-id="b475c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b475c-144">System.Boolean</span></span>

## <span data-ttu-id="b475c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="b475c-145">NOTES</span></span>

## <span data-ttu-id="b475c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b475c-146">RELATED LINKS</span></span>

[<span data-ttu-id="b475c-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b475c-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b475c-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b475c-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b475c-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b475c-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)