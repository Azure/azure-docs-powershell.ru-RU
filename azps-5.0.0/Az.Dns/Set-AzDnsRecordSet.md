---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248719"
---
# <span data-ttu-id="4c0b1-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0b1-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="4c0b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0b1-103">Обновляет набор записей DNS.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="4c0b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c0b1-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c0b1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c0b1-105">DESCRIPTION</span></span>
<span data-ttu-id="4c0b1-106">Командлет **Set-AzDnsRecordSet** обновляет набор записей в службе DNS Azure из локального объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="4c0b1-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="4c0b1-107">Вы можете передать объект **набора записей** как параметр или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="4c0b1-108">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4c0b1-109">Набор записей не обновляется, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="4c0b1-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="4c0b1-110">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="4c0b1-111">Это поведение можно отключить с помощью параметра *перезаписи* , который обновляет набор записей независимо от количества параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="4c0b1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c0b1-112">EXAMPLES</span></span>

### <span data-ttu-id="4c0b1-113">Пример 1: обновление набор записей</span><span class="sxs-lookup"><span data-stu-id="4c0b1-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="4c0b1-114">Первая команда использует командлет Get-AzDnsRecordSet для получения указанного множества записей и сохраняет его в переменной $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="4c0b1-115">Вторая и третья команды — это автономные операции, позволяющие добавить в набор записей две записи.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="4c0b1-116">В последней команде используется командлет **Set-AzDnsRecordSet** , чтобы зафиксировать обновление.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="4c0b1-117">Пример 2: Обновление записи SOA</span><span class="sxs-lookup"><span data-stu-id="4c0b1-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="4c0b1-118">Первая команда использует командлет **Get-AzDnsRecordset** для получения указанного множества записей и сохраняет ее в переменной $Recordset.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="4c0b1-119">Вторая команда обновляет указанную запись SOA в $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="4c0b1-120">В последней команде используется командлет **Set-AzDnsRecordSet** , чтобы распространить обновление в $Recordset.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="4c0b1-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c0b1-121">PARAMETERS</span></span>

### <span data-ttu-id="4c0b1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0b1-122">-DefaultProfile</span></span>
<span data-ttu-id="4c0b1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4c0b1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c0b1-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="4c0b1-124">-Overwrite</span></span>
<span data-ttu-id="4c0b1-125">Указывает, что нужно обновить набор записей независимо от одновременно выполняемых изменений.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="4c0b1-126">Набор записей не будет обновлен, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="4c0b1-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="4c0b1-127">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="4c0b1-128">Чтобы отменить это поведение, можно использовать параметр *overwrite* , который приводит к обновлению набора записей независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="4c0b1-129">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="4c0b1-129">-RecordSet</span></span>
<span data-ttu-id="4c0b1-130">Указывает **набор записей** для обновления.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0b1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c0b1-131">-Confirm</span></span>
<span data-ttu-id="4c0b1-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c0b1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c0b1-133">-WhatIf</span></span>
<span data-ttu-id="4c0b1-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c0b1-135">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c0b1-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c0b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0b1-137">CommonParameters</span></span>
<span data-ttu-id="4c0b1-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0b1-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c0b1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0b1-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c0b1-140">INPUTS</span></span>

### <span data-ttu-id="4c0b1-141">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0b1-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="4c0b1-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c0b1-142">OUTPUTS</span></span>

### <span data-ttu-id="4c0b1-143">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0b1-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="4c0b1-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c0b1-144">NOTES</span></span>
<span data-ttu-id="4c0b1-145">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4c0b1-146">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="4c0b1-147">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="4c0b1-148">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4c0b1-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="4c0b1-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c0b1-149">RELATED LINKS</span></span>

[<span data-ttu-id="4c0b1-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0b1-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="4c0b1-151">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0b1-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="4c0b1-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4c0b1-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)
