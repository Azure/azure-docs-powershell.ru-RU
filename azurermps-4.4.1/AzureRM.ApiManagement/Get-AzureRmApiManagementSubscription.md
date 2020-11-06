---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568366"
---
# <span data-ttu-id="b55b5-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b55b5-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="b55b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b55b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b55b5-103">Получение подписок.</span><span class="sxs-lookup"><span data-stu-id="b55b5-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b55b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b55b5-104">SYNTAX</span></span>

### <span data-ttu-id="b55b5-105">Получение всех подписок (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b55b5-105">Get all subscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b55b5-106">Получить с помощью идентификатора subsctiption</span><span class="sxs-lookup"><span data-stu-id="b55b5-106">Get by subsctiption ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b55b5-107">Получить с помощью идентификатора пользователя</span><span class="sxs-lookup"><span data-stu-id="b55b5-107">Get by user ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b55b5-108">Получить по коду продукта</span><span class="sxs-lookup"><span data-stu-id="b55b5-108">Get by product ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b55b5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b55b5-109">DESCRIPTION</span></span>
<span data-ttu-id="b55b5-110">Командлет **Get-AzureRmApiManagementSubscription** получает указанную подписку или все подписки, если подписка не указана.</span><span class="sxs-lookup"><span data-stu-id="b55b5-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="b55b5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b55b5-111">EXAMPLES</span></span>

### <span data-ttu-id="b55b5-112">Пример 1: получение всех подписок</span><span class="sxs-lookup"><span data-stu-id="b55b5-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="b55b5-113">Эта команда получает все подписки.</span><span class="sxs-lookup"><span data-stu-id="b55b5-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="b55b5-114">Пример 2: получение подписки с помощью указанного идентификатора</span><span class="sxs-lookup"><span data-stu-id="b55b5-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="b55b5-115">Эта команда получает подписку по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="b55b5-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="b55b5-116">Пример 3: получение всех подписок для пользователя</span><span class="sxs-lookup"><span data-stu-id="b55b5-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="b55b5-117">Эта команда получает пользовательские подписки.</span><span class="sxs-lookup"><span data-stu-id="b55b5-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="b55b5-118">Пример 4: получение всех подписок на продукт</span><span class="sxs-lookup"><span data-stu-id="b55b5-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="b55b5-119">Эта команда получает все подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="b55b5-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="b55b5-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b55b5-120">PARAMETERS</span></span>

### <span data-ttu-id="b55b5-121">-Context</span><span class="sxs-lookup"><span data-stu-id="b55b5-121">-Context</span></span>
<span data-ttu-id="b55b5-122">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b55b5-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b55b5-123">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b55b5-123">-ProductId</span></span>
<span data-ttu-id="b55b5-124">Указывает идентификатор продукта.</span><span class="sxs-lookup"><span data-stu-id="b55b5-124">Specifies a product identifier.</span></span>
<span data-ttu-id="b55b5-125">Если указан, этот командлет находит все подписки по идентификатору продукта.</span><span class="sxs-lookup"><span data-stu-id="b55b5-125">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b55b5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b55b5-126">-SubscriptionId</span></span>
<span data-ttu-id="b55b5-127">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="b55b5-127">Specifies a subscription identifier.</span></span>
<span data-ttu-id="b55b5-128">Если указан, этот командлет находит подписку с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="b55b5-128">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b55b5-129">-UserId</span><span class="sxs-lookup"><span data-stu-id="b55b5-129">-UserId</span></span>
<span data-ttu-id="b55b5-130">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="b55b5-130">Specifies a user identifier.</span></span>
<span data-ttu-id="b55b5-131">Если указан, этот командлет находит все подписки по идентификатору пользователя.</span><span class="sxs-lookup"><span data-stu-id="b55b5-131">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b55b5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b55b5-132">-DefaultProfile</span></span>
<span data-ttu-id="b55b5-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b55b5-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b55b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55b5-134">CommonParameters</span></span>
<span data-ttu-id="b55b5-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b55b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55b5-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b55b5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55b5-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b55b5-137">INPUTS</span></span>

## <span data-ttu-id="b55b5-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b55b5-138">OUTPUTS</span></span>

### <span data-ttu-id="b55b5-139">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="b55b5-139">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>

## <span data-ttu-id="b55b5-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="b55b5-140">NOTES</span></span>

## <span data-ttu-id="b55b5-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b55b5-141">RELATED LINKS</span></span>

[<span data-ttu-id="b55b5-142">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b55b5-142">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="b55b5-143">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b55b5-143">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="b55b5-144">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b55b5-144">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


