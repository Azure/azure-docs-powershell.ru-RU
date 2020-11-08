---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsdelegatedprovideroffer
schema: 2.0.0
ms.openlocfilehash: 118834c020a198d355d3f3b9e6dc17699f88e0cc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077027"
---
# <span data-ttu-id="760b4-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="760b4-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="760b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="760b4-102">SYNOPSIS</span></span>
<span data-ttu-id="760b4-103">Получить указанное предложение для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="760b4-103">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="760b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="760b4-104">SYNTAX</span></span>

### <span data-ttu-id="760b4-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="760b4-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="760b4-106">Получить</span><span class="sxs-lookup"><span data-stu-id="760b4-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> -OfferName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="760b4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="760b4-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderOffer -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="760b4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="760b4-108">DESCRIPTION</span></span>
<span data-ttu-id="760b4-109">Получить указанное предложение для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="760b4-109">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="760b4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="760b4-110">EXAMPLES</span></span>

### <span data-ttu-id="760b4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="760b4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d

{{ Add output here }}
```

<span data-ttu-id="760b4-112">Получение списка предложенных для указанного поставщика делегированных данных</span><span class="sxs-lookup"><span data-stu-id="760b4-112">Get the list of offers for the specified delegated provider</span></span>

## <span data-ttu-id="760b4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="760b4-113">PARAMETERS</span></span>

### <span data-ttu-id="760b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="760b4-114">-DefaultProfile</span></span>
<span data-ttu-id="760b4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="760b4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="760b4-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="760b4-116">-DelegatedProviderId</span></span>
<span data-ttu-id="760b4-117">Идентификатор поставщика делегирования.</span><span class="sxs-lookup"><span data-stu-id="760b4-117">Id of the delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="760b4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="760b4-118">-InputObject</span></span>
<span data-ttu-id="760b4-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="760b4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="760b4-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="760b4-120">-OfferName</span></span>
<span data-ttu-id="760b4-121">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="760b4-121">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="760b4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="760b4-122">CommonParameters</span></span>
<span data-ttu-id="760b4-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="760b4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="760b4-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="760b4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="760b4-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="760b4-125">INPUTS</span></span>

### <span data-ttu-id="760b4-126">Microsoft. Azure. PowerShell. командлеты. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="760b4-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="760b4-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="760b4-127">OUTPUTS</span></span>

### <span data-ttu-id="760b4-128">Microsoft. Azure. PowerShell. командлеты. Subscription. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="760b4-128">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="760b4-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="760b4-129">NOTES</span></span>

<span data-ttu-id="760b4-130">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="760b4-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="760b4-131">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="760b4-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="760b4-132">INPUTOBJECT <ISubscriptionIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="760b4-132">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="760b4-133">`[DelegatedProviderId <String>]`: Идентификатор поставщика с делегированными полномочиями.</span><span class="sxs-lookup"><span data-stu-id="760b4-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="760b4-134">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="760b4-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="760b4-135">`[OfferName <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="760b4-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="760b4-136">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="760b4-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="760b4-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="760b4-137">RELATED LINKS</span></span>

