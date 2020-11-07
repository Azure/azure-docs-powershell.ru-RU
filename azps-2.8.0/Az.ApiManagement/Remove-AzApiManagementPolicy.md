---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: c4f2ce8db3a799ad3d49d1c967da93a8fea93a39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727977"
---
# <span data-ttu-id="521ad-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="521ad-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="521ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="521ad-102">SYNOPSIS</span></span>
<span data-ttu-id="521ad-103">Удаление политики управления API из заданной области.</span><span class="sxs-lookup"><span data-stu-id="521ad-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="521ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="521ad-104">SYNTAX</span></span>

### <span data-ttu-id="521ad-105">RemoveTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="521ad-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="521ad-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="521ad-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="521ad-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="521ad-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="521ad-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="521ad-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="521ad-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="521ad-109">DESCRIPTION</span></span>
<span data-ttu-id="521ad-110">Командлет **Remove-AzApiManagementPolicy** удаляет политику управления API из указанной области.</span><span class="sxs-lookup"><span data-stu-id="521ad-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="521ad-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="521ad-111">EXAMPLES</span></span>

### <span data-ttu-id="521ad-112">Пример 1: Удаление политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="521ad-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="521ad-113">Эта команда удаляет политику уровня клиента из управления API.</span><span class="sxs-lookup"><span data-stu-id="521ad-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="521ad-114">Пример 2: Удаление политики уровня продукта</span><span class="sxs-lookup"><span data-stu-id="521ad-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="521ad-115">Эта команда удаляет политику области продукта из управления API.</span><span class="sxs-lookup"><span data-stu-id="521ad-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="521ad-116">Пример 3: Удаление политики области API</span><span class="sxs-lookup"><span data-stu-id="521ad-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="521ad-117">Эта команда удаляет политику области API из управления API.</span><span class="sxs-lookup"><span data-stu-id="521ad-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="521ad-118">Пример 4: Удаление политики области действий</span><span class="sxs-lookup"><span data-stu-id="521ad-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="521ad-119">Эта команда удаляет политику области действия из управления API.</span><span class="sxs-lookup"><span data-stu-id="521ad-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="521ad-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="521ad-120">PARAMETERS</span></span>

### <span data-ttu-id="521ad-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="521ad-121">-ApiId</span></span>
<span data-ttu-id="521ad-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="521ad-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="521ad-123">Если указать этот параметр, командлет удаляет политику области API.</span><span class="sxs-lookup"><span data-stu-id="521ad-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="521ad-124">-Context</span><span class="sxs-lookup"><span data-stu-id="521ad-124">-Context</span></span>
<span data-ttu-id="521ad-125">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="521ad-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="521ad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521ad-126">-DefaultProfile</span></span>
<span data-ttu-id="521ad-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="521ad-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="521ad-128">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="521ad-128">-OperationId</span></span>
<span data-ttu-id="521ad-129">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="521ad-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="521ad-130">Если указать этот параметр с помощью параметра *ApiId* , этот командлет удаляет политику области действия.</span><span class="sxs-lookup"><span data-stu-id="521ad-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="521ad-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="521ad-131">-PassThru</span></span>
<span data-ttu-id="521ad-132">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="521ad-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="521ad-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="521ad-133">-ProductId</span></span>
<span data-ttu-id="521ad-134">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="521ad-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="521ad-135">Если указать этот параметр, командлет удаляет политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="521ad-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="521ad-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="521ad-136">-Confirm</span></span>
<span data-ttu-id="521ad-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="521ad-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="521ad-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="521ad-138">-WhatIf</span></span>
<span data-ttu-id="521ad-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="521ad-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="521ad-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="521ad-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="521ad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521ad-141">CommonParameters</span></span>
<span data-ttu-id="521ad-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="521ad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521ad-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="521ad-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521ad-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="521ad-144">INPUTS</span></span>

### <span data-ttu-id="521ad-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="521ad-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="521ad-146">System. String</span><span class="sxs-lookup"><span data-stu-id="521ad-146">System.String</span></span>

### <span data-ttu-id="521ad-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="521ad-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="521ad-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="521ad-148">OUTPUTS</span></span>

### <span data-ttu-id="521ad-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="521ad-149">System.Boolean</span></span>

## <span data-ttu-id="521ad-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="521ad-150">NOTES</span></span>

## <span data-ttu-id="521ad-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="521ad-151">RELATED LINKS</span></span>

[<span data-ttu-id="521ad-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="521ad-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="521ad-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="521ad-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


