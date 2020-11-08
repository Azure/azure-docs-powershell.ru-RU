---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: e3400ea600ed2891101a94f9ec1a7853326a7c04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079895"
---
# <span data-ttu-id="90389-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="90389-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="90389-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90389-102">SYNOPSIS</span></span>
<span data-ttu-id="90389-103">Получение подписок.</span><span class="sxs-lookup"><span data-stu-id="90389-103">Gets subscriptions.</span></span>

## <span data-ttu-id="90389-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90389-104">SYNTAX</span></span>

### <span data-ttu-id="90389-105">GetAllSubscriptions (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90389-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90389-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90389-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90389-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="90389-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90389-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="90389-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90389-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="90389-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90389-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="90389-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90389-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90389-111">DESCRIPTION</span></span>
<span data-ttu-id="90389-112">Командлет **Get-AzApiManagementSubscription** получает указанную подписку или все подписки, если подписка не указана.</span><span class="sxs-lookup"><span data-stu-id="90389-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="90389-113">Ключи не будут включены в данные результата.</span><span class="sxs-lookup"><span data-stu-id="90389-113">Keys will not be included into result details.</span></span> <span data-ttu-id="90389-114">Чтобы получить доступ к клавишам, используйте **Get-AzApiManagementSubscriptionKey**.</span><span class="sxs-lookup"><span data-stu-id="90389-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="90389-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90389-115">EXAMPLES</span></span>

### <span data-ttu-id="90389-116">Пример 1: получение всех подписок</span><span class="sxs-lookup"><span data-stu-id="90389-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="90389-117">Эта команда получает все подписки.</span><span class="sxs-lookup"><span data-stu-id="90389-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="90389-118">Пример 2: получение подписки с помощью указанного идентификатора</span><span class="sxs-lookup"><span data-stu-id="90389-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="90389-119">Эта команда получает подписку по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="90389-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="90389-120">Пример 3: получение всех подписок для пользователя</span><span class="sxs-lookup"><span data-stu-id="90389-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="90389-121">Эта команда получает пользовательские подписки.</span><span class="sxs-lookup"><span data-stu-id="90389-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="90389-122">Пример 4: получение всех подписок на продукт</span><span class="sxs-lookup"><span data-stu-id="90389-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="90389-123">Эта команда получает все подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="90389-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="90389-124">Пример 5: получение всех подписок для области</span><span class="sxs-lookup"><span data-stu-id="90389-124">Example 5: Get all subscriptions for a Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -Scope "/apis"

SubscriptionId    : allApScope
UserId            :
OwnerId           :
ProductId         :
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis
Name              : All Api Scope
State             : Active
CreatedDate       : 6/18/2019 5:53:49 PM
StartDate         :
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
StateComment      :
AllowTracing      : False
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/allApScope
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="90389-125">Эта команда получает все подписки, настроенные для глобальной области API.</span><span class="sxs-lookup"><span data-stu-id="90389-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="90389-126">Пример 6: получение всех подписок для продукта и области пользователя</span><span class="sxs-lookup"><span data-stu-id="90389-126">Example 6: Get all subscriptions for a product and user scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId 59b872f28a82740f547e6270 -UserId 1

SubscriptionId    : 59b872f38a82741750c8da56
UserId            : 1
OwnerId           : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/users/1
ProductId         : 59b872f28a82740f547e6270
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/products/59b872f28a82740f547e6270
Name              :
State             : Active
CreatedDate       : 9/12/2017 11:51:15 PM
StartDate         : 9/12/2017 12:00:00 AM
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 7e64ef904b194706835febf87f729bb0
SecondaryKey      : 0354fccef73e43feb82e5c5da17674d5
StateComment      :
AllowTracing      : True
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/59b872f38a82741750c8da56
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="90389-127">Эта команда получает все подписки, настроенные для глобальной области API.</span><span class="sxs-lookup"><span data-stu-id="90389-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="90389-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90389-128">PARAMETERS</span></span>

### <span data-ttu-id="90389-129">-Context</span><span class="sxs-lookup"><span data-stu-id="90389-129">-Context</span></span>
<span data-ttu-id="90389-130">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="90389-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="90389-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90389-131">-DefaultProfile</span></span>
<span data-ttu-id="90389-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90389-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90389-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="90389-133">-ProductId</span></span>
<span data-ttu-id="90389-134">Указывает идентификатор продукта.</span><span class="sxs-lookup"><span data-stu-id="90389-134">Specifies a product identifier.</span></span>
<span data-ttu-id="90389-135">Если указан, этот командлет находит все подписки по идентификатору продукта.</span><span class="sxs-lookup"><span data-stu-id="90389-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90389-136">-Scope</span><span class="sxs-lookup"><span data-stu-id="90389-136">-Scope</span></span>
<span data-ttu-id="90389-137">Идентификатор области.</span><span class="sxs-lookup"><span data-stu-id="90389-137">Scope identifier.</span></span> <span data-ttu-id="90389-138">Область действия подписки, независимо от того, является ли она областью API/apis/{apiId} или областью продукта/products/{productId} или Global API Scope/APIs или Global Scope/.</span><span class="sxs-lookup"><span data-stu-id="90389-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90389-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90389-139">-SubscriptionId</span></span>
<span data-ttu-id="90389-140">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="90389-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="90389-141">Если указан, этот командлет находит подписку с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="90389-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90389-142">-UserId</span><span class="sxs-lookup"><span data-stu-id="90389-142">-UserId</span></span>
<span data-ttu-id="90389-143">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="90389-143">Specifies a user identifier.</span></span>
<span data-ttu-id="90389-144">Если указан, этот командлет находит все подписки по идентификатору пользователя.</span><span class="sxs-lookup"><span data-stu-id="90389-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90389-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90389-145">CommonParameters</span></span>
<span data-ttu-id="90389-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90389-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90389-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90389-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90389-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90389-148">INPUTS</span></span>

### <span data-ttu-id="90389-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90389-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="90389-150">System. String</span><span class="sxs-lookup"><span data-stu-id="90389-150">System.String</span></span>

## <span data-ttu-id="90389-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90389-151">OUTPUTS</span></span>

### <span data-ttu-id="90389-152">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="90389-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="90389-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="90389-153">NOTES</span></span>

## <span data-ttu-id="90389-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90389-154">RELATED LINKS</span></span>

[<span data-ttu-id="90389-155">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="90389-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="90389-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="90389-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="90389-157">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="90389-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


