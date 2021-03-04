---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: e827fcf43c151f0812d96456de430f57686d4562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959832"
---
# <span data-ttu-id="f1d84-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f1d84-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="f1d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1d84-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d84-103">Задает сведения о продукте для управления API.</span><span class="sxs-lookup"><span data-stu-id="f1d84-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="f1d84-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1d84-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1d84-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1d84-105">DESCRIPTION</span></span>
<span data-ttu-id="f1d84-106">Для управления API задаются сведения о продукте **Set-AzApiManagementProduct.**</span><span class="sxs-lookup"><span data-stu-id="f1d84-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="f1d84-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1d84-107">EXAMPLES</span></span>

### <span data-ttu-id="f1d84-108">Пример 1. Обновление сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="f1d84-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="f1d84-109">Эта команда обновляет сведения об управлении API, требует подписки, а затем отоздает ее.</span><span class="sxs-lookup"><span data-stu-id="f1d84-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="f1d84-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1d84-110">PARAMETERS</span></span>

### <span data-ttu-id="f1d84-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="f1d84-111">-ApprovalRequired</span></span>
<span data-ttu-id="f1d84-112">Указывает, требуется ли утверждение подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="f1d84-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="f1d84-113">Значение по умолчанию — **$False.**</span><span class="sxs-lookup"><span data-stu-id="f1d84-113">The default value is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d84-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="f1d84-114">-Context</span></span>
<span data-ttu-id="f1d84-115">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="f1d84-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f1d84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d84-116">-DefaultProfile</span></span>
<span data-ttu-id="f1d84-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1d84-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1d84-118">-Description</span><span class="sxs-lookup"><span data-stu-id="f1d84-118">-Description</span></span>
<span data-ttu-id="f1d84-119">Описание продукта.</span><span class="sxs-lookup"><span data-stu-id="f1d84-119">Specifies the product description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d84-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="f1d84-120">-LegalTerms</span></span>
<span data-ttu-id="f1d84-121">Определяет законные условия использования продукта.</span><span class="sxs-lookup"><span data-stu-id="f1d84-121">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d84-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1d84-122">-PassThru</span></span>
<span data-ttu-id="f1d84-123">passthru</span><span class="sxs-lookup"><span data-stu-id="f1d84-123">passthru</span></span>

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

### <span data-ttu-id="f1d84-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f1d84-124">-ProductId</span></span>
<span data-ttu-id="f1d84-125">Определяет идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="f1d84-125">Specifies the identifier of the existing product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d84-126">-State</span><span class="sxs-lookup"><span data-stu-id="f1d84-126">-State</span></span>
<span data-ttu-id="f1d84-127">Определяет состояние продукта.</span><span class="sxs-lookup"><span data-stu-id="f1d84-127">Specifies the product state.</span></span>
<span data-ttu-id="f1d84-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="f1d84-128">psdx_paramvalues</span></span>
- <span data-ttu-id="f1d84-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="f1d84-129">NotPublished</span></span>
- <span data-ttu-id="f1d84-130">Опубликовано</span><span class="sxs-lookup"><span data-stu-id="f1d84-130">Published</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases:
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d84-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="f1d84-131">-SubscriptionRequired</span></span>
<span data-ttu-id="f1d84-132">Указывает, требуется ли для продукта подписка.</span><span class="sxs-lookup"><span data-stu-id="f1d84-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="f1d84-133">По умолчанию этот параметр имеет значение **$True.**</span><span class="sxs-lookup"><span data-stu-id="f1d84-133">The default value for this parameter is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d84-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="f1d84-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="f1d84-135">Указывает максимальное количество одновременных подписок.</span><span class="sxs-lookup"><span data-stu-id="f1d84-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="f1d84-136">Значение по умолчанию для этого параметра — "Нет".</span><span class="sxs-lookup"><span data-stu-id="f1d84-136">The default value for this parameter is None.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d84-137">-Title</span><span class="sxs-lookup"><span data-stu-id="f1d84-137">-Title</span></span>
<span data-ttu-id="f1d84-138">Задает название продукта для этого набора cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1d84-138">Specifies the product title this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d84-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1d84-139">-Confirm</span></span>
<span data-ttu-id="f1d84-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1d84-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1d84-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1d84-141">-WhatIf</span></span>
<span data-ttu-id="f1d84-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1d84-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1d84-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f1d84-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1d84-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d84-144">CommonParameters</span></span>
<span data-ttu-id="f1d84-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1d84-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d84-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1d84-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d84-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1d84-147">INPUTS</span></span>

### <span data-ttu-id="f1d84-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1d84-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1d84-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f1d84-149">System.String</span></span>

### <span data-ttu-id="f1d84-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f1d84-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f1d84-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f1d84-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f1d84-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f1d84-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f1d84-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1d84-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1d84-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1d84-154">OUTPUTS</span></span>

### <span data-ttu-id="f1d84-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f1d84-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="f1d84-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1d84-156">NOTES</span></span>

## <span data-ttu-id="f1d84-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1d84-157">RELATED LINKS</span></span>

[<span data-ttu-id="f1d84-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f1d84-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="f1d84-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f1d84-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="f1d84-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f1d84-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


