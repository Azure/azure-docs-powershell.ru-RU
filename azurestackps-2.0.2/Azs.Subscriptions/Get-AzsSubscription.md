---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azssubscription
schema: 2.0.0
ms.openlocfilehash: 7dce95be9a936d341e0f063fd6d89701b18c2ce7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077026"
---
# <span data-ttu-id="c2b2b-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="c2b2b-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="c2b2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b2b-103">Получение сведений о конкретной подписке.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-103">Gets details about particular subscription.</span></span>

## <span data-ttu-id="c2b2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2b2b-104">SYNTAX</span></span>

### <span data-ttu-id="c2b2b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2b2b-105">List (Default)</span></span>
```
Get-AzsSubscription [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c2b2b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c2b2b-106">Get</span></span>
```
Get-AzsSubscription -SubscriptionId <String[]> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c2b2b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c2b2b-107">GetViaIdentity</span></span>
```
Get-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c2b2b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2b2b-108">DESCRIPTION</span></span>
<span data-ttu-id="c2b2b-109">Получение сведений о конкретной подписке.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-109">Gets details about particular subscription.</span></span>

## <span data-ttu-id="c2b2b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2b2b-110">EXAMPLES</span></span>

### <span data-ttu-id="c2b2b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2b2b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsSubscription | fl *

DisplayName    : Test User
Id             : /subscriptions/97d84f7a-bef7-4f2d-b651-c553be472311
OfferId        : /delegatedProviders/default/offers/TestOffer-590376ac-c8dd-4b3d-9674-b5b8fcde095b
State          : Enabled
SubscriptionId : 97d84f7a-bef7-4f2d-b651-c553be472311
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb

DisplayName    : cnur
Id             : /subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId        : /delegatedProviders/default/offers/cnur4866tenantsubsvcoffer843
State          : Enabled
SubscriptionId : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="c2b2b-112">Получение списка подписок.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-112">Get the list of subscriptions.</span></span>

## <span data-ttu-id="c2b2b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2b2b-113">PARAMETERS</span></span>

### <span data-ttu-id="c2b2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b2b-114">-DefaultProfile</span></span>
<span data-ttu-id="c2b2b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c2b2b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2b2b-116">-InputObject</span></span>
<span data-ttu-id="c2b2b-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c2b2b-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2b2b-118">-SubscriptionId</span></span>
<span data-ttu-id="c2b2b-119">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-119">Id of the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c2b2b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b2b-120">CommonParameters</span></span>
<span data-ttu-id="c2b2b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b2b-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2b2b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b2b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2b2b-123">INPUTS</span></span>

### <span data-ttu-id="c2b2b-124">Microsoft. Azure. PowerShell. командлеты. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="c2b2b-124">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="c2b2b-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2b2b-125">OUTPUTS</span></span>

### <span data-ttu-id="c2b2b-126">Microsoft. Azure. PowerShell. командлеты. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="c2b2b-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="c2b2b-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2b2b-127">NOTES</span></span>

<span data-ttu-id="c2b2b-128">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2b2b-129">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c2b2b-130">INPUTOBJECT <ISubscriptionIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="c2b2b-130">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c2b2b-131">`[DelegatedProviderId <String>]`: Идентификатор поставщика с делегированными полномочиями.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-131">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="c2b2b-132">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="c2b2b-132">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c2b2b-133">`[OfferName <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-133">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="c2b2b-134">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="c2b2b-134">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="c2b2b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2b2b-135">RELATED LINKS</span></span>

