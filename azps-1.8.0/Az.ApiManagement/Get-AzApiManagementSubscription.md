---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 885d552f6040d4c88c007a37f839ac030ba671c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720137"
---
# <span data-ttu-id="c56c4-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c56c4-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="c56c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c56c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c56c4-103">Получение подписок.</span><span class="sxs-lookup"><span data-stu-id="c56c4-103">Gets subscriptions.</span></span>

## <span data-ttu-id="c56c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c56c4-104">SYNTAX</span></span>

### <span data-ttu-id="c56c4-105">GetAllSubscriptions (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c56c4-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c56c4-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c56c4-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c56c4-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="c56c4-107">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c56c4-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="c56c4-108">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c56c4-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c56c4-109">DESCRIPTION</span></span>
<span data-ttu-id="c56c4-110">Командлет **Get-AzApiManagementSubscription** получает указанную подписку или все подписки, если подписка не указана.</span><span class="sxs-lookup"><span data-stu-id="c56c4-110">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="c56c4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c56c4-111">EXAMPLES</span></span>

### <span data-ttu-id="c56c4-112">Пример 1: получение всех подписок</span><span class="sxs-lookup"><span data-stu-id="c56c4-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="c56c4-113">Эта команда получает все подписки.</span><span class="sxs-lookup"><span data-stu-id="c56c4-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="c56c4-114">Пример 2: получение подписки с помощью указанного идентификатора</span><span class="sxs-lookup"><span data-stu-id="c56c4-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="c56c4-115">Эта команда получает подписку по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="c56c4-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="c56c4-116">Пример 3: получение всех подписок для пользователя</span><span class="sxs-lookup"><span data-stu-id="c56c4-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="c56c4-117">Эта команда получает пользовательские подписки.</span><span class="sxs-lookup"><span data-stu-id="c56c4-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="c56c4-118">Пример 4: получение всех подписок на продукт</span><span class="sxs-lookup"><span data-stu-id="c56c4-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="c56c4-119">Эта команда получает все подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="c56c4-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="c56c4-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c56c4-120">PARAMETERS</span></span>

### <span data-ttu-id="c56c4-121">-Context</span><span class="sxs-lookup"><span data-stu-id="c56c4-121">-Context</span></span>
<span data-ttu-id="c56c4-122">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c56c4-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c56c4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56c4-123">-DefaultProfile</span></span>
<span data-ttu-id="c56c4-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c56c4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c56c4-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c56c4-125">-ProductId</span></span>
<span data-ttu-id="c56c4-126">Указывает идентификатор продукта.</span><span class="sxs-lookup"><span data-stu-id="c56c4-126">Specifies a product identifier.</span></span>
<span data-ttu-id="c56c4-127">Если указан, этот командлет находит все подписки по идентификатору продукта.</span><span class="sxs-lookup"><span data-stu-id="c56c4-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="c56c4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c56c4-128">-SubscriptionId</span></span>
<span data-ttu-id="c56c4-129">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="c56c4-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="c56c4-130">Если указан, этот командлет находит подписку с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="c56c4-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="c56c4-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="c56c4-131">-UserId</span></span>
<span data-ttu-id="c56c4-132">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="c56c4-132">Specifies a user identifier.</span></span>
<span data-ttu-id="c56c4-133">Если указан, этот командлет находит все подписки по идентификатору пользователя.</span><span class="sxs-lookup"><span data-stu-id="c56c4-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="c56c4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56c4-134">CommonParameters</span></span>
<span data-ttu-id="c56c4-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c56c4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56c4-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c56c4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56c4-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c56c4-137">INPUTS</span></span>

### <span data-ttu-id="c56c4-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c56c4-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c56c4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c56c4-139">System.String</span></span>

## <span data-ttu-id="c56c4-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c56c4-140">OUTPUTS</span></span>

### <span data-ttu-id="c56c4-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c56c4-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="c56c4-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c56c4-142">NOTES</span></span>

## <span data-ttu-id="c56c4-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c56c4-143">RELATED LINKS</span></span>

[<span data-ttu-id="c56c4-144">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c56c4-144">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="c56c4-145">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c56c4-145">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="c56c4-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c56c4-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


