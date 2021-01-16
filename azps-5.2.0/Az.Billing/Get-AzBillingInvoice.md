---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397636"
---
# <span data-ttu-id="41ec8-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="41ec8-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="41ec8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="41ec8-103">Получите счета-фактуры по подписке.</span><span class="sxs-lookup"><span data-stu-id="41ec8-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="41ec8-104">Получить счета-фактуры для учетной записи выставления счетов и профиля выставления счетов</span><span class="sxs-lookup"><span data-stu-id="41ec8-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="41ec8-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41ec8-105">SYNTAX</span></span>

### <span data-ttu-id="41ec8-106">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41ec8-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="41ec8-107">Последняя версия</span><span class="sxs-lookup"><span data-stu-id="41ec8-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="41ec8-108">Один</span><span class="sxs-lookup"><span data-stu-id="41ec8-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41ec8-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41ec8-109">DESCRIPTION</span></span>
<span data-ttu-id="41ec8-110">Для подписки на счет выставляются счета- инициализирующая его **cmdlet Get-AzBillingInvoice.**</span><span class="sxs-lookup"><span data-stu-id="41ec8-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="41ec8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41ec8-111">EXAMPLES</span></span>

### <span data-ttu-id="41ec8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41ec8-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="41ec8-113">Получите последний счет за подписку.</span><span class="sxs-lookup"><span data-stu-id="41ec8-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="41ec8-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="41ec8-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="41ec8-115">Получите счет за подписку с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="41ec8-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="41ec8-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="41ec8-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="41ec8-117">Получить все доступные счета за подписку в обратном хронологическом порядке, начиная с самого последнего счета без url-адреса скачивания.</span><span class="sxs-lookup"><span data-stu-id="41ec8-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="41ec8-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="41ec8-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="41ec8-119">Получите последние 10 счетов за подписку и включите в результат URL-адрес для скачивания.</span><span class="sxs-lookup"><span data-stu-id="41ec8-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="41ec8-120">Пример 5</span><span class="sxs-lookup"><span data-stu-id="41ec8-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="41ec8-121">Получите конкретный счет по имени и включите в результат URL-адрес для скачивания.</span><span class="sxs-lookup"><span data-stu-id="41ec8-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="41ec8-122">Пример 6</span><span class="sxs-lookup"><span data-stu-id="41ec8-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="41ec8-123">Поисайте счета по имени учетной записи выставления счетов и включите в результат URL-адрес для скачивания каждого счета.</span><span class="sxs-lookup"><span data-stu-id="41ec8-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="41ec8-124">Пример 7</span><span class="sxs-lookup"><span data-stu-id="41ec8-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="41ec8-125">Получите определенный счет по имени счета и имени учетной записи выставления счетов и включите URL-адрес для скачивания каждого счета в результатах.</span><span class="sxs-lookup"><span data-stu-id="41ec8-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="41ec8-126">Пример 8</span><span class="sxs-lookup"><span data-stu-id="41ec8-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="41ec8-127">Получите последний счет по имени учетной записи выставления счетов и включите в результат URL-адрес для скачивания счета.</span><span class="sxs-lookup"><span data-stu-id="41ec8-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="41ec8-128">Пример 9</span><span class="sxs-lookup"><span data-stu-id="41ec8-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="41ec8-129">Получите последние 10 счетов для конкретной учетной записи выставления счетов и определенного профиля выставления счетов и включите в результат URL-адрес для скачивания.</span><span class="sxs-lookup"><span data-stu-id="41ec8-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="41ec8-130">Пример 10</span><span class="sxs-lookup"><span data-stu-id="41ec8-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="41ec8-131">Получите последнюю версию счета по имени учетной записи выставления счетов и имени профиля выставления счетов и укайте в результатах URL-адрес для скачивания счета.</span><span class="sxs-lookup"><span data-stu-id="41ec8-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="41ec8-132">Пример 10</span><span class="sxs-lookup"><span data-stu-id="41ec8-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="41ec8-133">Поставлять счета по имени учетной записи выставления счетов и имени профиля выставления счетов за период выставления счетов, определенный датой и датой окончания расчетного периода.</span><span class="sxs-lookup"><span data-stu-id="41ec8-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="41ec8-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41ec8-134">PARAMETERS</span></span>

### <span data-ttu-id="41ec8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ec8-135">-DefaultProfile</span></span>
<span data-ttu-id="41ec8-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="41ec8-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41ec8-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="41ec8-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="41ec8-138">Создание URL-адреса для скачивания счетов.</span><span class="sxs-lookup"><span data-stu-id="41ec8-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="41ec8-139">-Последняя версия</span><span class="sxs-lookup"><span data-stu-id="41ec8-139">-Latest</span></span>
<span data-ttu-id="41ec8-140">Получите последний счет.</span><span class="sxs-lookup"><span data-stu-id="41ec8-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="41ec8-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="41ec8-141">-MaxCount</span></span>
<span data-ttu-id="41ec8-142">Определяет максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="41ec8-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="41ec8-143">-Name</span><span class="sxs-lookup"><span data-stu-id="41ec8-143">-Name</span></span>
<span data-ttu-id="41ec8-144">Имя определенного счета, который нужно получить, или самые последние, если не указаны.</span><span class="sxs-lookup"><span data-stu-id="41ec8-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="41ec8-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="41ec8-145">-BillingAccountName</span></span>
<span data-ttu-id="41ec8-146">Имя определенной учетной записи выставления счетов для получения счетов.</span><span class="sxs-lookup"><span data-stu-id="41ec8-146">Name of a specific billing account to get invoices for.</span></span>

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

### <span data-ttu-id="41ec8-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="41ec8-147">-BillingProfileName</span></span>
<span data-ttu-id="41ec8-148">Имя определенного профиля выставления счетов для получения счетов.</span><span class="sxs-lookup"><span data-stu-id="41ec8-148">Name of a specific billing profile to get invoices for.</span></span>

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

### <span data-ttu-id="41ec8-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="41ec8-149">-PeriodStartDate</span></span>
<span data-ttu-id="41ec8-150">Дата начала счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="41ec8-150">Start date for invoice.</span></span>

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

### <span data-ttu-id="41ec8-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="41ec8-151">-PeriodEndDate</span></span>
<span data-ttu-id="41ec8-152">Дата окончания для счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="41ec8-152">End date for invoice.</span></span>

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



### <span data-ttu-id="41ec8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ec8-153">CommonParameters</span></span>
<span data-ttu-id="41ec8-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41ec8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ec8-155">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41ec8-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ec8-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41ec8-156">INPUTS</span></span>

### <span data-ttu-id="41ec8-157">Нет</span><span class="sxs-lookup"><span data-stu-id="41ec8-157">None</span></span>

## <span data-ttu-id="41ec8-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41ec8-158">OUTPUTS</span></span>

### <span data-ttu-id="41ec8-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span><span class="sxs-lookup"><span data-stu-id="41ec8-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="41ec8-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41ec8-160">NOTES</span></span>

## <span data-ttu-id="41ec8-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41ec8-161">RELATED LINKS</span></span>
