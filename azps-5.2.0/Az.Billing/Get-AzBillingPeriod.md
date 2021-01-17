---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407044"
---
# <span data-ttu-id="cef07-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="cef07-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="cef07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef07-102">SYNOPSIS</span></span>
<span data-ttu-id="cef07-103">Периоды выплаты за подписку.</span><span class="sxs-lookup"><span data-stu-id="cef07-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="cef07-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cef07-104">SYNTAX</span></span>

### <span data-ttu-id="cef07-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cef07-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cef07-106">Один</span><span class="sxs-lookup"><span data-stu-id="cef07-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cef07-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef07-107">DESCRIPTION</span></span>
<span data-ttu-id="cef07-108">Для получения периодов выплаты за подписку будет период, соответствующий **cmdlet Get-AzBillingPeriod.**</span><span class="sxs-lookup"><span data-stu-id="cef07-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="cef07-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cef07-109">EXAMPLES</span></span>

### <span data-ttu-id="cef07-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cef07-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="cef07-111">Получите все доступные периоды выплаты за подписку.</span><span class="sxs-lookup"><span data-stu-id="cef07-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="cef07-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cef07-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="cef07-113">Получите период вы выставления счета для подписки с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="cef07-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="cef07-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cef07-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="cef07-115">Получите не более 2 периодов выплаты за подписку.</span><span class="sxs-lookup"><span data-stu-id="cef07-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="cef07-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cef07-116">PARAMETERS</span></span>

### <span data-ttu-id="cef07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef07-117">-DefaultProfile</span></span>
<span data-ttu-id="cef07-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cef07-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cef07-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="cef07-119">-MaxCount</span></span>
<span data-ttu-id="cef07-120">Определите максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="cef07-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="cef07-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cef07-121">-Name</span></span>
<span data-ttu-id="cef07-122">Название определенного периода вы выставления счета, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="cef07-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="cef07-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef07-123">CommonParameters</span></span>
<span data-ttu-id="cef07-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef07-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef07-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef07-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef07-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cef07-126">INPUTS</span></span>

### <span data-ttu-id="cef07-127">Нет</span><span class="sxs-lookup"><span data-stu-id="cef07-127">None</span></span>

## <span data-ttu-id="cef07-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cef07-128">OUTPUTS</span></span>

### <span data-ttu-id="cef07-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="cef07-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="cef07-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cef07-130">NOTES</span></span>

## <span data-ttu-id="cef07-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cef07-131">RELATED LINKS</span></span>
