---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 2b04478e80010f0edfac9488d45b36700db45eec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567130"
---
# <span data-ttu-id="82f6d-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="82f6d-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="82f6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="82f6d-103">Создание новой зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="82f6d-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82f6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82f6d-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82f6d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82f6d-105">DESCRIPTION</span></span>
<span data-ttu-id="82f6d-106">Командлет **New-AzureRmDnsZone** создает новую зону DNS (Domain Name System) в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82f6d-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="82f6d-107">Необходимо указать уникальное имя зоны DNS для параметра *Name* , иначе командлет будет возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="82f6d-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="82f6d-108">После создания зоны используйте командлет New-AzureRmDnsRecordSet для создания наборов записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="82f6d-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="82f6d-109">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="82f6d-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="82f6d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82f6d-110">EXAMPLES</span></span>

### <span data-ttu-id="82f6d-111">Пример 1: создание зоны DNS</span><span class="sxs-lookup"><span data-stu-id="82f6d-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="82f6d-112">Эта команда создает новую зону DNS с именем myzone.com в заданной группе ресурсов, а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="82f6d-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="82f6d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82f6d-113">PARAMETERS</span></span>

### <span data-ttu-id="82f6d-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82f6d-114">-Name</span></span>
<span data-ttu-id="82f6d-115">Указывает имя зоны DNS, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="82f6d-115">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82f6d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f6d-116">-ResourceGroupName</span></span>
<span data-ttu-id="82f6d-117">Указывает группу ресурсов, в которой нужно создать зону.</span><span class="sxs-lookup"><span data-stu-id="82f6d-117">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82f6d-118">-Тег</span><span class="sxs-lookup"><span data-stu-id="82f6d-118">-Tag</span></span>
<span data-ttu-id="82f6d-119">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="82f6d-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="82f6d-120">Например:</span><span class="sxs-lookup"><span data-stu-id="82f6d-120">For example:</span></span>

<span data-ttu-id="82f6d-121">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="82f6d-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82f6d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82f6d-122">-Confirm</span></span>
<span data-ttu-id="82f6d-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="82f6d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f6d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f6d-124">-WhatIf</span></span>
<span data-ttu-id="82f6d-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82f6d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82f6d-126">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82f6d-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82f6d-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="82f6d-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f6d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f6d-128">-DefaultProfile</span></span>
<span data-ttu-id="82f6d-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82f6d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82f6d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f6d-130">CommonParameters</span></span>
<span data-ttu-id="82f6d-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82f6d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f6d-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82f6d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f6d-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82f6d-133">INPUTS</span></span>

### <span data-ttu-id="82f6d-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="82f6d-134">None</span></span>
<span data-ttu-id="82f6d-135">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="82f6d-135">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="82f6d-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82f6d-136">OUTPUTS</span></span>

### <span data-ttu-id="82f6d-137">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="82f6d-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="82f6d-138">Этот командлет возвращает объект Microsoft. Azure. Commands. DNS. DnsZone, который представляет новую зону DNS.</span><span class="sxs-lookup"><span data-stu-id="82f6d-138">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="82f6d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="82f6d-139">NOTES</span></span>
<span data-ttu-id="82f6d-140">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="82f6d-140">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="82f6d-141">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="82f6d-141">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="82f6d-142">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="82f6d-142">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="82f6d-143">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="82f6d-143">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="82f6d-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82f6d-144">RELATED LINKS</span></span>

[<span data-ttu-id="82f6d-145">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="82f6d-145">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="82f6d-146">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="82f6d-146">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="82f6d-147">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="82f6d-147">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
