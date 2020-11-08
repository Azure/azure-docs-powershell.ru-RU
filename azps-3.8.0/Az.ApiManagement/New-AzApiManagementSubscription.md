---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066307"
---
# <span data-ttu-id="e247b-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e247b-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="e247b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e247b-102">SYNOPSIS</span></span>
<span data-ttu-id="e247b-103">Создание подписки.</span><span class="sxs-lookup"><span data-stu-id="e247b-103">Creates a subscription.</span></span>

## <span data-ttu-id="e247b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e247b-104">SYNTAX</span></span>

### <span data-ttu-id="e247b-105">OldSubscriptionModel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e247b-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e247b-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="e247b-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e247b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e247b-107">DESCRIPTION</span></span>
<span data-ttu-id="e247b-108">Командлет **New-AzApiManagementSubscription** создает подписку.</span><span class="sxs-lookup"><span data-stu-id="e247b-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="e247b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e247b-109">EXAMPLES</span></span>

### <span data-ttu-id="e247b-110">Пример 1: Подписка пользователя на продукт</span><span class="sxs-lookup"><span data-stu-id="e247b-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="e247b-111">Эта команда подписала существующего пользователя на продукт.</span><span class="sxs-lookup"><span data-stu-id="e247b-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="e247b-112">Пример 2: Создание подписки для всех областей API</span><span class="sxs-lookup"><span data-stu-id="e247b-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="e247b-113">Пример 3: Создание подписки на область продукта</span><span class="sxs-lookup"><span data-stu-id="e247b-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="e247b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e247b-114">PARAMETERS</span></span>

### <span data-ttu-id="e247b-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="e247b-115">-AllowTracing</span></span>
<span data-ttu-id="e247b-116">Флаг, который определяет, может ли трассировка быть включена на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="e247b-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="e247b-117">Это необязательный параметр, по умолчанию $null.</span><span class="sxs-lookup"><span data-stu-id="e247b-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="e247b-118">-Context</span><span class="sxs-lookup"><span data-stu-id="e247b-118">-Context</span></span>
<span data-ttu-id="e247b-119">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e247b-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e247b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e247b-120">-DefaultProfile</span></span>
<span data-ttu-id="e247b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e247b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e247b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e247b-122">-Name</span></span>
<span data-ttu-id="e247b-123">Указывает имя подписки.</span><span class="sxs-lookup"><span data-stu-id="e247b-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="e247b-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e247b-124">-PrimaryKey</span></span>
<span data-ttu-id="e247b-125">Указывает первичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="e247b-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="e247b-126">Если этот параметр не указан, ключ создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="e247b-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="e247b-127">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="e247b-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="e247b-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e247b-128">-ProductId</span></span>
<span data-ttu-id="e247b-129">Указывает идентификатор продукта, подписку на который вы хотите подписать.</span><span class="sxs-lookup"><span data-stu-id="e247b-129">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247b-130">-Scope</span><span class="sxs-lookup"><span data-stu-id="e247b-130">-Scope</span></span>
<span data-ttu-id="e247b-131">Область действия подписки, независимо от того, является ли она областью API/apis/{apiId} или областью продукта/products/{productId} или Global API Scope/APIs или Global Scope/.</span><span class="sxs-lookup"><span data-stu-id="e247b-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="e247b-132">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e247b-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247b-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="e247b-133">-SecondaryKey</span></span>
<span data-ttu-id="e247b-134">Задает вторичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="e247b-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="e247b-135">Этот параметр создается автоматически, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="e247b-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="e247b-136">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="e247b-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="e247b-137">-State</span><span class="sxs-lookup"><span data-stu-id="e247b-137">-State</span></span>
<span data-ttu-id="e247b-138">Указывает состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="e247b-138">Specifies the subscription state.</span></span>
<span data-ttu-id="e247b-139">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="e247b-139">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247b-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e247b-140">-SubscriptionId</span></span>
<span data-ttu-id="e247b-141">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="e247b-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="e247b-142">Этот параметр создается, если не указан.</span><span class="sxs-lookup"><span data-stu-id="e247b-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="e247b-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="e247b-143">-UserId</span></span>
<span data-ttu-id="e247b-144">Указывает идентификатор подписчика.</span><span class="sxs-lookup"><span data-stu-id="e247b-144">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e247b-145">CommonParameters</span></span>
<span data-ttu-id="e247b-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e247b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e247b-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e247b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e247b-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e247b-148">INPUTS</span></span>

### <span data-ttu-id="e247b-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e247b-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e247b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e247b-150">System.String</span></span>

### <span data-ttu-id="e247b-151">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="e247b-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e247b-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e247b-152">OUTPUTS</span></span>

### <span data-ttu-id="e247b-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e247b-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="e247b-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="e247b-154">NOTES</span></span>

## <span data-ttu-id="e247b-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e247b-155">RELATED LINKS</span></span>

[<span data-ttu-id="e247b-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e247b-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="e247b-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e247b-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="e247b-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e247b-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


