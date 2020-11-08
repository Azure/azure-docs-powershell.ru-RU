---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: 9bee67dd299163b8e660b0e17c4e3bc11da5b40e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242665"
---
# <span data-ttu-id="59d03-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="59d03-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="59d03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59d03-102">SYNOPSIS</span></span>
<span data-ttu-id="59d03-103">Задает сведения о продукте для управления API.</span><span class="sxs-lookup"><span data-stu-id="59d03-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="59d03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59d03-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d03-105">DESCRIPTION</span></span>
<span data-ttu-id="59d03-106">Командлет **Set-AzApiManagementProduct** задает сведения о продукте для управления API.</span><span class="sxs-lookup"><span data-stu-id="59d03-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="59d03-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59d03-107">EXAMPLES</span></span>

### <span data-ttu-id="59d03-108">Пример 1: обновление сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="59d03-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="59d03-109">Эта команда обновляет сведения о продукте для управления API, требует подписки, а затем отменяет публикацию.</span><span class="sxs-lookup"><span data-stu-id="59d03-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="59d03-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59d03-110">PARAMETERS</span></span>

### <span data-ttu-id="59d03-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="59d03-111">-ApprovalRequired</span></span>
<span data-ttu-id="59d03-112">Указывает, требуется ли утверждение подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="59d03-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="59d03-113">Значение по умолчанию — **$false**.</span><span class="sxs-lookup"><span data-stu-id="59d03-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="59d03-114">-Context</span><span class="sxs-lookup"><span data-stu-id="59d03-114">-Context</span></span>
<span data-ttu-id="59d03-115">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="59d03-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="59d03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d03-116">-DefaultProfile</span></span>
<span data-ttu-id="59d03-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59d03-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59d03-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="59d03-118">-Description</span></span>
<span data-ttu-id="59d03-119">Указывает описание продукта.</span><span class="sxs-lookup"><span data-stu-id="59d03-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="59d03-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="59d03-120">-LegalTerms</span></span>
<span data-ttu-id="59d03-121">Указывает юридические условия использования продукта.</span><span class="sxs-lookup"><span data-stu-id="59d03-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="59d03-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59d03-122">-PassThru</span></span>
<span data-ttu-id="59d03-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="59d03-123">passthru</span></span>

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

### <span data-ttu-id="59d03-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="59d03-124">-ProductId</span></span>
<span data-ttu-id="59d03-125">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="59d03-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="59d03-126">-State</span><span class="sxs-lookup"><span data-stu-id="59d03-126">-State</span></span>
<span data-ttu-id="59d03-127">Задает состояние продукта.</span><span class="sxs-lookup"><span data-stu-id="59d03-127">Specifies the product state.</span></span>
<span data-ttu-id="59d03-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="59d03-128">psdx_paramvalues</span></span>
- <span data-ttu-id="59d03-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="59d03-129">NotPublished</span></span>
- <span data-ttu-id="59d03-130">Отменить</span><span class="sxs-lookup"><span data-stu-id="59d03-130">Published</span></span>

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

### <span data-ttu-id="59d03-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="59d03-131">-SubscriptionRequired</span></span>
<span data-ttu-id="59d03-132">Указывает, требуется ли для продукта подписка.</span><span class="sxs-lookup"><span data-stu-id="59d03-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="59d03-133">Значением по умолчанию для этого параметра является **$true**.</span><span class="sxs-lookup"><span data-stu-id="59d03-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="59d03-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="59d03-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="59d03-135">Задает максимальное количество одновременных подписок.</span><span class="sxs-lookup"><span data-stu-id="59d03-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="59d03-136">Значением по умолчанию для этого параметра является None.</span><span class="sxs-lookup"><span data-stu-id="59d03-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="59d03-137">-Title</span><span class="sxs-lookup"><span data-stu-id="59d03-137">-Title</span></span>
<span data-ttu-id="59d03-138">Задает название продукта, заданное этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="59d03-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="59d03-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59d03-139">-Confirm</span></span>
<span data-ttu-id="59d03-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59d03-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d03-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d03-141">-WhatIf</span></span>
<span data-ttu-id="59d03-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="59d03-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59d03-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="59d03-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d03-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d03-144">CommonParameters</span></span>
<span data-ttu-id="59d03-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59d03-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d03-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59d03-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d03-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59d03-147">INPUTS</span></span>

### <span data-ttu-id="59d03-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="59d03-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="59d03-149">System. String</span><span class="sxs-lookup"><span data-stu-id="59d03-149">System.String</span></span>

### <span data-ttu-id="59d03-150">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="59d03-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="59d03-151">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="59d03-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="59d03-152">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementProductState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="59d03-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="59d03-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="59d03-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="59d03-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d03-154">OUTPUTS</span></span>

### <span data-ttu-id="59d03-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="59d03-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="59d03-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="59d03-156">NOTES</span></span>

## <span data-ttu-id="59d03-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59d03-157">RELATED LINKS</span></span>

[<span data-ttu-id="59d03-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="59d03-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="59d03-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="59d03-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="59d03-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="59d03-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


