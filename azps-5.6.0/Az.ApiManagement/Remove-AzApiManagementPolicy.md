---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: aecf4982b6a48ac5afca1379e1f920cfa3d6e267
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979032"
---
# <span data-ttu-id="305f8-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="305f8-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="305f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="305f8-102">SYNOPSIS</span></span>
<span data-ttu-id="305f8-103">Удаляет политику управления API из указанной области.</span><span class="sxs-lookup"><span data-stu-id="305f8-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="305f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="305f8-104">SYNTAX</span></span>

### <span data-ttu-id="305f8-105">RemoveTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="305f8-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="305f8-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="305f8-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="305f8-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="305f8-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="305f8-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="305f8-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="305f8-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="305f8-109">DESCRIPTION</span></span>
<span data-ttu-id="305f8-110">При **этом из указанной** области удаляется политика управления API.</span><span class="sxs-lookup"><span data-stu-id="305f8-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="305f8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="305f8-111">EXAMPLES</span></span>

### <span data-ttu-id="305f8-112">Пример 1. Удаление политики на уровне клиента</span><span class="sxs-lookup"><span data-stu-id="305f8-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="305f8-113">Эта команда удаляет политику на уровне клиента из управления API.</span><span class="sxs-lookup"><span data-stu-id="305f8-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="305f8-114">Пример 2. Удаление политики области продуктов</span><span class="sxs-lookup"><span data-stu-id="305f8-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="305f8-115">Эта команда удаляет политику области продуктов из управления API.</span><span class="sxs-lookup"><span data-stu-id="305f8-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="305f8-116">Пример 3. Удаление политики области API</span><span class="sxs-lookup"><span data-stu-id="305f8-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="305f8-117">Эта команда удаляет политику области API из управления API.</span><span class="sxs-lookup"><span data-stu-id="305f8-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="305f8-118">Пример 4. Удаление политики области действия</span><span class="sxs-lookup"><span data-stu-id="305f8-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="305f8-119">Эта команда удаляет политику области операций из управления API.</span><span class="sxs-lookup"><span data-stu-id="305f8-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="305f8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="305f8-120">PARAMETERS</span></span>

### <span data-ttu-id="305f8-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="305f8-121">-ApiId</span></span>
<span data-ttu-id="305f8-122">Определяет идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="305f8-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="305f8-123">При указании этого параметра cmdlet удаляет политику области API.</span><span class="sxs-lookup"><span data-stu-id="305f8-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="305f8-124">-Контекст</span><span class="sxs-lookup"><span data-stu-id="305f8-124">-Context</span></span>
<span data-ttu-id="305f8-125">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="305f8-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="305f8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305f8-126">-DefaultProfile</span></span>
<span data-ttu-id="305f8-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="305f8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="305f8-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="305f8-128">-OperationId</span></span>
<span data-ttu-id="305f8-129">Определяет идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="305f8-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="305f8-130">Если указать этот параметр с *параметром ApiId,* этот cmdlet удалит политику области операций.</span><span class="sxs-lookup"><span data-stu-id="305f8-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="305f8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="305f8-131">-PassThru</span></span>
<span data-ttu-id="305f8-132">Указывает на то, что этот $True возвращает значение $True, если он успешно, или значение $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="305f8-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="305f8-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="305f8-133">-ProductId</span></span>
<span data-ttu-id="305f8-134">Определяет идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="305f8-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="305f8-135">Если этот параметр задан, этот cmdlet удаляет политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="305f8-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="305f8-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="305f8-136">-Confirm</span></span>
<span data-ttu-id="305f8-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="305f8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="305f8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="305f8-138">-WhatIf</span></span>
<span data-ttu-id="305f8-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="305f8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="305f8-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="305f8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="305f8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305f8-141">CommonParameters</span></span>
<span data-ttu-id="305f8-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="305f8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305f8-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="305f8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305f8-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="305f8-144">INPUTS</span></span>

### <span data-ttu-id="305f8-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="305f8-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="305f8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="305f8-146">System.String</span></span>

### <span data-ttu-id="305f8-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="305f8-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="305f8-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="305f8-148">OUTPUTS</span></span>

### <span data-ttu-id="305f8-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="305f8-149">System.Boolean</span></span>

## <span data-ttu-id="305f8-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="305f8-150">NOTES</span></span>

## <span data-ttu-id="305f8-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="305f8-151">RELATED LINKS</span></span>

[<span data-ttu-id="305f8-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="305f8-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="305f8-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="305f8-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


