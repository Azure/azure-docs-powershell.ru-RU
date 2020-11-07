---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: f28bfc223ed187724aa8702c378bfce5d88755fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732126"
---
# <span data-ttu-id="f8f09-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f8f09-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="f8f09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8f09-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f09-103">Задает сведения о продукте для управления API.</span><span class="sxs-lookup"><span data-stu-id="f8f09-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8f09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8f09-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8f09-105">DESCRIPTION</span></span>
<span data-ttu-id="f8f09-106">Командлет **Set-AzureRmApiManagementProduct** задает сведения о продукте для управления API.</span><span class="sxs-lookup"><span data-stu-id="f8f09-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="f8f09-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8f09-107">EXAMPLES</span></span>

### <span data-ttu-id="f8f09-108">Пример 1: обновление сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="f8f09-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="f8f09-109">Эта команда обновляет сведения о продукте для управления API, требует подписки, а затем отменяет публикацию.</span><span class="sxs-lookup"><span data-stu-id="f8f09-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="f8f09-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8f09-110">PARAMETERS</span></span>

### <span data-ttu-id="f8f09-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="f8f09-111">-ApprovalRequired</span></span>
<span data-ttu-id="f8f09-112">Указывает, требуется ли утверждение подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="f8f09-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="f8f09-113">Значение по умолчанию — **$false**.</span><span class="sxs-lookup"><span data-stu-id="f8f09-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="f8f09-114">-Context</span><span class="sxs-lookup"><span data-stu-id="f8f09-114">-Context</span></span>
<span data-ttu-id="f8f09-115">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f8f09-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f8f09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f09-116">-DefaultProfile</span></span>
<span data-ttu-id="f8f09-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8f09-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8f09-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="f8f09-118">-Description</span></span>
<span data-ttu-id="f8f09-119">Указывает описание продукта.</span><span class="sxs-lookup"><span data-stu-id="f8f09-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="f8f09-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="f8f09-120">-LegalTerms</span></span>
<span data-ttu-id="f8f09-121">Указывает юридические условия использования продукта.</span><span class="sxs-lookup"><span data-stu-id="f8f09-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="f8f09-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8f09-122">-PassThru</span></span>
<span data-ttu-id="f8f09-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="f8f09-123">passthru</span></span>

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

### <span data-ttu-id="f8f09-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f8f09-124">-ProductId</span></span>
<span data-ttu-id="f8f09-125">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="f8f09-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="f8f09-126">-State</span><span class="sxs-lookup"><span data-stu-id="f8f09-126">-State</span></span>
<span data-ttu-id="f8f09-127">Задает состояние продукта.</span><span class="sxs-lookup"><span data-stu-id="f8f09-127">Specifies the product state.</span></span>
<span data-ttu-id="f8f09-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="f8f09-128">psdx_paramvalues</span></span>
- <span data-ttu-id="f8f09-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="f8f09-129">NotPublished</span></span>
- <span data-ttu-id="f8f09-130">Отменить</span><span class="sxs-lookup"><span data-stu-id="f8f09-130">Published</span></span>

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

### <span data-ttu-id="f8f09-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="f8f09-131">-SubscriptionRequired</span></span>
<span data-ttu-id="f8f09-132">Указывает, требуется ли для продукта подписка.</span><span class="sxs-lookup"><span data-stu-id="f8f09-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="f8f09-133">Значением по умолчанию для этого параметра является **$true**.</span><span class="sxs-lookup"><span data-stu-id="f8f09-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="f8f09-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="f8f09-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="f8f09-135">Задает максимальное количество одновременных подписок.</span><span class="sxs-lookup"><span data-stu-id="f8f09-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="f8f09-136">Значением по умолчанию для этого параметра является 1.</span><span class="sxs-lookup"><span data-stu-id="f8f09-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="f8f09-137">-Title</span><span class="sxs-lookup"><span data-stu-id="f8f09-137">-Title</span></span>
<span data-ttu-id="f8f09-138">Задает название продукта, заданное этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f8f09-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="f8f09-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f09-139">CommonParameters</span></span>
<span data-ttu-id="f8f09-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8f09-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f09-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f09-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f09-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8f09-142">INPUTS</span></span>

### <span data-ttu-id="f8f09-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f8f09-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f8f09-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f8f09-144">System.String</span></span>

### <span data-ttu-id="f8f09-145">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f8f09-145">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f8f09-146">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f8f09-146">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f8f09-147">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProductState, Microsoft. Azure. Commands. ApiManagement. ServiceManagement, Version = 6.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="f8f09-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f8f09-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f8f09-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f8f09-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8f09-149">OUTPUTS</span></span>

### <span data-ttu-id="f8f09-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f8f09-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="f8f09-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8f09-151">NOTES</span></span>

## <span data-ttu-id="f8f09-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8f09-152">RELATED LINKS</span></span>

[<span data-ttu-id="f8f09-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f8f09-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="f8f09-154">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f8f09-154">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="f8f09-155">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f8f09-155">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


