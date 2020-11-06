---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 360bf469f5496d837d12fb6cd4fa8dba9cefd724
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568353"
---
# <span data-ttu-id="1b2db-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1b2db-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="1b2db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b2db-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2db-103">Создание подписки.</span><span class="sxs-lookup"><span data-stu-id="1b2db-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b2db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b2db-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b2db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b2db-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2db-106">Командлет **New-AzureRmApiManagementSubscription** создает подписку.</span><span class="sxs-lookup"><span data-stu-id="1b2db-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="1b2db-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b2db-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2db-108">Пример 1: Подписка пользователя на продукт</span><span class="sxs-lookup"><span data-stu-id="1b2db-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="1b2db-109">Эта команда подписала существующего пользователя на продукт.</span><span class="sxs-lookup"><span data-stu-id="1b2db-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="1b2db-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b2db-110">PARAMETERS</span></span>

### <span data-ttu-id="1b2db-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1b2db-111">-Context</span></span>
<span data-ttu-id="1b2db-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1b2db-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1b2db-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b2db-113">-Name</span></span>
<span data-ttu-id="1b2db-114">Указывает имя подписки.</span><span class="sxs-lookup"><span data-stu-id="1b2db-114">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="1b2db-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="1b2db-115">-PrimaryKey</span></span>
<span data-ttu-id="1b2db-116">Указывает первичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="1b2db-116">Specifies the subscription primary key.</span></span>
<span data-ttu-id="1b2db-117">Если этот параметр не указан, ключ создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="1b2db-117">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="1b2db-118">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="1b2db-118">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="1b2db-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1b2db-119">-ProductId</span></span>
<span data-ttu-id="1b2db-120">Указывает идентификатор продукта, подписку на который вы хотите подписать.</span><span class="sxs-lookup"><span data-stu-id="1b2db-120">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="1b2db-121">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1b2db-121">-SecondaryKey</span></span>
<span data-ttu-id="1b2db-122">Задает вторичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="1b2db-122">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="1b2db-123">Этот параметр создается автоматически, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="1b2db-123">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="1b2db-124">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="1b2db-124">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="1b2db-125">-State</span><span class="sxs-lookup"><span data-stu-id="1b2db-125">-State</span></span>
<span data-ttu-id="1b2db-126">Указывает состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="1b2db-126">Specifies the subscription state.</span></span>
<span data-ttu-id="1b2db-127">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="1b2db-127">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b2db-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b2db-128">-SubscriptionId</span></span>
<span data-ttu-id="1b2db-129">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="1b2db-129">Specifies the subscription ID.</span></span>
<span data-ttu-id="1b2db-130">Этот параметр создается, если не указан.</span><span class="sxs-lookup"><span data-stu-id="1b2db-130">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="1b2db-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="1b2db-131">-UserId</span></span>
<span data-ttu-id="1b2db-132">Указывает идентификатор подписчика.</span><span class="sxs-lookup"><span data-stu-id="1b2db-132">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="1b2db-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2db-133">-DefaultProfile</span></span>
<span data-ttu-id="1b2db-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b2db-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b2db-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2db-135">CommonParameters</span></span>
<span data-ttu-id="1b2db-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b2db-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2db-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b2db-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2db-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b2db-138">INPUTS</span></span>

## <span data-ttu-id="1b2db-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b2db-139">OUTPUTS</span></span>

### <span data-ttu-id="1b2db-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1b2db-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="1b2db-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b2db-141">NOTES</span></span>

## <span data-ttu-id="1b2db-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b2db-142">RELATED LINKS</span></span>

[<span data-ttu-id="1b2db-143">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1b2db-143">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="1b2db-144">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1b2db-144">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="1b2db-145">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1b2db-145">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


