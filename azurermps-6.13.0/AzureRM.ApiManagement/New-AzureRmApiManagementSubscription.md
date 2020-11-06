---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 2600f8f4039e0d719df2f393ffa16d42a712634a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556960"
---
# <span data-ttu-id="c6b39-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c6b39-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="c6b39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6b39-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b39-103">Создание подписки.</span><span class="sxs-lookup"><span data-stu-id="c6b39-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6b39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6b39-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6b39-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6b39-105">DESCRIPTION</span></span>
<span data-ttu-id="c6b39-106">Командлет **New-AzureRmApiManagementSubscription** создает подписку.</span><span class="sxs-lookup"><span data-stu-id="c6b39-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="c6b39-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6b39-107">EXAMPLES</span></span>

### <span data-ttu-id="c6b39-108">Пример 1: Подписка пользователя на продукт</span><span class="sxs-lookup"><span data-stu-id="c6b39-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="c6b39-109">Эта команда подписала существующего пользователя на продукт.</span><span class="sxs-lookup"><span data-stu-id="c6b39-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="c6b39-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6b39-110">PARAMETERS</span></span>

### <span data-ttu-id="c6b39-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c6b39-111">-Context</span></span>
<span data-ttu-id="c6b39-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c6b39-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c6b39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b39-113">-DefaultProfile</span></span>
<span data-ttu-id="c6b39-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b39-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6b39-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6b39-115">-Name</span></span>
<span data-ttu-id="c6b39-116">Указывает имя подписки.</span><span class="sxs-lookup"><span data-stu-id="c6b39-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="c6b39-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c6b39-117">-PrimaryKey</span></span>
<span data-ttu-id="c6b39-118">Указывает первичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="c6b39-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="c6b39-119">Если этот параметр не указан, ключ создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="c6b39-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="c6b39-120">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="c6b39-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c6b39-121">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c6b39-121">-ProductId</span></span>
<span data-ttu-id="c6b39-122">Указывает идентификатор продукта, подписку на который вы хотите подписать.</span><span class="sxs-lookup"><span data-stu-id="c6b39-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="c6b39-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="c6b39-123">-SecondaryKey</span></span>
<span data-ttu-id="c6b39-124">Задает вторичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="c6b39-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="c6b39-125">Этот параметр создается автоматически, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="c6b39-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="c6b39-126">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="c6b39-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c6b39-127">-State</span><span class="sxs-lookup"><span data-stu-id="c6b39-127">-State</span></span>
<span data-ttu-id="c6b39-128">Указывает состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="c6b39-128">Specifies the subscription state.</span></span>
<span data-ttu-id="c6b39-129">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="c6b39-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="c6b39-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6b39-130">-SubscriptionId</span></span>
<span data-ttu-id="c6b39-131">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="c6b39-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="c6b39-132">Этот параметр создается, если не указан.</span><span class="sxs-lookup"><span data-stu-id="c6b39-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="c6b39-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="c6b39-133">-UserId</span></span>
<span data-ttu-id="c6b39-134">Указывает идентификатор подписчика.</span><span class="sxs-lookup"><span data-stu-id="c6b39-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="c6b39-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b39-135">CommonParameters</span></span>
<span data-ttu-id="c6b39-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6b39-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b39-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6b39-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b39-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6b39-138">INPUTS</span></span>

### <span data-ttu-id="c6b39-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c6b39-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c6b39-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c6b39-140">System.String</span></span>

### <span data-ttu-id="c6b39-141">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. Commands. ApiManagement. ServiceManagement, Version = 6.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="c6b39-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c6b39-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6b39-142">OUTPUTS</span></span>

### <span data-ttu-id="c6b39-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c6b39-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="c6b39-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6b39-144">NOTES</span></span>

## <span data-ttu-id="c6b39-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6b39-145">RELATED LINKS</span></span>

[<span data-ttu-id="c6b39-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c6b39-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c6b39-147">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c6b39-147">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c6b39-148">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c6b39-148">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


