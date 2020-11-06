---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 38b1c4e29ed82ac3bddcff9565a216bd6db23411
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566751"
---
# <span data-ttu-id="814cf-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="814cf-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="814cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="814cf-102">SYNOPSIS</span></span>
<span data-ttu-id="814cf-103">Получение выставления счетов для подписки на план.</span><span class="sxs-lookup"><span data-stu-id="814cf-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="814cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="814cf-104">SYNTAX</span></span>

### <span data-ttu-id="814cf-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="814cf-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="814cf-106">Последнюю</span><span class="sxs-lookup"><span data-stu-id="814cf-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="814cf-107">Единственное</span><span class="sxs-lookup"><span data-stu-id="814cf-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="814cf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="814cf-108">DESCRIPTION</span></span>
<span data-ttu-id="814cf-109">Командлет **Get-AzureRmBillingInvoice** получает счета для выставления счетов по подписке.</span><span class="sxs-lookup"><span data-stu-id="814cf-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="814cf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="814cf-110">EXAMPLES</span></span>

### <span data-ttu-id="814cf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="814cf-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="814cf-112">Получить последнюю накладную по подписке.</span><span class="sxs-lookup"><span data-stu-id="814cf-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="814cf-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="814cf-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="814cf-114">Получение счета по подписке с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="814cf-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="814cf-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="814cf-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="814cf-116">Получите все доступные счета по подписке в обратном хронологическом порядке, начиная с самого последнего счета, без URL-адреса скачивания.</span><span class="sxs-lookup"><span data-stu-id="814cf-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="814cf-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="814cf-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="814cf-118">Получение последних 10 накладных по подписке и включение URL-адреса скачивания в результат.</span><span class="sxs-lookup"><span data-stu-id="814cf-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="814cf-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="814cf-119">PARAMETERS</span></span>

### <span data-ttu-id="814cf-120">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="814cf-120">-GenerateDownloadUrl</span></span>
<span data-ttu-id="814cf-121">Создание URL-адреса скачивания для счетов.</span><span class="sxs-lookup"><span data-stu-id="814cf-121">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="814cf-122">-Последние</span><span class="sxs-lookup"><span data-stu-id="814cf-122">-Latest</span></span>
<span data-ttu-id="814cf-123">Получить последнюю накладную.</span><span class="sxs-lookup"><span data-stu-id="814cf-123">Get the latest invoice.</span></span>

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

### <span data-ttu-id="814cf-124">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="814cf-124">-MaxCount</span></span>
<span data-ttu-id="814cf-125">Определяет максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="814cf-125">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="814cf-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="814cf-126">-Name</span></span>
<span data-ttu-id="814cf-127">Имя определенного счета-фактуры, который вы хотите получить или является последним, если не указан.</span><span class="sxs-lookup"><span data-stu-id="814cf-127">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="814cf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="814cf-128">-DefaultProfile</span></span>
<span data-ttu-id="814cf-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="814cf-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="814cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="814cf-130">CommonParameters</span></span>
<span data-ttu-id="814cf-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="814cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="814cf-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="814cf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="814cf-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="814cf-133">INPUTS</span></span>

### <span data-ttu-id="814cf-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="814cf-134">None</span></span>

## <span data-ttu-id="814cf-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="814cf-135">OUTPUTS</span></span>

### <span data-ttu-id="814cf-136">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. выставление счетов, версия = 1.0.0.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="814cf-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Billing.Models.Invoice, Microsoft.Azure.Commands.Billing, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="814cf-137">Microsoft. Azure. Management. Bill. Models. Invoice</span><span class="sxs-lookup"><span data-stu-id="814cf-137">Microsoft.Azure.Management.Billing.Models.Invoice</span></span>

## <span data-ttu-id="814cf-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="814cf-138">NOTES</span></span>

## <span data-ttu-id="814cf-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="814cf-139">RELATED LINKS</span></span>

