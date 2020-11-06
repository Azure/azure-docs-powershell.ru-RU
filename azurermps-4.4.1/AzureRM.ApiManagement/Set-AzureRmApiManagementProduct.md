---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: dac6e48faba1590897161ab59fed05f1f0b331df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565712"
---
# <span data-ttu-id="95e2a-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="95e2a-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="95e2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="95e2a-103">Задает сведения о продукте для управления API.</span><span class="sxs-lookup"><span data-stu-id="95e2a-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95e2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95e2a-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95e2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95e2a-105">DESCRIPTION</span></span>
<span data-ttu-id="95e2a-106">Командлет **Set-AzureRmApiManagementProduct** задает сведения о продукте для управления API.</span><span class="sxs-lookup"><span data-stu-id="95e2a-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="95e2a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95e2a-107">EXAMPLES</span></span>

### <span data-ttu-id="95e2a-108">Пример 1: обновление сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="95e2a-108">Example 1: Update the product details</span></span>
```
PS C:\>Set-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="95e2a-109">Эта команда обновляет сведения о продукте для управления API, требует подписки, а затем отменяет публикацию.</span><span class="sxs-lookup"><span data-stu-id="95e2a-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="95e2a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95e2a-110">PARAMETERS</span></span>

### <span data-ttu-id="95e2a-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="95e2a-111">-ApprovalRequired</span></span>
<span data-ttu-id="95e2a-112">Указывает, требуется ли утверждение подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="95e2a-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="95e2a-113">Значение по умолчанию — **$false**.</span><span class="sxs-lookup"><span data-stu-id="95e2a-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="95e2a-114">-Context</span><span class="sxs-lookup"><span data-stu-id="95e2a-114">-Context</span></span>
<span data-ttu-id="95e2a-115">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="95e2a-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="95e2a-116">-Описание</span><span class="sxs-lookup"><span data-stu-id="95e2a-116">-Description</span></span>
<span data-ttu-id="95e2a-117">Указывает описание продукта.</span><span class="sxs-lookup"><span data-stu-id="95e2a-117">Specifies the product description.</span></span>

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

### <span data-ttu-id="95e2a-118">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="95e2a-118">-LegalTerms</span></span>
<span data-ttu-id="95e2a-119">Указывает юридические условия использования продукта.</span><span class="sxs-lookup"><span data-stu-id="95e2a-119">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="95e2a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95e2a-120">-PassThru</span></span>
<span data-ttu-id="95e2a-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="95e2a-121">passthru</span></span>

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

### <span data-ttu-id="95e2a-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="95e2a-122">-ProductId</span></span>
<span data-ttu-id="95e2a-123">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="95e2a-123">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="95e2a-124">-State</span><span class="sxs-lookup"><span data-stu-id="95e2a-124">-State</span></span>
<span data-ttu-id="95e2a-125">Задает состояние продукта.</span><span class="sxs-lookup"><span data-stu-id="95e2a-125">Specifies the product state.</span></span>
<span data-ttu-id="95e2a-126">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="95e2a-126">psdx_paramvalues</span></span>

- <span data-ttu-id="95e2a-127">NotPublished</span><span class="sxs-lookup"><span data-stu-id="95e2a-127">NotPublished</span></span>
- <span data-ttu-id="95e2a-128">Отменить</span><span class="sxs-lookup"><span data-stu-id="95e2a-128">Published</span></span>

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

### <span data-ttu-id="95e2a-129">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="95e2a-129">-SubscriptionRequired</span></span>
<span data-ttu-id="95e2a-130">Указывает, требуется ли для продукта подписка.</span><span class="sxs-lookup"><span data-stu-id="95e2a-130">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="95e2a-131">Значением по умолчанию для этого параметра является **$true**.</span><span class="sxs-lookup"><span data-stu-id="95e2a-131">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="95e2a-132">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="95e2a-132">-SubscriptionsLimit</span></span>
<span data-ttu-id="95e2a-133">Задает максимальное количество одновременных подписок.</span><span class="sxs-lookup"><span data-stu-id="95e2a-133">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="95e2a-134">Значением по умолчанию для этого параметра является 1.</span><span class="sxs-lookup"><span data-stu-id="95e2a-134">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="95e2a-135">-Title</span><span class="sxs-lookup"><span data-stu-id="95e2a-135">-Title</span></span>
<span data-ttu-id="95e2a-136">Задает название продукта, заданное этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="95e2a-136">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="95e2a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e2a-137">-DefaultProfile</span></span>
<span data-ttu-id="95e2a-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95e2a-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95e2a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e2a-139">CommonParameters</span></span>
<span data-ttu-id="95e2a-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95e2a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e2a-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95e2a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e2a-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95e2a-142">INPUTS</span></span>

## <span data-ttu-id="95e2a-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95e2a-143">OUTPUTS</span></span>

### <span data-ttu-id="95e2a-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="95e2a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="95e2a-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="95e2a-145">NOTES</span></span>

## <span data-ttu-id="95e2a-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95e2a-146">RELATED LINKS</span></span>

[<span data-ttu-id="95e2a-147">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="95e2a-147">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="95e2a-148">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="95e2a-148">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="95e2a-149">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="95e2a-149">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


