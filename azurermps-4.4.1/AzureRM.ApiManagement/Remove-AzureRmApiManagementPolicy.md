---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 5f7fa78cb368afe3e277661122682f43f885f7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558011"
---
# <span data-ttu-id="ad88a-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ad88a-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="ad88a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad88a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad88a-103">Удаление политики управления API из заданной области.</span><span class="sxs-lookup"><span data-stu-id="ad88a-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad88a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad88a-104">SYNTAX</span></span>

### <span data-ttu-id="ad88a-105">Уровень клиента (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad88a-105">Tenant level (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad88a-106">Уровень продукта</span><span class="sxs-lookup"><span data-stu-id="ad88a-106">Product level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad88a-107">Уровень API</span><span class="sxs-lookup"><span data-stu-id="ad88a-107">API level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad88a-108">Уровень операций</span><span class="sxs-lookup"><span data-stu-id="ad88a-108">Operation level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad88a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad88a-109">DESCRIPTION</span></span>
<span data-ttu-id="ad88a-110">Командлет **Remove-AzureRmApiManagementPolicy** удаляет политику управления API из указанной области.</span><span class="sxs-lookup"><span data-stu-id="ad88a-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="ad88a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad88a-111">EXAMPLES</span></span>

### <span data-ttu-id="ad88a-112">Пример 1: Удаление политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="ad88a-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext
```

<span data-ttu-id="ad88a-113">Эта команда удаляет политику уровня клиента из управления API.</span><span class="sxs-lookup"><span data-stu-id="ad88a-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="ad88a-114">Пример 2: Удаление политики уровня продукта</span><span class="sxs-lookup"><span data-stu-id="ad88a-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="ad88a-115">Эта команда удаляет политику области продукта из управления API.</span><span class="sxs-lookup"><span data-stu-id="ad88a-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="ad88a-116">Пример 3: Удаление политики области API</span><span class="sxs-lookup"><span data-stu-id="ad88a-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="ad88a-117">Эта команда удаляет политику области API из управления API.</span><span class="sxs-lookup"><span data-stu-id="ad88a-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="ad88a-118">Пример 4: Удаление политики области действий</span><span class="sxs-lookup"><span data-stu-id="ad88a-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="ad88a-119">Эта команда удаляет политику области действия из управления API.</span><span class="sxs-lookup"><span data-stu-id="ad88a-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="ad88a-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad88a-120">PARAMETERS</span></span>

### <span data-ttu-id="ad88a-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ad88a-121">-ApiId</span></span>
<span data-ttu-id="ad88a-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="ad88a-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="ad88a-123">Если указать этот параметр, командлет удаляет политику области API.</span><span class="sxs-lookup"><span data-stu-id="ad88a-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad88a-124">-Context</span><span class="sxs-lookup"><span data-stu-id="ad88a-124">-Context</span></span>
<span data-ttu-id="ad88a-125">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ad88a-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ad88a-126">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="ad88a-126">-OperationId</span></span>
<span data-ttu-id="ad88a-127">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="ad88a-127">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="ad88a-128">Если указать этот параметр с помощью параметра *ApiId* , этот командлет удаляет политику области действия.</span><span class="sxs-lookup"><span data-stu-id="ad88a-128">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad88a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad88a-129">-PassThru</span></span>
<span data-ttu-id="ad88a-130">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ad88a-130">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="ad88a-131">-ProductId</span><span class="sxs-lookup"><span data-stu-id="ad88a-131">-ProductId</span></span>
<span data-ttu-id="ad88a-132">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="ad88a-132">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="ad88a-133">Если указать этот параметр, командлет удаляет политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="ad88a-133">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad88a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad88a-134">-Confirm</span></span>
<span data-ttu-id="ad88a-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad88a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad88a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad88a-136">-WhatIf</span></span>
<span data-ttu-id="ad88a-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad88a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad88a-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad88a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad88a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad88a-139">-DefaultProfile</span></span>
<span data-ttu-id="ad88a-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad88a-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad88a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad88a-141">CommonParameters</span></span>
<span data-ttu-id="ad88a-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad88a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad88a-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad88a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad88a-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad88a-144">INPUTS</span></span>

## <span data-ttu-id="ad88a-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad88a-145">OUTPUTS</span></span>

### <span data-ttu-id="ad88a-146">Значением</span><span class="sxs-lookup"><span data-stu-id="ad88a-146">Boolean</span></span>

## <span data-ttu-id="ad88a-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad88a-147">NOTES</span></span>

## <span data-ttu-id="ad88a-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad88a-148">RELATED LINKS</span></span>

[<span data-ttu-id="ad88a-149">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ad88a-149">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="ad88a-150">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ad88a-150">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


