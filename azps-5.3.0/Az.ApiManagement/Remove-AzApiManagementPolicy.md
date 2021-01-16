---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: a51bd7aed5ca8793a921c2cde7729c5280df44b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423356"
---
# <span data-ttu-id="f7825-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f7825-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="f7825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7825-102">SYNOPSIS</span></span>
<span data-ttu-id="f7825-103">Удаляет политику управления API из указанной области.</span><span class="sxs-lookup"><span data-stu-id="f7825-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="f7825-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7825-104">SYNTAX</span></span>

### <span data-ttu-id="f7825-105">RemoveTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7825-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7825-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="f7825-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7825-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="f7825-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7825-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="f7825-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7825-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7825-109">DESCRIPTION</span></span>
<span data-ttu-id="f7825-110">При **этом из указанной** области удаляется политика управления API.</span><span class="sxs-lookup"><span data-stu-id="f7825-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="f7825-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7825-111">EXAMPLES</span></span>

### <span data-ttu-id="f7825-112">Пример 1. Удаление политики на уровне клиента</span><span class="sxs-lookup"><span data-stu-id="f7825-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="f7825-113">Эта команда удаляет политику на уровне клиента из управления API.</span><span class="sxs-lookup"><span data-stu-id="f7825-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="f7825-114">Пример 2. Удаление политики области продуктов</span><span class="sxs-lookup"><span data-stu-id="f7825-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="f7825-115">Эта команда удаляет политику области продуктов из управления API.</span><span class="sxs-lookup"><span data-stu-id="f7825-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="f7825-116">Пример 3. Удаление политики области API</span><span class="sxs-lookup"><span data-stu-id="f7825-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="f7825-117">Эта команда удаляет политику области API из управления API.</span><span class="sxs-lookup"><span data-stu-id="f7825-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="f7825-118">Пример 4. Удаление политики области действия</span><span class="sxs-lookup"><span data-stu-id="f7825-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="f7825-119">Эта команда удаляет политику области операций из управления API.</span><span class="sxs-lookup"><span data-stu-id="f7825-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="f7825-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7825-120">PARAMETERS</span></span>

### <span data-ttu-id="f7825-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f7825-121">-ApiId</span></span>
<span data-ttu-id="f7825-122">Определяет идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="f7825-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="f7825-123">Если этот параметр задан, этот cmdlet удаляет политику области API.</span><span class="sxs-lookup"><span data-stu-id="f7825-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="f7825-124">-Контекст</span><span class="sxs-lookup"><span data-stu-id="f7825-124">-Context</span></span>
<span data-ttu-id="f7825-125">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="f7825-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f7825-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7825-126">-DefaultProfile</span></span>
<span data-ttu-id="f7825-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7825-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7825-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f7825-128">-OperationId</span></span>
<span data-ttu-id="f7825-129">Определяет идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="f7825-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="f7825-130">Если указать этот параметр с *параметром ApiId,* этот cmdlet удалит политику области операций.</span><span class="sxs-lookup"><span data-stu-id="f7825-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="f7825-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7825-131">-PassThru</span></span>
<span data-ttu-id="f7825-132">Указывает на то, что этот $True возвращает значение $True, если он успешно, или значение $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f7825-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="f7825-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f7825-133">-ProductId</span></span>
<span data-ttu-id="f7825-134">Определяет идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="f7825-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="f7825-135">Если этот параметр задан, этот cmdlet удаляет политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="f7825-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="f7825-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7825-136">-Confirm</span></span>
<span data-ttu-id="f7825-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7825-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7825-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7825-138">-WhatIf</span></span>
<span data-ttu-id="f7825-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7825-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7825-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f7825-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7825-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7825-141">CommonParameters</span></span>
<span data-ttu-id="f7825-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7825-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7825-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7825-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7825-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7825-144">INPUTS</span></span>

### <span data-ttu-id="f7825-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f7825-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f7825-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f7825-146">System.String</span></span>

### <span data-ttu-id="f7825-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f7825-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f7825-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7825-148">OUTPUTS</span></span>

### <span data-ttu-id="f7825-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7825-149">System.Boolean</span></span>

## <span data-ttu-id="f7825-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7825-150">NOTES</span></span>

## <span data-ttu-id="f7825-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7825-151">RELATED LINKS</span></span>

[<span data-ttu-id="f7825-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f7825-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="f7825-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f7825-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


