---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 0b41ff25823e44b31c7ff7677678a332782e7615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911225"
---
# <span data-ttu-id="05d86-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="05d86-101">New-AzDnsZone</span></span>

## <span data-ttu-id="05d86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05d86-102">SYNOPSIS</span></span>
<span data-ttu-id="05d86-103">Создание новой зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="05d86-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="05d86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05d86-104">SYNTAX</span></span>

```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05d86-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05d86-105">DESCRIPTION</span></span>
<span data-ttu-id="05d86-106">Командлет **New-AzDnsZone** создает новую зону DNS (Domain Name System) в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05d86-106">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="05d86-107">Необходимо указать уникальное имя зоны DNS для параметра *Name* , иначе командлет будет возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="05d86-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="05d86-108">После создания зоны используйте командлет New-AzDnsRecordSet для создания наборов записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="05d86-108">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="05d86-109">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="05d86-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="05d86-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05d86-110">EXAMPLES</span></span>

### <span data-ttu-id="05d86-111">Пример 1: создание зоны DNS</span><span class="sxs-lookup"><span data-stu-id="05d86-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="05d86-112">Эта команда создает новую зону DNS с именем myzone.com в заданной группе ресурсов, а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="05d86-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="05d86-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05d86-113">PARAMETERS</span></span>

### <span data-ttu-id="05d86-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="05d86-114">-Name</span></span>
<span data-ttu-id="05d86-115">Указывает имя зоны DNS, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="05d86-115">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d86-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d86-116">-ResourceGroupName</span></span>
<span data-ttu-id="05d86-117">Указывает группу ресурсов, в которой нужно создать зону.</span><span class="sxs-lookup"><span data-stu-id="05d86-117">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d86-118">-Тег</span><span class="sxs-lookup"><span data-stu-id="05d86-118">-Tag</span></span>
<span data-ttu-id="05d86-119">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="05d86-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="05d86-120">Например:</span><span class="sxs-lookup"><span data-stu-id="05d86-120">For example:</span></span>

<span data-ttu-id="05d86-121">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="05d86-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d86-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05d86-122">-Confirm</span></span>
<span data-ttu-id="05d86-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05d86-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d86-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05d86-124">-WhatIf</span></span>
<span data-ttu-id="05d86-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05d86-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05d86-126">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05d86-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05d86-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="05d86-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d86-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d86-128">CommonParameters</span></span>
<span data-ttu-id="05d86-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05d86-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d86-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05d86-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d86-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05d86-131">INPUTS</span></span>

### <span data-ttu-id="05d86-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="05d86-132">None</span></span>

<span data-ttu-id="05d86-133">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="05d86-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="05d86-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05d86-134">OUTPUTS</span></span>

### <span data-ttu-id="05d86-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="05d86-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="05d86-136">Этот командлет возвращает объект Microsoft. Azure. Commands. DNS. DnsZone, который представляет новую зону DNS.</span><span class="sxs-lookup"><span data-stu-id="05d86-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="05d86-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="05d86-137">NOTES</span></span>
<span data-ttu-id="05d86-138">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="05d86-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="05d86-139">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="05d86-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="05d86-140">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="05d86-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="05d86-141">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="05d86-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="05d86-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05d86-142">RELATED LINKS</span></span>

[<span data-ttu-id="05d86-143">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="05d86-143">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="05d86-144">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="05d86-144">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="05d86-145">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="05d86-145">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)