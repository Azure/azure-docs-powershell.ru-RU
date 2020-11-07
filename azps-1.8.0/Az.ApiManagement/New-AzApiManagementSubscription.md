---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: b836fec6074767e4b97188b5bb75f38d22724eb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901726"
---
# <span data-ttu-id="ae65b-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ae65b-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="ae65b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae65b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae65b-103">Создание подписки.</span><span class="sxs-lookup"><span data-stu-id="ae65b-103">Creates a subscription.</span></span>

## <span data-ttu-id="ae65b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae65b-104">SYNTAX</span></span>

```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae65b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae65b-105">DESCRIPTION</span></span>
<span data-ttu-id="ae65b-106">Командлет **New-AzApiManagementSubscription** создает подписку.</span><span class="sxs-lookup"><span data-stu-id="ae65b-106">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="ae65b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae65b-107">EXAMPLES</span></span>

### <span data-ttu-id="ae65b-108">Пример 1: Подписка пользователя на продукт</span><span class="sxs-lookup"><span data-stu-id="ae65b-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="ae65b-109">Эта команда подписала существующего пользователя на продукт.</span><span class="sxs-lookup"><span data-stu-id="ae65b-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="ae65b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae65b-110">PARAMETERS</span></span>

### <span data-ttu-id="ae65b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ae65b-111">-Context</span></span>
<span data-ttu-id="ae65b-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ae65b-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ae65b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae65b-113">-DefaultProfile</span></span>
<span data-ttu-id="ae65b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae65b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae65b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae65b-115">-Name</span></span>
<span data-ttu-id="ae65b-116">Указывает имя подписки.</span><span class="sxs-lookup"><span data-stu-id="ae65b-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="ae65b-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ae65b-117">-PrimaryKey</span></span>
<span data-ttu-id="ae65b-118">Указывает первичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="ae65b-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="ae65b-119">Если этот параметр не указан, ключ создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="ae65b-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="ae65b-120">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="ae65b-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="ae65b-121">-ProductId</span><span class="sxs-lookup"><span data-stu-id="ae65b-121">-ProductId</span></span>
<span data-ttu-id="ae65b-122">Указывает идентификатор продукта, подписку на который вы хотите подписать.</span><span class="sxs-lookup"><span data-stu-id="ae65b-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="ae65b-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ae65b-123">-SecondaryKey</span></span>
<span data-ttu-id="ae65b-124">Задает вторичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="ae65b-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="ae65b-125">Этот параметр создается автоматически, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="ae65b-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="ae65b-126">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="ae65b-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="ae65b-127">-State</span><span class="sxs-lookup"><span data-stu-id="ae65b-127">-State</span></span>
<span data-ttu-id="ae65b-128">Указывает состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="ae65b-128">Specifies the subscription state.</span></span>
<span data-ttu-id="ae65b-129">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="ae65b-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="ae65b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae65b-130">-SubscriptionId</span></span>
<span data-ttu-id="ae65b-131">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="ae65b-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="ae65b-132">Этот параметр создается, если не указан.</span><span class="sxs-lookup"><span data-stu-id="ae65b-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="ae65b-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="ae65b-133">-UserId</span></span>
<span data-ttu-id="ae65b-134">Указывает идентификатор подписчика.</span><span class="sxs-lookup"><span data-stu-id="ae65b-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="ae65b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae65b-135">CommonParameters</span></span>
<span data-ttu-id="ae65b-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae65b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae65b-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae65b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae65b-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae65b-138">INPUTS</span></span>

### <span data-ttu-id="ae65b-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ae65b-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ae65b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ae65b-140">System.String</span></span>

### <span data-ttu-id="ae65b-141">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ae65b-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ae65b-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae65b-142">OUTPUTS</span></span>

### <span data-ttu-id="ae65b-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ae65b-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="ae65b-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae65b-144">NOTES</span></span>

## <span data-ttu-id="ae65b-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae65b-145">RELATED LINKS</span></span>

[<span data-ttu-id="ae65b-146">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ae65b-146">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="ae65b-147">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ae65b-147">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="ae65b-148">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ae65b-148">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


