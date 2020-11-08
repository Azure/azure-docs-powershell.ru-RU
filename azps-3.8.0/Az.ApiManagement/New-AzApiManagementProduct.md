---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 3d14ef7dca35796baa3e3aecf0c3df98674bfb9b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066695"
---
# <span data-ttu-id="745a5-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="745a5-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="745a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="745a5-102">SYNOPSIS</span></span>
<span data-ttu-id="745a5-103">Создает продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="745a5-103">Creates an API Management product.</span></span>

## <span data-ttu-id="745a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="745a5-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="745a5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="745a5-105">DESCRIPTION</span></span>
<span data-ttu-id="745a5-106">Командлет **New-AzApiManagementProduct** создает продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="745a5-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="745a5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="745a5-107">EXAMPLES</span></span>

### <span data-ttu-id="745a5-108">Пример 1: создание продукта, для которого не требуется подписка</span><span class="sxs-lookup"><span data-stu-id="745a5-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="745a5-109">Эта команда создает продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="745a5-109">This command creates an API Management product.</span></span>
<span data-ttu-id="745a5-110">Подписка не требуется.</span><span class="sxs-lookup"><span data-stu-id="745a5-110">No subscription is required.</span></span>

### <span data-ttu-id="745a5-111">Пример 2: создание продукта, для которого требуется подписка и утверждение</span><span class="sxs-lookup"><span data-stu-id="745a5-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="745a5-112">Эта команда создает продукт.</span><span class="sxs-lookup"><span data-stu-id="745a5-112">This command creates a product.</span></span>
<span data-ttu-id="745a5-113">Необходимо подписаться на подписку и утверждение.</span><span class="sxs-lookup"><span data-stu-id="745a5-113">A subscription and approval are required.</span></span>
<span data-ttu-id="745a5-114">Эта команда задает период уведомления в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="745a5-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="745a5-115">Срок действия подписки на год равен 1 году.</span><span class="sxs-lookup"><span data-stu-id="745a5-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="745a5-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="745a5-116">PARAMETERS</span></span>

### <span data-ttu-id="745a5-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="745a5-117">-ApprovalRequired</span></span>
<span data-ttu-id="745a5-118">Указывает, требуется ли утверждение подписки на продукт или нет.</span><span class="sxs-lookup"><span data-stu-id="745a5-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="745a5-119">По умолчанию этот параметр имеет значение **$false**.</span><span class="sxs-lookup"><span data-stu-id="745a5-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="745a5-120">-Context</span><span class="sxs-lookup"><span data-stu-id="745a5-120">-Context</span></span>
<span data-ttu-id="745a5-121">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="745a5-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="745a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745a5-122">-DefaultProfile</span></span>
<span data-ttu-id="745a5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="745a5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="745a5-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="745a5-124">-Description</span></span>
<span data-ttu-id="745a5-125">Указывает описание продукта.</span><span class="sxs-lookup"><span data-stu-id="745a5-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="745a5-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="745a5-126">-LegalTerms</span></span>
<span data-ttu-id="745a5-127">Указывает юридические условия использования продукта.</span><span class="sxs-lookup"><span data-stu-id="745a5-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="745a5-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="745a5-128">-ProductId</span></span>
<span data-ttu-id="745a5-129">Указывает идентификатор нового продукта.</span><span class="sxs-lookup"><span data-stu-id="745a5-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="745a5-130">Если этот параметр не указан, создается новый продукт.</span><span class="sxs-lookup"><span data-stu-id="745a5-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="745a5-131">-State</span><span class="sxs-lookup"><span data-stu-id="745a5-131">-State</span></span>
<span data-ttu-id="745a5-132">Задает состояние продукта.</span><span class="sxs-lookup"><span data-stu-id="745a5-132">Specifies the product state.</span></span>
<span data-ttu-id="745a5-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="745a5-133">psdx_paramvalues</span></span>
- <span data-ttu-id="745a5-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="745a5-134">NotPublished</span></span>
- <span data-ttu-id="745a5-135">Опубликовано значение по умолчанию — NotPublished.</span><span class="sxs-lookup"><span data-stu-id="745a5-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="745a5-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="745a5-136">-SubscriptionRequired</span></span>
<span data-ttu-id="745a5-137">Указывает, требуется ли для продукта подписка.</span><span class="sxs-lookup"><span data-stu-id="745a5-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="745a5-138">Значение по умолчанию — **$true**.</span><span class="sxs-lookup"><span data-stu-id="745a5-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="745a5-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="745a5-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="745a5-140">Задает максимальное количество одновременных подписок.</span><span class="sxs-lookup"><span data-stu-id="745a5-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="745a5-141">Значение по умолчанию — None (нет).</span><span class="sxs-lookup"><span data-stu-id="745a5-141">The default value is None.</span></span>

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

### <span data-ttu-id="745a5-142">-Title</span><span class="sxs-lookup"><span data-stu-id="745a5-142">-Title</span></span>
<span data-ttu-id="745a5-143">Указывает название продукта.</span><span class="sxs-lookup"><span data-stu-id="745a5-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="745a5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745a5-144">CommonParameters</span></span>
<span data-ttu-id="745a5-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="745a5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="745a5-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="745a5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745a5-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="745a5-147">INPUTS</span></span>

### <span data-ttu-id="745a5-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="745a5-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="745a5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="745a5-149">System.String</span></span>

### <span data-ttu-id="745a5-150">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="745a5-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="745a5-151">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="745a5-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="745a5-152">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementProductState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="745a5-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="745a5-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="745a5-153">OUTPUTS</span></span>

### <span data-ttu-id="745a5-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="745a5-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="745a5-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="745a5-155">NOTES</span></span>

## <span data-ttu-id="745a5-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="745a5-156">RELATED LINKS</span></span>

[<span data-ttu-id="745a5-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="745a5-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="745a5-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="745a5-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="745a5-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="745a5-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


