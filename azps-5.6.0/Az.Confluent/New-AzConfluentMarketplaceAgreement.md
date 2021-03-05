---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: f8c293870fa4eeb6f0df8a543473c8a9bda314c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012584"
---
# <span data-ttu-id="8f74d-101">New-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="8f74d-101">New-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="8f74d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f74d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f74d-103">Примите условия marketplace.</span><span class="sxs-lookup"><span data-stu-id="8f74d-103">Accept marketplace terms.</span></span>

## <span data-ttu-id="8f74d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f74d-104">SYNTAX</span></span>

```
New-AzConfluentMarketplaceAgreement [-SubscriptionId <String>] [-Accepted] [-LicenseTextLink <String>]
 [-Plan <String>] [-PrivacyPolicyLink <String>] [-Product <String>] [-Publisher <String>]
 [-RetrieveDatetime <DateTime>] [-Signature <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8f74d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f74d-105">DESCRIPTION</span></span>
<span data-ttu-id="8f74d-106">Примите условия marketplace.</span><span class="sxs-lookup"><span data-stu-id="8f74d-106">Accept marketplace terms.</span></span>

## <span data-ttu-id="8f74d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f74d-107">EXAMPLES</span></span>

### <span data-ttu-id="8f74d-108">Пример 1. Создание соглашения confluent marketplace в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="8f74d-108">Example 1: Create confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> New-AzConfluentMarketplaceAgreement -Accepted

Name    Type
----    ----
default Microsoft.Confluent/agreement
```

<span data-ttu-id="8f74d-109">Эта команда создает соглашение confluent marketplace в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="8f74d-109">This command create confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="8f74d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f74d-110">PARAMETERS</span></span>

### <span data-ttu-id="8f74d-111">-Accepted</span><span class="sxs-lookup"><span data-stu-id="8f74d-111">-Accepted</span></span>
<span data-ttu-id="8f74d-112">Если была принята любая версия условий, в противном случае это ложь.</span><span class="sxs-lookup"><span data-stu-id="8f74d-112">If any version of the terms have been accepted, otherwise false.</span></span>

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

### <span data-ttu-id="8f74d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f74d-113">-DefaultProfile</span></span>
<span data-ttu-id="8f74d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f74d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f74d-115">-LicenseTextLink</span><span class="sxs-lookup"><span data-stu-id="8f74d-115">-LicenseTextLink</span></span>
<span data-ttu-id="8f74d-116">Ссылка на HTML с терминами Microsoft и Publisher.</span><span class="sxs-lookup"><span data-stu-id="8f74d-116">Link to HTML with Microsoft and Publisher terms.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f74d-117">-Plan</span><span class="sxs-lookup"><span data-stu-id="8f74d-117">-Plan</span></span>
<span data-ttu-id="8f74d-118">Строка идентификатора плана.</span><span class="sxs-lookup"><span data-stu-id="8f74d-118">Plan identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f74d-119">-PrivacyPolicyLink</span><span class="sxs-lookup"><span data-stu-id="8f74d-119">-PrivacyPolicyLink</span></span>
<span data-ttu-id="8f74d-120">Ссылка на политику конфиденциальности издателя.</span><span class="sxs-lookup"><span data-stu-id="8f74d-120">Link to the privacy policy of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f74d-121">-Product</span><span class="sxs-lookup"><span data-stu-id="8f74d-121">-Product</span></span>
<span data-ttu-id="8f74d-122">Строка идентификатора продукта.</span><span class="sxs-lookup"><span data-stu-id="8f74d-122">Product identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f74d-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8f74d-123">-Publisher</span></span>
<span data-ttu-id="8f74d-124">Строка идентификатора Publisher.</span><span class="sxs-lookup"><span data-stu-id="8f74d-124">Publisher identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f74d-125">-RetrieveDatetime</span><span class="sxs-lookup"><span data-stu-id="8f74d-125">-RetrieveDatetime</span></span>
<span data-ttu-id="8f74d-126">Дата и время даты и времени даты и времени в UTC.</span><span class="sxs-lookup"><span data-stu-id="8f74d-126">Date and time in UTC of when the terms were accepted.</span></span>
<span data-ttu-id="8f74d-127">Если "Принято" ложно, этот вопрос будет пустым.</span><span class="sxs-lookup"><span data-stu-id="8f74d-127">This is empty if Accepted is false.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f74d-128">-Signature</span><span class="sxs-lookup"><span data-stu-id="8f74d-128">-Signature</span></span>
<span data-ttu-id="8f74d-129">Подпись условий.</span><span class="sxs-lookup"><span data-stu-id="8f74d-129">Terms signature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f74d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f74d-130">-SubscriptionId</span></span>
<span data-ttu-id="8f74d-131">ИД подписки Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="8f74d-131">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f74d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f74d-132">-Confirm</span></span>
<span data-ttu-id="8f74d-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8f74d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f74d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f74d-134">-WhatIf</span></span>
<span data-ttu-id="8f74d-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f74d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f74d-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8f74d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f74d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f74d-137">CommonParameters</span></span>
<span data-ttu-id="8f74d-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f74d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f74d-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f74d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f74d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f74d-140">INPUTS</span></span>

## <span data-ttu-id="8f74d-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f74d-141">OUTPUTS</span></span>

### <span data-ttu-id="8f74d-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="8f74d-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="8f74d-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f74d-143">NOTES</span></span>

<span data-ttu-id="8f74d-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8f74d-144">ALIASES</span></span>

## <span data-ttu-id="8f74d-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f74d-145">RELATED LINKS</span></span>

