---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 66c9a0bb9ba4aa2f17c48ffb737f1c8d72034f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567302"
---
# <span data-ttu-id="15d1a-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="15d1a-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="15d1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="15d1a-103">Получение расчетных периодов для подписки.</span><span class="sxs-lookup"><span data-stu-id="15d1a-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15d1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15d1a-104">SYNTAX</span></span>

### <span data-ttu-id="15d1a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15d1a-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15d1a-106">Единственное</span><span class="sxs-lookup"><span data-stu-id="15d1a-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15d1a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15d1a-107">DESCRIPTION</span></span>
<span data-ttu-id="15d1a-108">Командлет **Get-AzureRmBillingPeriod** возвращает периоды выставления счетов для подписки.</span><span class="sxs-lookup"><span data-stu-id="15d1a-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="15d1a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15d1a-109">EXAMPLES</span></span>

### <span data-ttu-id="15d1a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15d1a-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="15d1a-111">Получить все доступные расчетные периоды для подписки.</span><span class="sxs-lookup"><span data-stu-id="15d1a-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="15d1a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="15d1a-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="15d1a-113">Получить период выставления счетов для подписки с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="15d1a-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="15d1a-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="15d1a-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="15d1a-115">Получить не более двух расчетных периодов подписки.</span><span class="sxs-lookup"><span data-stu-id="15d1a-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="15d1a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15d1a-116">PARAMETERS</span></span>

### <span data-ttu-id="15d1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d1a-117">-DefaultProfile</span></span>
<span data-ttu-id="15d1a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="15d1a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15d1a-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="15d1a-119">-MaxCount</span></span>
<span data-ttu-id="15d1a-120">Определение максимального числа возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="15d1a-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d1a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15d1a-121">-Name</span></span>
<span data-ttu-id="15d1a-122">Название определенного расчетного периода, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="15d1a-122">Name of a specific billing period to get.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d1a-123">CommonParameters</span></span>
<span data-ttu-id="15d1a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15d1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d1a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d1a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d1a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15d1a-126">INPUTS</span></span>

### <span data-ttu-id="15d1a-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="15d1a-127">None</span></span>

## <span data-ttu-id="15d1a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15d1a-128">OUTPUTS</span></span>

### <span data-ttu-id="15d1a-129">Microsoft. Azure. Commands. Bill. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="15d1a-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="15d1a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="15d1a-130">NOTES</span></span>

## <span data-ttu-id="15d1a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15d1a-131">RELATED LINKS</span></span>
