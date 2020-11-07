---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: b050b55c978313cf038e8a27d5be0f7ad722905b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734733"
---
# <span data-ttu-id="591ae-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="591ae-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="591ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="591ae-102">SYNOPSIS</span></span>
<span data-ttu-id="591ae-103">Задает сведения о продукте для управления API.</span><span class="sxs-lookup"><span data-stu-id="591ae-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="591ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="591ae-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="591ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="591ae-105">DESCRIPTION</span></span>
<span data-ttu-id="591ae-106">Командлет **Set-AzureRmApiManagementProduct** задает сведения о продукте для управления API.</span><span class="sxs-lookup"><span data-stu-id="591ae-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="591ae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="591ae-107">EXAMPLES</span></span>

### <span data-ttu-id="591ae-108">Пример 1: обновление сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="591ae-108">Example 1: Update the product details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="591ae-109">Эта команда обновляет сведения о продукте для управления API, требует подписки, а затем отменяет публикацию.</span><span class="sxs-lookup"><span data-stu-id="591ae-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="591ae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="591ae-110">PARAMETERS</span></span>

### <span data-ttu-id="591ae-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="591ae-111">-ApprovalRequired</span></span>
<span data-ttu-id="591ae-112">Указывает, требуется ли утверждение подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="591ae-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="591ae-113">Значение по умолчанию — **$false**.</span><span class="sxs-lookup"><span data-stu-id="591ae-113">The default value is **$False**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-114">-Context</span><span class="sxs-lookup"><span data-stu-id="591ae-114">-Context</span></span>
<span data-ttu-id="591ae-115">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="591ae-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591ae-116">-DefaultProfile</span></span>
<span data-ttu-id="591ae-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="591ae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="591ae-118">-Description</span></span>
<span data-ttu-id="591ae-119">Указывает описание продукта.</span><span class="sxs-lookup"><span data-stu-id="591ae-119">Specifies the product description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="591ae-120">-LegalTerms</span></span>
<span data-ttu-id="591ae-121">Указывает юридические условия использования продукта.</span><span class="sxs-lookup"><span data-stu-id="591ae-121">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="591ae-122">-PassThru</span></span>
<span data-ttu-id="591ae-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="591ae-123">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="591ae-124">-ProductId</span></span>
<span data-ttu-id="591ae-125">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="591ae-125">Specifies the identifier of the existing product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-126">-State</span><span class="sxs-lookup"><span data-stu-id="591ae-126">-State</span></span>
<span data-ttu-id="591ae-127">Задает состояние продукта.</span><span class="sxs-lookup"><span data-stu-id="591ae-127">Specifies the product state.</span></span>
<span data-ttu-id="591ae-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="591ae-128">psdx_paramvalues</span></span>

- <span data-ttu-id="591ae-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="591ae-129">NotPublished</span></span>
- <span data-ttu-id="591ae-130">Отменить</span><span class="sxs-lookup"><span data-stu-id="591ae-130">Published</span></span>

```yaml
Type: PsApiManagementProductState
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="591ae-131">-SubscriptionRequired</span></span>
<span data-ttu-id="591ae-132">Указывает, требуется ли для продукта подписка.</span><span class="sxs-lookup"><span data-stu-id="591ae-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="591ae-133">Значением по умолчанию для этого параметра является **$true**.</span><span class="sxs-lookup"><span data-stu-id="591ae-133">The default value for this parameter is **$True**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="591ae-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="591ae-135">Задает максимальное количество одновременных подписок.</span><span class="sxs-lookup"><span data-stu-id="591ae-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="591ae-136">Значением по умолчанию для этого параметра является 1.</span><span class="sxs-lookup"><span data-stu-id="591ae-136">The default value for this parameter is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-137">-Title</span><span class="sxs-lookup"><span data-stu-id="591ae-137">-Title</span></span>
<span data-ttu-id="591ae-138">Задает название продукта, заданное этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="591ae-138">Specifies the product title this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591ae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591ae-139">CommonParameters</span></span>
<span data-ttu-id="591ae-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="591ae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591ae-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591ae-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591ae-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="591ae-142">INPUTS</span></span>

### <span data-ttu-id="591ae-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="591ae-143">None</span></span>
<span data-ttu-id="591ae-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="591ae-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="591ae-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="591ae-145">OUTPUTS</span></span>

### <span data-ttu-id="591ae-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="591ae-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="591ae-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="591ae-147">NOTES</span></span>

## <span data-ttu-id="591ae-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="591ae-148">RELATED LINKS</span></span>

[<span data-ttu-id="591ae-149">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="591ae-149">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="591ae-150">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="591ae-150">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="591ae-151">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="591ae-151">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


