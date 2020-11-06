---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: 9db3efc71b751f291c5bb8636246ed6927200c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559816"
---
# <span data-ttu-id="ef131-101">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef131-101">Set-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="ef131-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef131-102">SYNOPSIS</span></span>
<span data-ttu-id="ef131-103">Обновляет набор записей DNS.</span><span class="sxs-lookup"><span data-stu-id="ef131-103">Updates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef131-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef131-104">SYNTAX</span></span>

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef131-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef131-105">DESCRIPTION</span></span>
<span data-ttu-id="ef131-106">Командлет **Set-AzureRmDnsRecordSet** обновляет набор записей в службе DNS Azure из локального объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ef131-106">The **Set-AzureRmDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="ef131-107">Вы можете передать объект **набора записей** как параметр или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ef131-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="ef131-108">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ef131-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="ef131-109">Набор записей не обновляется, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ef131-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="ef131-110">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="ef131-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="ef131-111">Это поведение можно отключить с помощью параметра *перезаписи* , который обновляет набор записей независимо от количества параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="ef131-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="ef131-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef131-112">EXAMPLES</span></span>

### <span data-ttu-id="ef131-113">Пример 1: обновление набор записей</span><span class="sxs-lookup"><span data-stu-id="ef131-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ef131-114">Первая команда использует командлет Get-AzureRmDnsRecordSet для получения указанного множества записей и сохраняет его в переменной $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ef131-114">The first command uses the Get-AzureRmDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="ef131-115">Вторая и третья команды — это автономные операции, позволяющие добавить в набор записей две записи.</span><span class="sxs-lookup"><span data-stu-id="ef131-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="ef131-116">В последней команде используется командлет **Set-AzureRmDnsRecordSet** , чтобы зафиксировать обновление.</span><span class="sxs-lookup"><span data-stu-id="ef131-116">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="ef131-117">Пример 2: Обновление записи SOA</span><span class="sxs-lookup"><span data-stu-id="ef131-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="ef131-118">Первая команда использует командлет **Get-AzureRmDnsRecordset** для получения указанного множества записей и сохраняет ее в переменной $Recordset.</span><span class="sxs-lookup"><span data-stu-id="ef131-118">The first command uses the **Get-AzureRmDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="ef131-119">Вторая команда обновляет указанную запись SOA в $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ef131-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="ef131-120">В последней команде используется командлет **Set-AzureRmDnsRecordSet** , чтобы распространить обновление в $Recordset.</span><span class="sxs-lookup"><span data-stu-id="ef131-120">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="ef131-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef131-121">PARAMETERS</span></span>

### <span data-ttu-id="ef131-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ef131-122">-Overwrite</span></span>
<span data-ttu-id="ef131-123">Указывает, что нужно обновить набор записей независимо от одновременно выполняемых изменений.</span><span class="sxs-lookup"><span data-stu-id="ef131-123">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="ef131-124">Набор записей не будет обновлен, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ef131-124">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="ef131-125">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="ef131-125">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="ef131-126">Чтобы отменить это поведение, можно использовать параметр *overwrite* , который приводит к обновлению набора записей независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="ef131-126">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="ef131-127">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="ef131-127">-RecordSet</span></span>
<span data-ttu-id="ef131-128">Указывает **набор записей** для обновления.</span><span class="sxs-lookup"><span data-stu-id="ef131-128">Specifies the **RecordSet** to update.</span></span>

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

### <span data-ttu-id="ef131-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef131-129">-Confirm</span></span>
<span data-ttu-id="ef131-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef131-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef131-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef131-131">-WhatIf</span></span>
<span data-ttu-id="ef131-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef131-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef131-133">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef131-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef131-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef131-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef131-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef131-135">-DefaultProfile</span></span>
<span data-ttu-id="ef131-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef131-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef131-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef131-137">CommonParameters</span></span>
<span data-ttu-id="ef131-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef131-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef131-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef131-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef131-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef131-140">INPUTS</span></span>

### <span data-ttu-id="ef131-141">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef131-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="ef131-142">Вы можете передать в этот командлет объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ef131-142">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="ef131-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef131-143">OUTPUTS</span></span>

### <span data-ttu-id="ef131-144">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef131-144">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="ef131-145">Этот командлет возвращает объект, который представляет обновленный объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ef131-145">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="ef131-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef131-146">NOTES</span></span>
<span data-ttu-id="ef131-147">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ef131-147">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ef131-148">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="ef131-148">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="ef131-149">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="ef131-149">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ef131-150">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ef131-150">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="ef131-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef131-151">RELATED LINKS</span></span>

[<span data-ttu-id="ef131-152">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef131-152">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ef131-153">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef131-153">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ef131-154">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef131-154">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)
