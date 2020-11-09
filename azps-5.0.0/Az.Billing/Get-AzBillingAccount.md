---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317285"
---
# <span data-ttu-id="792ec-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="792ec-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="792ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="792ec-102">SYNOPSIS</span></span>
<span data-ttu-id="792ec-103">Получение счетов для выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="792ec-103">Get billing accounts.</span></span>

## <span data-ttu-id="792ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="792ec-104">SYNTAX</span></span>

### <span data-ttu-id="792ec-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="792ec-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="792ec-106">Единственное</span><span class="sxs-lookup"><span data-stu-id="792ec-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="792ec-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="792ec-107">DESCRIPTION</span></span>
<span data-ttu-id="792ec-108">Командлет **Get-AzBillingAccount** получает учетные записи выставления счетов, пользователь может получить к ним доступ.</span><span class="sxs-lookup"><span data-stu-id="792ec-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="792ec-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="792ec-109">EXAMPLES</span></span>

### <span data-ttu-id="792ec-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="792ec-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="792ec-111">Получить доступ ко всем учетным записям для выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="792ec-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="792ec-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="792ec-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="792ec-113">Получение счета для выставления счетов с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="792ec-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="792ec-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="792ec-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="792ec-115">Получить доступ ко всем учетным записям для выставления счетов и включить в результат этот адрес.</span><span class="sxs-lookup"><span data-stu-id="792ec-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="792ec-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="792ec-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="792ec-117">Получить доступ ко всем учетным записям для выставления счетов и включить в результат профили выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="792ec-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="792ec-118">Пример 5</span><span class="sxs-lookup"><span data-stu-id="792ec-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="792ec-119">Получить доступ ко всем учетным записям для выставления счетов, а также включить в него профили выставления счетов и подсчеты.</span><span class="sxs-lookup"><span data-stu-id="792ec-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="792ec-120">Пример 6</span><span class="sxs-lookup"><span data-stu-id="792ec-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="792ec-121">Получить счет для выставления счетов с указанным именем и включить в него адрес, профили выставления счетов и разделы счета.</span><span class="sxs-lookup"><span data-stu-id="792ec-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="792ec-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="792ec-122">PARAMETERS</span></span>

### <span data-ttu-id="792ec-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792ec-123">-DefaultProfile</span></span>
<span data-ttu-id="792ec-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="792ec-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="792ec-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="792ec-125">-IncludeAddress</span></span>
<span data-ttu-id="792ec-126">Включите адрес счета выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="792ec-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="792ec-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="792ec-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="792ec-128">Включить профили выставления счетов в счет выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="792ec-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="792ec-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="792ec-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="792ec-130">Включите профили выставления счетов в раздел счета для выставления счетов и счета.</span><span class="sxs-lookup"><span data-stu-id="792ec-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="792ec-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="792ec-131">-Name</span></span>
<span data-ttu-id="792ec-132">Название определенного счета выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="792ec-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="792ec-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="792ec-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="792ec-134">Список сущностей выставления счетов для выставления счетов, которую можно использовать в качестве входных данных для создания подписки.</span><span class="sxs-lookup"><span data-stu-id="792ec-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792ec-135">CommonParameters</span></span>
<span data-ttu-id="792ec-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="792ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792ec-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="792ec-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792ec-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="792ec-138">INPUTS</span></span>

### <span data-ttu-id="792ec-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="792ec-139">None</span></span>

## <span data-ttu-id="792ec-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="792ec-140">OUTPUTS</span></span>

### <span data-ttu-id="792ec-141">Microsoft. Azure. Commands. Bill. Models. PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="792ec-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="792ec-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="792ec-142">NOTES</span></span>

## <span data-ttu-id="792ec-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="792ec-143">RELATED LINKS</span></span>
