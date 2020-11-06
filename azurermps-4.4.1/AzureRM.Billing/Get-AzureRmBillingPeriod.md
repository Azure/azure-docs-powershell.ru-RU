---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: f6b75a1c161515ee45571ba3db6d2f84b95af967
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560500"
---
# <span data-ttu-id="16a0e-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="16a0e-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="16a0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="16a0e-103">Получение расчетных периодов для подписки.</span><span class="sxs-lookup"><span data-stu-id="16a0e-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16a0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16a0e-104">SYNTAX</span></span>

### <span data-ttu-id="16a0e-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16a0e-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16a0e-106">Единственное</span><span class="sxs-lookup"><span data-stu-id="16a0e-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16a0e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16a0e-107">DESCRIPTION</span></span>
<span data-ttu-id="16a0e-108">Командлет **Get-AzureRmBillingPeriod** возвращает периоды выставления счетов для подписки.</span><span class="sxs-lookup"><span data-stu-id="16a0e-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="16a0e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16a0e-109">EXAMPLES</span></span>

### <span data-ttu-id="16a0e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16a0e-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="16a0e-111">Получить все доступные расчетные периоды для подписки.</span><span class="sxs-lookup"><span data-stu-id="16a0e-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="16a0e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="16a0e-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="16a0e-113">Получить период выставления счетов для подписки с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="16a0e-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="16a0e-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="16a0e-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="16a0e-115">Получить не более двух расчетных периодов подписки.</span><span class="sxs-lookup"><span data-stu-id="16a0e-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="16a0e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16a0e-116">PARAMETERS</span></span>

### <span data-ttu-id="16a0e-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="16a0e-117">-MaxCount</span></span>
<span data-ttu-id="16a0e-118">Определение максимального числа возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="16a0e-118">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="16a0e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16a0e-119">-Name</span></span>
<span data-ttu-id="16a0e-120">Название определенного расчетного периода, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="16a0e-120">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="16a0e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a0e-121">-DefaultProfile</span></span>
<span data-ttu-id="16a0e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16a0e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16a0e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a0e-123">CommonParameters</span></span>
<span data-ttu-id="16a0e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16a0e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a0e-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16a0e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a0e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16a0e-126">INPUTS</span></span>

### <span data-ttu-id="16a0e-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="16a0e-127">None</span></span>

## <span data-ttu-id="16a0e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16a0e-128">OUTPUTS</span></span>

### <span data-ttu-id="16a0e-129">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. выставление PSBillingPeriod, версия = 0.12.0.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="16a0e-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod, Microsoft.Azure.Commands.Billing, Version=0.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="16a0e-130">Microsoft. Azure. Commands. Bill. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="16a0e-130">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="16a0e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="16a0e-131">NOTES</span></span>

## <span data-ttu-id="16a0e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16a0e-132">RELATED LINKS</span></span>

