---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077021"
---
# <span data-ttu-id="e44df-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="e44df-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="e44df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e44df-102">SYNOPSIS</span></span>


## <span data-ttu-id="e44df-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e44df-103">SYNTAX</span></span>

### <span data-ttu-id="e44df-104">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e44df-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e44df-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e44df-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e44df-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e44df-106">DESCRIPTION</span></span>


## <span data-ttu-id="e44df-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e44df-107">EXAMPLES</span></span>

### <span data-ttu-id="e44df-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e44df-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="e44df-109">Удаление указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="e44df-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="e44df-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e44df-110">PARAMETERS</span></span>

### <span data-ttu-id="e44df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44df-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="e44df-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e44df-112">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e44df-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e44df-113">-InputObject</span></span>
<span data-ttu-id="e44df-114">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e44df-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e44df-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e44df-115">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e44df-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e44df-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e44df-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e44df-117">-Confirm</span></span>
<span data-ttu-id="e44df-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e44df-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e44df-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e44df-119">-WhatIf</span></span>
<span data-ttu-id="e44df-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e44df-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e44df-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e44df-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e44df-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44df-122">CommonParameters</span></span>
<span data-ttu-id="e44df-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e44df-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44df-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e44df-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44df-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e44df-125">INPUTS</span></span>

### <span data-ttu-id="e44df-126">Microsoft. Azure. PowerShell. командлеты. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="e44df-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="e44df-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e44df-127">OUTPUTS</span></span>

### <span data-ttu-id="e44df-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e44df-128">System.Boolean</span></span>



## <span data-ttu-id="e44df-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="e44df-129">NOTES</span></span>

<span data-ttu-id="e44df-130">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e44df-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e44df-131">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e44df-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e44df-132">INPUTOBJECT <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="e44df-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="e44df-133">`[DelegatedProviderId <String>]`: Идентификатор поставщика с делегированными полномочиями.</span><span class="sxs-lookup"><span data-stu-id="e44df-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="e44df-134">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e44df-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e44df-135">`[OfferName <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="e44df-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="e44df-136">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="e44df-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="e44df-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e44df-137">RELATED LINKS</span></span>

