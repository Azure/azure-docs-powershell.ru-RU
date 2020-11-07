---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: b4e85f85d0e7b7724b2a09f3c78af03dfd489014
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901502"
---
# <span data-ttu-id="bfc89-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="bfc89-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="bfc89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfc89-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc89-103">Получение расчетных периодов для подписки.</span><span class="sxs-lookup"><span data-stu-id="bfc89-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="bfc89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfc89-104">SYNTAX</span></span>

### <span data-ttu-id="bfc89-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bfc89-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfc89-106">Единственное</span><span class="sxs-lookup"><span data-stu-id="bfc89-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfc89-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfc89-107">DESCRIPTION</span></span>
<span data-ttu-id="bfc89-108">Командлет **Get-AzBillingPeriod** возвращает периоды выставления счетов для подписки.</span><span class="sxs-lookup"><span data-stu-id="bfc89-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="bfc89-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfc89-109">EXAMPLES</span></span>

### <span data-ttu-id="bfc89-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bfc89-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="bfc89-111">Получить все доступные расчетные периоды для подписки.</span><span class="sxs-lookup"><span data-stu-id="bfc89-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="bfc89-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bfc89-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="bfc89-113">Получить период выставления счетов для подписки с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="bfc89-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="bfc89-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bfc89-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="bfc89-115">Получить не более двух расчетных периодов подписки.</span><span class="sxs-lookup"><span data-stu-id="bfc89-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="bfc89-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfc89-116">PARAMETERS</span></span>

### <span data-ttu-id="bfc89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc89-117">-DefaultProfile</span></span>
<span data-ttu-id="bfc89-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bfc89-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfc89-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bfc89-119">-MaxCount</span></span>
<span data-ttu-id="bfc89-120">Определение максимального числа возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="bfc89-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="bfc89-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfc89-121">-Name</span></span>
<span data-ttu-id="bfc89-122">Название определенного расчетного периода, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="bfc89-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="bfc89-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc89-123">CommonParameters</span></span>
<span data-ttu-id="bfc89-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfc89-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc89-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc89-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc89-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfc89-126">INPUTS</span></span>

### <span data-ttu-id="bfc89-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="bfc89-127">None</span></span>

## <span data-ttu-id="bfc89-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfc89-128">OUTPUTS</span></span>

### <span data-ttu-id="bfc89-129">Microsoft. Azure. Commands. Bill. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="bfc89-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="bfc89-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfc89-130">NOTES</span></span>

## <span data-ttu-id="bfc89-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfc89-131">RELATED LINKS</span></span>
