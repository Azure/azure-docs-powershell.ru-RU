---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2b1906d07b3e08b1761469b4a9d6d8d565e0fd8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242592"
---
# <span data-ttu-id="7598a-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="7598a-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="7598a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7598a-102">SYNOPSIS</span></span>
<span data-ttu-id="7598a-103">Получение выставления счетов для подписки на план.</span><span class="sxs-lookup"><span data-stu-id="7598a-103">Get billing invoices of the subscription.</span></span>

## <span data-ttu-id="7598a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7598a-104">SYNTAX</span></span>

### <span data-ttu-id="7598a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7598a-105">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7598a-106">Последнюю</span><span class="sxs-lookup"><span data-stu-id="7598a-106">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7598a-107">Единственное</span><span class="sxs-lookup"><span data-stu-id="7598a-107">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7598a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7598a-108">DESCRIPTION</span></span>
<span data-ttu-id="7598a-109">Командлет **Get-AzBillingInvoice** получает счета для выставления счетов по подписке.</span><span class="sxs-lookup"><span data-stu-id="7598a-109">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="7598a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7598a-110">EXAMPLES</span></span>

### <span data-ttu-id="7598a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7598a-111">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="7598a-112">Получить последнюю накладную по подписке.</span><span class="sxs-lookup"><span data-stu-id="7598a-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="7598a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7598a-113">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="7598a-114">Получение счета по подписке с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="7598a-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="7598a-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7598a-115">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="7598a-116">Получите все доступные счета по подписке в обратном хронологическом порядке, начиная с самого последнего счета, без URL-адреса скачивания.</span><span class="sxs-lookup"><span data-stu-id="7598a-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="7598a-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="7598a-117">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="7598a-118">Получение последних 10 накладных по подписке и включение URL-адреса скачивания в результат.</span><span class="sxs-lookup"><span data-stu-id="7598a-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="7598a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7598a-119">PARAMETERS</span></span>

### <span data-ttu-id="7598a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7598a-120">-DefaultProfile</span></span>
<span data-ttu-id="7598a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7598a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7598a-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="7598a-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="7598a-123">Создание URL-адреса скачивания для счетов.</span><span class="sxs-lookup"><span data-stu-id="7598a-123">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7598a-124">-Последние</span><span class="sxs-lookup"><span data-stu-id="7598a-124">-Latest</span></span>
<span data-ttu-id="7598a-125">Получить последнюю накладную.</span><span class="sxs-lookup"><span data-stu-id="7598a-125">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7598a-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7598a-126">-MaxCount</span></span>
<span data-ttu-id="7598a-127">Определяет максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="7598a-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="7598a-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7598a-128">-Name</span></span>
<span data-ttu-id="7598a-129">Имя определенного счета-фактуры, который вы хотите получить или является последним, если не указан.</span><span class="sxs-lookup"><span data-stu-id="7598a-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="7598a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7598a-130">CommonParameters</span></span>
<span data-ttu-id="7598a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7598a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7598a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7598a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7598a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7598a-133">INPUTS</span></span>

### <span data-ttu-id="7598a-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="7598a-134">None</span></span>

## <span data-ttu-id="7598a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7598a-135">OUTPUTS</span></span>

### <span data-ttu-id="7598a-136">Microsoft. Azure. Commands. Bill. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="7598a-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="7598a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="7598a-137">NOTES</span></span>

## <span data-ttu-id="7598a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7598a-138">RELATED LINKS</span></span>
