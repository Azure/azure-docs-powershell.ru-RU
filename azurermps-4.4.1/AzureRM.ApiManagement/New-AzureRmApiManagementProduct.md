---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: a978fce4d44a061796597f2f3ae08c78c1021bdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565721"
---
# <span data-ttu-id="90a97-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="90a97-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="90a97-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90a97-102">SYNOPSIS</span></span>
<span data-ttu-id="90a97-103">Создает продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="90a97-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90a97-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90a97-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90a97-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90a97-105">DESCRIPTION</span></span>
<span data-ttu-id="90a97-106">Командлет **New-AzureRmApiManagementProduct** создает продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="90a97-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="90a97-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90a97-107">EXAMPLES</span></span>

### <span data-ttu-id="90a97-108">Пример 1: создание продукта, для которого не требуется подписка</span><span class="sxs-lookup"><span data-stu-id="90a97-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="90a97-109">Эта команда создает продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="90a97-109">This command creates an API Management product.</span></span>
<span data-ttu-id="90a97-110">Подписка не требуется.</span><span class="sxs-lookup"><span data-stu-id="90a97-110">No subscription is required.</span></span>

### <span data-ttu-id="90a97-111">Пример 2: создание продукта, для которого требуется подписка и утверждение</span><span class="sxs-lookup"><span data-stu-id="90a97-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="90a97-112">Эта команда создает продукт.</span><span class="sxs-lookup"><span data-stu-id="90a97-112">This command creates a product.</span></span>
<span data-ttu-id="90a97-113">Необходимо подписаться на подписку и утверждение.</span><span class="sxs-lookup"><span data-stu-id="90a97-113">A subscription and approval are required.</span></span>
<span data-ttu-id="90a97-114">Эта команда задает период уведомления в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="90a97-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="90a97-115">Срок действия подписки на год равен 1 году.</span><span class="sxs-lookup"><span data-stu-id="90a97-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="90a97-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90a97-116">PARAMETERS</span></span>

### <span data-ttu-id="90a97-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="90a97-117">-ApprovalRequired</span></span>
<span data-ttu-id="90a97-118">Указывает, требуется ли утверждение подписки на продукт или нет.</span><span class="sxs-lookup"><span data-stu-id="90a97-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="90a97-119">По умолчанию этот параметр имеет значение **$false**.</span><span class="sxs-lookup"><span data-stu-id="90a97-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="90a97-120">-Context</span><span class="sxs-lookup"><span data-stu-id="90a97-120">-Context</span></span>
<span data-ttu-id="90a97-121">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="90a97-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="90a97-122">-Описание</span><span class="sxs-lookup"><span data-stu-id="90a97-122">-Description</span></span>
<span data-ttu-id="90a97-123">Указывает описание продукта.</span><span class="sxs-lookup"><span data-stu-id="90a97-123">Specifies the product description.</span></span>

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

### <span data-ttu-id="90a97-124">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="90a97-124">-LegalTerms</span></span>
<span data-ttu-id="90a97-125">Указывает юридические условия использования продукта.</span><span class="sxs-lookup"><span data-stu-id="90a97-125">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="90a97-126">-ProductId</span><span class="sxs-lookup"><span data-stu-id="90a97-126">-ProductId</span></span>
<span data-ttu-id="90a97-127">Указывает идентификатор нового продукта.</span><span class="sxs-lookup"><span data-stu-id="90a97-127">Specifies the identifier of new product.</span></span>
<span data-ttu-id="90a97-128">Если этот параметр не указан, создается новый продукт.</span><span class="sxs-lookup"><span data-stu-id="90a97-128">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="90a97-129">-State</span><span class="sxs-lookup"><span data-stu-id="90a97-129">-State</span></span>
<span data-ttu-id="90a97-130">Задает состояние продукта.</span><span class="sxs-lookup"><span data-stu-id="90a97-130">Specifies the product state.</span></span>
<span data-ttu-id="90a97-131">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="90a97-131">psdx_paramvalues</span></span>

- <span data-ttu-id="90a97-132">NotPublished</span><span class="sxs-lookup"><span data-stu-id="90a97-132">NotPublished</span></span>
- <span data-ttu-id="90a97-133">Отменить</span><span class="sxs-lookup"><span data-stu-id="90a97-133">Published</span></span> 

<span data-ttu-id="90a97-134">Значением по умолчанию является NotPublished.</span><span class="sxs-lookup"><span data-stu-id="90a97-134">The default value is NotPublished.</span></span>

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

### <span data-ttu-id="90a97-135">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="90a97-135">-SubscriptionRequired</span></span>
<span data-ttu-id="90a97-136">Указывает, требуется ли для продукта подписка.</span><span class="sxs-lookup"><span data-stu-id="90a97-136">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="90a97-137">Значение по умолчанию — **$true**.</span><span class="sxs-lookup"><span data-stu-id="90a97-137">The default value is **$True**.</span></span>

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

### <span data-ttu-id="90a97-138">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="90a97-138">-SubscriptionsLimit</span></span>
<span data-ttu-id="90a97-139">Задает максимальное количество одновременных подписок.</span><span class="sxs-lookup"><span data-stu-id="90a97-139">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="90a97-140">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="90a97-140">The default value is 1.</span></span>

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

### <span data-ttu-id="90a97-141">-Title</span><span class="sxs-lookup"><span data-stu-id="90a97-141">-Title</span></span>
<span data-ttu-id="90a97-142">Указывает название продукта.</span><span class="sxs-lookup"><span data-stu-id="90a97-142">Specifies the product title.</span></span>

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

### <span data-ttu-id="90a97-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a97-143">-DefaultProfile</span></span>
<span data-ttu-id="90a97-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90a97-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90a97-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a97-145">CommonParameters</span></span>
<span data-ttu-id="90a97-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90a97-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a97-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a97-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a97-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90a97-148">INPUTS</span></span>

## <span data-ttu-id="90a97-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90a97-149">OUTPUTS</span></span>

### <span data-ttu-id="90a97-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="90a97-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="90a97-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="90a97-151">NOTES</span></span>

## <span data-ttu-id="90a97-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90a97-152">RELATED LINKS</span></span>

[<span data-ttu-id="90a97-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="90a97-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="90a97-154">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="90a97-154">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="90a97-155">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="90a97-155">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


