---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557644"
---
# <span data-ttu-id="0a237-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a237-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="0a237-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a237-102">SYNOPSIS</span></span>
<span data-ttu-id="0a237-103">Получение подписок.</span><span class="sxs-lookup"><span data-stu-id="0a237-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a237-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a237-104">SYNTAX</span></span>

### <span data-ttu-id="0a237-105">GetAllSubscriptions (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a237-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a237-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a237-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a237-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="0a237-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a237-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="0a237-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a237-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a237-109">DESCRIPTION</span></span>
<span data-ttu-id="0a237-110">Командлет **Get-AzureRmApiManagementSubscription** получает указанную подписку или все подписки, если подписка не указана.</span><span class="sxs-lookup"><span data-stu-id="0a237-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="0a237-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a237-111">EXAMPLES</span></span>

### <span data-ttu-id="0a237-112">Пример 1: получение всех подписок</span><span class="sxs-lookup"><span data-stu-id="0a237-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="0a237-113">Эта команда получает все подписки.</span><span class="sxs-lookup"><span data-stu-id="0a237-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="0a237-114">Пример 2: получение подписки с помощью указанного идентификатора</span><span class="sxs-lookup"><span data-stu-id="0a237-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="0a237-115">Эта команда получает подписку по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="0a237-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="0a237-116">Пример 3: получение всех подписок для пользователя</span><span class="sxs-lookup"><span data-stu-id="0a237-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="0a237-117">Эта команда получает пользовательские подписки.</span><span class="sxs-lookup"><span data-stu-id="0a237-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="0a237-118">Пример 4: получение всех подписок на продукт</span><span class="sxs-lookup"><span data-stu-id="0a237-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="0a237-119">Эта команда получает все подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="0a237-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="0a237-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a237-120">PARAMETERS</span></span>

### <span data-ttu-id="0a237-121">-Context</span><span class="sxs-lookup"><span data-stu-id="0a237-121">-Context</span></span>
<span data-ttu-id="0a237-122">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0a237-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0a237-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a237-123">-DefaultProfile</span></span>
<span data-ttu-id="0a237-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a237-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0a237-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="0a237-125">-ProductId</span></span>
<span data-ttu-id="0a237-126">Указывает идентификатор продукта.</span><span class="sxs-lookup"><span data-stu-id="0a237-126">Specifies a product identifier.</span></span>
<span data-ttu-id="0a237-127">Если указан, этот командлет находит все подписки по идентификатору продукта.</span><span class="sxs-lookup"><span data-stu-id="0a237-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a237-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a237-128">-SubscriptionId</span></span>
<span data-ttu-id="0a237-129">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="0a237-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="0a237-130">Если указан, этот командлет находит подписку с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="0a237-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetBySubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a237-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="0a237-131">-UserId</span></span>
<span data-ttu-id="0a237-132">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a237-132">Specifies a user identifier.</span></span>
<span data-ttu-id="0a237-133">Если указан, этот командлет находит все подписки по идентификатору пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a237-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a237-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a237-134">CommonParameters</span></span>
<span data-ttu-id="0a237-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a237-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a237-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a237-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a237-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a237-137">INPUTS</span></span>

### <span data-ttu-id="0a237-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="0a237-138">None</span></span>
<span data-ttu-id="0a237-139">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0a237-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a237-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a237-140">OUTPUTS</span></span>

### <span data-ttu-id="0a237-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a237-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>
<span data-ttu-id="0a237-142">Сведения о подписке в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="0a237-142">The detail of the subscription in the API Management service.</span></span>

### <span data-ttu-id="0a237-143">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="0a237-143">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>
<span data-ttu-id="0a237-144">Список подписок в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="0a237-144">The list of subscription in API Management service.</span></span>

## <span data-ttu-id="0a237-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a237-145">NOTES</span></span>

## <span data-ttu-id="0a237-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a237-146">RELATED LINKS</span></span>

[<span data-ttu-id="0a237-147">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a237-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="0a237-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a237-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="0a237-149">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a237-149">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


