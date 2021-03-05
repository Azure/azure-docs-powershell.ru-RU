---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: 00186ae370b7f5ccaac14bbdc85ba6b1f7aaa762
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994535"
---
# <span data-ttu-id="f17c5-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f17c5-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="f17c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f17c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f17c5-103">Создает подписку.</span><span class="sxs-lookup"><span data-stu-id="f17c5-103">Creates a subscription.</span></span>

## <span data-ttu-id="f17c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f17c5-104">SYNTAX</span></span>

### <span data-ttu-id="f17c5-105">OldSubscriptionModel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f17c5-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f17c5-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="f17c5-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f17c5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f17c5-107">DESCRIPTION</span></span>
<span data-ttu-id="f17c5-108">Для создания подписки будет замерен новый для **AzApiManagementSubscription.**</span><span class="sxs-lookup"><span data-stu-id="f17c5-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="f17c5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f17c5-109">EXAMPLES</span></span>

### <span data-ttu-id="f17c5-110">Пример 1. Подписка пользователя на продукт</span><span class="sxs-lookup"><span data-stu-id="f17c5-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="f17c5-111">Эта команда подписывает существующего пользователя на продукт.</span><span class="sxs-lookup"><span data-stu-id="f17c5-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="f17c5-112">Пример 2. Создание подписки для всех областей Api</span><span class="sxs-lookup"><span data-stu-id="f17c5-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="f17c5-113">Пример 3. Создание подписки для области продуктов</span><span class="sxs-lookup"><span data-stu-id="f17c5-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="f17c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f17c5-114">PARAMETERS</span></span>

### <span data-ttu-id="f17c5-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="f17c5-115">-AllowTracing</span></span>
<span data-ttu-id="f17c5-116">Флаг, который определяет, можно ли включить трассировку на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="f17c5-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="f17c5-117">Это необязательный параметр, который по умолчанию $null.</span><span class="sxs-lookup"><span data-stu-id="f17c5-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="f17c5-118">-Контекст</span><span class="sxs-lookup"><span data-stu-id="f17c5-118">-Context</span></span>
<span data-ttu-id="f17c5-119">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="f17c5-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f17c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17c5-120">-DefaultProfile</span></span>
<span data-ttu-id="f17c5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f17c5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f17c5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f17c5-122">-Name</span></span>
<span data-ttu-id="f17c5-123">Указывает имя подписки.</span><span class="sxs-lookup"><span data-stu-id="f17c5-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="f17c5-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f17c5-124">-PrimaryKey</span></span>
<span data-ttu-id="f17c5-125">Определяет первичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="f17c5-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="f17c5-126">Если этот параметр не указан, ключ создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="f17c5-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="f17c5-127">Этот параметр должен иметь длину от 1 до 300 знаков.</span><span class="sxs-lookup"><span data-stu-id="f17c5-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="f17c5-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f17c5-128">-ProductId</span></span>
<span data-ttu-id="f17c5-129">Определяет ИД продукта, на который нужно подписаться.</span><span class="sxs-lookup"><span data-stu-id="f17c5-129">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="f17c5-130">-Scope</span><span class="sxs-lookup"><span data-stu-id="f17c5-130">-Scope</span></span>
<span data-ttu-id="f17c5-131">Область действия подписки, будь то область API /apis/{apiId}, область продуктов /products/{productId} или глобальная область API /apis или глобальная область /.</span><span class="sxs-lookup"><span data-stu-id="f17c5-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="f17c5-132">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="f17c5-132">This parameter is required.</span></span>

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

### <span data-ttu-id="f17c5-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="f17c5-133">-SecondaryKey</span></span>
<span data-ttu-id="f17c5-134">Определяет дополнительный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="f17c5-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="f17c5-135">Этот параметр создается автоматически, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="f17c5-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="f17c5-136">Этот параметр должен иметь длину от 1 до 300 знаков.</span><span class="sxs-lookup"><span data-stu-id="f17c5-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="f17c5-137">-State</span><span class="sxs-lookup"><span data-stu-id="f17c5-137">-State</span></span>
<span data-ttu-id="f17c5-138">Определяет состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="f17c5-138">Specifies the subscription state.</span></span>
<span data-ttu-id="f17c5-139">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="f17c5-139">The default value is $Null.</span></span>

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

### <span data-ttu-id="f17c5-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f17c5-140">-SubscriptionId</span></span>
<span data-ttu-id="f17c5-141">Определяет ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="f17c5-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="f17c5-142">Этот параметр создается, если не указан.</span><span class="sxs-lookup"><span data-stu-id="f17c5-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="f17c5-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="f17c5-143">-UserId</span></span>
<span data-ttu-id="f17c5-144">Определяет ИД подписчика.</span><span class="sxs-lookup"><span data-stu-id="f17c5-144">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="f17c5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17c5-145">CommonParameters</span></span>
<span data-ttu-id="f17c5-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f17c5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17c5-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f17c5-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17c5-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f17c5-148">INPUTS</span></span>

### <span data-ttu-id="f17c5-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f17c5-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f17c5-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f17c5-150">System.String</span></span>

### <span data-ttu-id="f17c5-151">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f17c5-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f17c5-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f17c5-152">OUTPUTS</span></span>

### <span data-ttu-id="f17c5-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f17c5-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="f17c5-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f17c5-154">NOTES</span></span>

## <span data-ttu-id="f17c5-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f17c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="f17c5-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f17c5-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="f17c5-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f17c5-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="f17c5-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f17c5-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


