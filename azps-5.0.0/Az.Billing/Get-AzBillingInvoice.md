---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248429"
---
# <span data-ttu-id="d3596-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="d3596-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="d3596-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3596-102">SYNOPSIS</span></span>
<span data-ttu-id="d3596-103">Получение выставления счетов для подписки на план.</span><span class="sxs-lookup"><span data-stu-id="d3596-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="d3596-104">Получение счетов-фактур для счета выставления счетов и профиля выставления счетов</span><span class="sxs-lookup"><span data-stu-id="d3596-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="d3596-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3596-105">SYNTAX</span></span>

### <span data-ttu-id="d3596-106">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3596-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="d3596-107">Последнюю</span><span class="sxs-lookup"><span data-stu-id="d3596-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="d3596-108">Единственное</span><span class="sxs-lookup"><span data-stu-id="d3596-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3596-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3596-109">DESCRIPTION</span></span>
<span data-ttu-id="d3596-110">Командлет **Get-AzBillingInvoice** получает счета для выставления счетов по подписке.</span><span class="sxs-lookup"><span data-stu-id="d3596-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="d3596-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3596-111">EXAMPLES</span></span>

### <span data-ttu-id="d3596-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3596-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="d3596-113">Получить последнюю накладную по подписке.</span><span class="sxs-lookup"><span data-stu-id="d3596-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="d3596-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d3596-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="d3596-115">Получение счета по подписке с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="d3596-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="d3596-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d3596-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="d3596-117">Получите все доступные счета по подписке в обратном хронологическом порядке, начиная с самого последнего счета, без URL-адреса скачивания.</span><span class="sxs-lookup"><span data-stu-id="d3596-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="d3596-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d3596-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="d3596-119">Получение последних 10 накладных по подписке и включение URL-адреса скачивания в результат.</span><span class="sxs-lookup"><span data-stu-id="d3596-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="d3596-120">Пример 5</span><span class="sxs-lookup"><span data-stu-id="d3596-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="d3596-121">Получение определенного счета по имени и включение URL-адреса скачивания в результат.</span><span class="sxs-lookup"><span data-stu-id="d3596-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="d3596-122">Пример 6</span><span class="sxs-lookup"><span data-stu-id="d3596-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="d3596-123">Получение счетов по названию счета для выставления счетов и включение URL-адреса скачивания для каждой накладной в результате.</span><span class="sxs-lookup"><span data-stu-id="d3596-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="d3596-124">Пример 7</span><span class="sxs-lookup"><span data-stu-id="d3596-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="d3596-125">Получить определенную накладную по названию счета и названию счета для выставления счетов и включить URL-адрес скачивания для каждой накладной в результате.</span><span class="sxs-lookup"><span data-stu-id="d3596-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="d3596-126">Пример 8</span><span class="sxs-lookup"><span data-stu-id="d3596-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="d3596-127">Получить последнюю накладную по названию счета для выставления счетов и включить URL-адрес скачивания для счета в результатах.</span><span class="sxs-lookup"><span data-stu-id="d3596-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="d3596-128">Пример 9</span><span class="sxs-lookup"><span data-stu-id="d3596-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="d3596-129">Получайте последние 10 счетов для определенного счета и определенного профиля выставления счетов и включают в результат URL-адрес скачивания.</span><span class="sxs-lookup"><span data-stu-id="d3596-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="d3596-130">Пример 10</span><span class="sxs-lookup"><span data-stu-id="d3596-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="d3596-131">Получить последнюю накладную по имени счета выставления счетов и имени профиля выставления счетов, а также включить URL-адрес скачивания для счета в результате.</span><span class="sxs-lookup"><span data-stu-id="d3596-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="d3596-132">Пример 10</span><span class="sxs-lookup"><span data-stu-id="d3596-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="d3596-133">Получение счетов по названию счета для выставления счетов и имени профиля выставления счетов за расчетный период, указанный в perioStart дате и periodEnd дате.</span><span class="sxs-lookup"><span data-stu-id="d3596-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="d3596-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3596-134">PARAMETERS</span></span>

### <span data-ttu-id="d3596-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3596-135">-DefaultProfile</span></span>
<span data-ttu-id="d3596-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d3596-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3596-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="d3596-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="d3596-138">Создание URL-адреса скачивания для счетов.</span><span class="sxs-lookup"><span data-stu-id="d3596-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="d3596-139">-Последние</span><span class="sxs-lookup"><span data-stu-id="d3596-139">-Latest</span></span>
<span data-ttu-id="d3596-140">Получить последнюю накладную.</span><span class="sxs-lookup"><span data-stu-id="d3596-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="d3596-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d3596-141">-MaxCount</span></span>
<span data-ttu-id="d3596-142">Определяет максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="d3596-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="d3596-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3596-143">-Name</span></span>
<span data-ttu-id="d3596-144">Имя определенного счета-фактуры, который вы хотите получить или является последним, если не указан.</span><span class="sxs-lookup"><span data-stu-id="d3596-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="d3596-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="d3596-145">-BillingAccountName</span></span>
<span data-ttu-id="d3596-146">Название определенного счета выставления счетов, для которого нужно получить счета.</span><span class="sxs-lookup"><span data-stu-id="d3596-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3596-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="d3596-147">-BillingProfileName</span></span>
<span data-ttu-id="d3596-148">Название определенного профиля выставления счетов, для которого нужно получить счета.</span><span class="sxs-lookup"><span data-stu-id="d3596-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3596-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="d3596-149">-PeriodStartDate</span></span>
<span data-ttu-id="d3596-150">Дата начала счета.</span><span class="sxs-lookup"><span data-stu-id="d3596-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3596-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="d3596-151">-PeriodEndDate</span></span>
<span data-ttu-id="d3596-152">Дата окончания счета.</span><span class="sxs-lookup"><span data-stu-id="d3596-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="d3596-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3596-153">CommonParameters</span></span>
<span data-ttu-id="d3596-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3596-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3596-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3596-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3596-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3596-156">INPUTS</span></span>

### <span data-ttu-id="d3596-157">Ничего</span><span class="sxs-lookup"><span data-stu-id="d3596-157">None</span></span>

## <span data-ttu-id="d3596-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3596-158">OUTPUTS</span></span>

### <span data-ttu-id="d3596-159">Microsoft. Azure. Commands. Bill. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="d3596-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="d3596-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3596-160">NOTES</span></span>

## <span data-ttu-id="d3596-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3596-161">RELATED LINKS</span></span>
