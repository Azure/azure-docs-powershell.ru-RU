---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 1066598a9e255cecbf7238208b5f06f74d88511e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563176"
---
# <span data-ttu-id="9f164-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9f164-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="9f164-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f164-102">SYNOPSIS</span></span>
<span data-ttu-id="9f164-103">Удаление политики управления API из заданной области.</span><span class="sxs-lookup"><span data-stu-id="9f164-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f164-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f164-104">SYNTAX</span></span>

### <span data-ttu-id="9f164-105">RemoveTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f164-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f164-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="9f164-106">RemoveProductLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f164-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="9f164-107">RemoveApiLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f164-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="9f164-108">RemoveOperationLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f164-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f164-109">DESCRIPTION</span></span>
<span data-ttu-id="9f164-110">Командлет **Remove-AzureRmApiManagementPolicy** удаляет политику управления API из указанной области.</span><span class="sxs-lookup"><span data-stu-id="9f164-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="9f164-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f164-111">EXAMPLES</span></span>

### <span data-ttu-id="9f164-112">Пример 1: Удаление политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="9f164-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="9f164-113">Эта команда удаляет политику уровня клиента из управления API.</span><span class="sxs-lookup"><span data-stu-id="9f164-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="9f164-114">Пример 2: Удаление политики уровня продукта</span><span class="sxs-lookup"><span data-stu-id="9f164-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="9f164-115">Эта команда удаляет политику области продукта из управления API.</span><span class="sxs-lookup"><span data-stu-id="9f164-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="9f164-116">Пример 3: Удаление политики области API</span><span class="sxs-lookup"><span data-stu-id="9f164-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="9f164-117">Эта команда удаляет политику области API из управления API.</span><span class="sxs-lookup"><span data-stu-id="9f164-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="9f164-118">Пример 4: Удаление политики области действий</span><span class="sxs-lookup"><span data-stu-id="9f164-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="9f164-119">Эта команда удаляет политику области действия из управления API.</span><span class="sxs-lookup"><span data-stu-id="9f164-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="9f164-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f164-120">PARAMETERS</span></span>

### <span data-ttu-id="9f164-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9f164-121">-ApiId</span></span>
<span data-ttu-id="9f164-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="9f164-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="9f164-123">Если указать этот параметр, командлет удаляет политику области API.</span><span class="sxs-lookup"><span data-stu-id="9f164-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="9f164-124">-Context</span><span class="sxs-lookup"><span data-stu-id="9f164-124">-Context</span></span>
<span data-ttu-id="9f164-125">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9f164-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f164-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f164-126">-DefaultProfile</span></span>
<span data-ttu-id="9f164-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f164-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f164-128">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="9f164-128">-OperationId</span></span>
<span data-ttu-id="9f164-129">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="9f164-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="9f164-130">Если указать этот параметр с помощью параметра *ApiId* , этот командлет удаляет политику области действия.</span><span class="sxs-lookup"><span data-stu-id="9f164-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="9f164-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f164-131">-PassThru</span></span>
<span data-ttu-id="9f164-132">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9f164-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="9f164-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9f164-133">-ProductId</span></span>
<span data-ttu-id="9f164-134">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="9f164-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="9f164-135">Если указать этот параметр, командлет удаляет политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="9f164-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="9f164-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f164-136">-Confirm</span></span>
<span data-ttu-id="9f164-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f164-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f164-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f164-138">-WhatIf</span></span>
<span data-ttu-id="9f164-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f164-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f164-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f164-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f164-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f164-141">CommonParameters</span></span>
<span data-ttu-id="9f164-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f164-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f164-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f164-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f164-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f164-144">INPUTS</span></span>

### <span data-ttu-id="9f164-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9f164-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9f164-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9f164-146">System.String</span></span>

### <span data-ttu-id="9f164-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9f164-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9f164-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f164-148">OUTPUTS</span></span>

### <span data-ttu-id="9f164-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f164-149">System.Boolean</span></span>

## <span data-ttu-id="9f164-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f164-150">NOTES</span></span>

## <span data-ttu-id="9f164-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f164-151">RELATED LINKS</span></span>

[<span data-ttu-id="9f164-152">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9f164-152">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="9f164-153">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9f164-153">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


