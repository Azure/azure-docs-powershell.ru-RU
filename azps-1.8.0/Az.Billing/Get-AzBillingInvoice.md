---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 8c5e107de50d5e1df1f0c9da7305dbe801857410
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731451"
---
# <span data-ttu-id="82071-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="82071-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="82071-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82071-102">SYNOPSIS</span></span>
<span data-ttu-id="82071-103">Получение выставления счетов для подписки на план.</span><span class="sxs-lookup"><span data-stu-id="82071-103">Get billing invoices of the subscription.</span></span>

## <span data-ttu-id="82071-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82071-104">SYNTAX</span></span>

### <span data-ttu-id="82071-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82071-105">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82071-106">Последнюю</span><span class="sxs-lookup"><span data-stu-id="82071-106">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82071-107">Единственное</span><span class="sxs-lookup"><span data-stu-id="82071-107">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82071-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82071-108">DESCRIPTION</span></span>
<span data-ttu-id="82071-109">Командлет **Get-AzBillingInvoice** получает счета для выставления счетов по подписке.</span><span class="sxs-lookup"><span data-stu-id="82071-109">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="82071-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82071-110">EXAMPLES</span></span>

### <span data-ttu-id="82071-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82071-111">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="82071-112">Получить последнюю накладную по подписке.</span><span class="sxs-lookup"><span data-stu-id="82071-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="82071-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="82071-113">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="82071-114">Получение счета по подписке с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="82071-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="82071-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="82071-115">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="82071-116">Получите все доступные счета по подписке в обратном хронологическом порядке, начиная с самого последнего счета, без URL-адреса скачивания.</span><span class="sxs-lookup"><span data-stu-id="82071-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="82071-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="82071-117">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="82071-118">Получение последних 10 накладных по подписке и включение URL-адреса скачивания в результат.</span><span class="sxs-lookup"><span data-stu-id="82071-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="82071-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82071-119">PARAMETERS</span></span>

### <span data-ttu-id="82071-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82071-120">-DefaultProfile</span></span>
<span data-ttu-id="82071-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82071-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82071-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="82071-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="82071-123">Создание URL-адреса скачивания для счетов.</span><span class="sxs-lookup"><span data-stu-id="82071-123">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="82071-124">-Последние</span><span class="sxs-lookup"><span data-stu-id="82071-124">-Latest</span></span>
<span data-ttu-id="82071-125">Получить последнюю накладную.</span><span class="sxs-lookup"><span data-stu-id="82071-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="82071-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="82071-126">-MaxCount</span></span>
<span data-ttu-id="82071-127">Определяет максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="82071-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="82071-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82071-128">-Name</span></span>
<span data-ttu-id="82071-129">Имя определенного счета-фактуры, который вы хотите получить или является последним, если не указан.</span><span class="sxs-lookup"><span data-stu-id="82071-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="82071-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82071-130">CommonParameters</span></span>
<span data-ttu-id="82071-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82071-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82071-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82071-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82071-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82071-133">INPUTS</span></span>

### <span data-ttu-id="82071-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="82071-134">None</span></span>

## <span data-ttu-id="82071-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82071-135">OUTPUTS</span></span>

### <span data-ttu-id="82071-136">Microsoft. Azure. Commands. Bill. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="82071-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="82071-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="82071-137">NOTES</span></span>

## <span data-ttu-id="82071-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82071-138">RELATED LINKS</span></span>
