---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: a51bd7aed5ca8793a921c2cde7729c5280df44b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318737"
---
# <span data-ttu-id="783eb-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="783eb-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="783eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="783eb-102">SYNOPSIS</span></span>
<span data-ttu-id="783eb-103">Удаление политики управления API из заданной области.</span><span class="sxs-lookup"><span data-stu-id="783eb-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="783eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="783eb-104">SYNTAX</span></span>

### <span data-ttu-id="783eb-105">RemoveTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="783eb-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783eb-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="783eb-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783eb-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="783eb-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783eb-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="783eb-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="783eb-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="783eb-109">DESCRIPTION</span></span>
<span data-ttu-id="783eb-110">Командлет **Remove-AzApiManagementPolicy** удаляет политику управления API из указанной области.</span><span class="sxs-lookup"><span data-stu-id="783eb-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="783eb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="783eb-111">EXAMPLES</span></span>

### <span data-ttu-id="783eb-112">Пример 1: Удаление политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="783eb-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="783eb-113">Эта команда удаляет политику уровня клиента из управления API.</span><span class="sxs-lookup"><span data-stu-id="783eb-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="783eb-114">Пример 2: Удаление политики уровня продукта</span><span class="sxs-lookup"><span data-stu-id="783eb-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="783eb-115">Эта команда удаляет политику области продукта из управления API.</span><span class="sxs-lookup"><span data-stu-id="783eb-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="783eb-116">Пример 3: Удаление политики области API</span><span class="sxs-lookup"><span data-stu-id="783eb-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="783eb-117">Эта команда удаляет политику области API из управления API.</span><span class="sxs-lookup"><span data-stu-id="783eb-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="783eb-118">Пример 4: Удаление политики области действий</span><span class="sxs-lookup"><span data-stu-id="783eb-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="783eb-119">Эта команда удаляет политику области действия из управления API.</span><span class="sxs-lookup"><span data-stu-id="783eb-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="783eb-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="783eb-120">PARAMETERS</span></span>

### <span data-ttu-id="783eb-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="783eb-121">-ApiId</span></span>
<span data-ttu-id="783eb-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="783eb-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="783eb-123">Если указать этот параметр, командлет удаляет политику области API.</span><span class="sxs-lookup"><span data-stu-id="783eb-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="783eb-124">-Context</span><span class="sxs-lookup"><span data-stu-id="783eb-124">-Context</span></span>
<span data-ttu-id="783eb-125">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="783eb-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="783eb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783eb-126">-DefaultProfile</span></span>
<span data-ttu-id="783eb-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="783eb-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="783eb-128">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="783eb-128">-OperationId</span></span>
<span data-ttu-id="783eb-129">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="783eb-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="783eb-130">Если указать этот параметр с помощью параметра *ApiId* , этот командлет удаляет политику области действия.</span><span class="sxs-lookup"><span data-stu-id="783eb-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="783eb-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="783eb-131">-PassThru</span></span>
<span data-ttu-id="783eb-132">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="783eb-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="783eb-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="783eb-133">-ProductId</span></span>
<span data-ttu-id="783eb-134">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="783eb-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="783eb-135">Если указать этот параметр, командлет удаляет политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="783eb-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="783eb-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="783eb-136">-Confirm</span></span>
<span data-ttu-id="783eb-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="783eb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="783eb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="783eb-138">-WhatIf</span></span>
<span data-ttu-id="783eb-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="783eb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="783eb-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="783eb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="783eb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783eb-141">CommonParameters</span></span>
<span data-ttu-id="783eb-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="783eb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783eb-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="783eb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783eb-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="783eb-144">INPUTS</span></span>

### <span data-ttu-id="783eb-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="783eb-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="783eb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="783eb-146">System.String</span></span>

### <span data-ttu-id="783eb-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="783eb-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="783eb-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="783eb-148">OUTPUTS</span></span>

### <span data-ttu-id="783eb-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="783eb-149">System.Boolean</span></span>

## <span data-ttu-id="783eb-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="783eb-150">NOTES</span></span>

## <span data-ttu-id="783eb-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="783eb-151">RELATED LINKS</span></span>

[<span data-ttu-id="783eb-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="783eb-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="783eb-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="783eb-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


