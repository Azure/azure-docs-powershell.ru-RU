---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 1b99a5ac02364b54cf4411a0341ceaf749b8fa70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728033"
---
# <span data-ttu-id="097df-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="097df-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="097df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="097df-102">SYNOPSIS</span></span>
<span data-ttu-id="097df-103">Создает продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="097df-103">Creates an API Management product.</span></span>

## <span data-ttu-id="097df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="097df-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="097df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="097df-105">DESCRIPTION</span></span>
<span data-ttu-id="097df-106">Командлет **New-AzApiManagementProduct** создает продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="097df-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="097df-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="097df-107">EXAMPLES</span></span>

### <span data-ttu-id="097df-108">Пример 1: создание продукта, для которого не требуется подписка</span><span class="sxs-lookup"><span data-stu-id="097df-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="097df-109">Эта команда создает продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="097df-109">This command creates an API Management product.</span></span>
<span data-ttu-id="097df-110">Подписка не требуется.</span><span class="sxs-lookup"><span data-stu-id="097df-110">No subscription is required.</span></span>

### <span data-ttu-id="097df-111">Пример 2: создание продукта, для которого требуется подписка и утверждение</span><span class="sxs-lookup"><span data-stu-id="097df-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="097df-112">Эта команда создает продукт.</span><span class="sxs-lookup"><span data-stu-id="097df-112">This command creates a product.</span></span>
<span data-ttu-id="097df-113">Необходимо подписаться на подписку и утверждение.</span><span class="sxs-lookup"><span data-stu-id="097df-113">A subscription and approval are required.</span></span>
<span data-ttu-id="097df-114">Эта команда задает период уведомления в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="097df-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="097df-115">Срок действия подписки на год равен 1 году.</span><span class="sxs-lookup"><span data-stu-id="097df-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="097df-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="097df-116">PARAMETERS</span></span>

### <span data-ttu-id="097df-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="097df-117">-ApprovalRequired</span></span>
<span data-ttu-id="097df-118">Указывает, требуется ли утверждение подписки на продукт или нет.</span><span class="sxs-lookup"><span data-stu-id="097df-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="097df-119">По умолчанию этот параметр имеет значение **$false**.</span><span class="sxs-lookup"><span data-stu-id="097df-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="097df-120">-Context</span><span class="sxs-lookup"><span data-stu-id="097df-120">-Context</span></span>
<span data-ttu-id="097df-121">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="097df-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="097df-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097df-122">-DefaultProfile</span></span>
<span data-ttu-id="097df-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="097df-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="097df-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="097df-124">-Description</span></span>
<span data-ttu-id="097df-125">Указывает описание продукта.</span><span class="sxs-lookup"><span data-stu-id="097df-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="097df-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="097df-126">-LegalTerms</span></span>
<span data-ttu-id="097df-127">Указывает юридические условия использования продукта.</span><span class="sxs-lookup"><span data-stu-id="097df-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="097df-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="097df-128">-ProductId</span></span>
<span data-ttu-id="097df-129">Указывает идентификатор нового продукта.</span><span class="sxs-lookup"><span data-stu-id="097df-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="097df-130">Если этот параметр не указан, создается новый продукт.</span><span class="sxs-lookup"><span data-stu-id="097df-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="097df-131">-State</span><span class="sxs-lookup"><span data-stu-id="097df-131">-State</span></span>
<span data-ttu-id="097df-132">Задает состояние продукта.</span><span class="sxs-lookup"><span data-stu-id="097df-132">Specifies the product state.</span></span>
<span data-ttu-id="097df-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="097df-133">psdx_paramvalues</span></span>
- <span data-ttu-id="097df-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="097df-134">NotPublished</span></span>
- <span data-ttu-id="097df-135">Опубликовано значение по умолчанию — NotPublished.</span><span class="sxs-lookup"><span data-stu-id="097df-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="097df-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="097df-136">-SubscriptionRequired</span></span>
<span data-ttu-id="097df-137">Указывает, требуется ли для продукта подписка.</span><span class="sxs-lookup"><span data-stu-id="097df-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="097df-138">Значение по умолчанию — **$true**.</span><span class="sxs-lookup"><span data-stu-id="097df-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="097df-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="097df-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="097df-140">Задает максимальное количество одновременных подписок.</span><span class="sxs-lookup"><span data-stu-id="097df-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="097df-141">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="097df-141">The default value is 1.</span></span>

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

### <span data-ttu-id="097df-142">-Title</span><span class="sxs-lookup"><span data-stu-id="097df-142">-Title</span></span>
<span data-ttu-id="097df-143">Указывает название продукта.</span><span class="sxs-lookup"><span data-stu-id="097df-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="097df-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097df-144">CommonParameters</span></span>
<span data-ttu-id="097df-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="097df-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097df-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="097df-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097df-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="097df-147">INPUTS</span></span>

### <span data-ttu-id="097df-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="097df-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="097df-149">System. String</span><span class="sxs-lookup"><span data-stu-id="097df-149">System.String</span></span>

### <span data-ttu-id="097df-150">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="097df-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="097df-151">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="097df-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="097df-152">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementProductState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="097df-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="097df-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="097df-153">OUTPUTS</span></span>

### <span data-ttu-id="097df-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="097df-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="097df-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="097df-155">NOTES</span></span>

## <span data-ttu-id="097df-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="097df-156">RELATED LINKS</span></span>

[<span data-ttu-id="097df-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="097df-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="097df-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="097df-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="097df-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="097df-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


