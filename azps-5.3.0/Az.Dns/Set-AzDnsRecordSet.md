---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504936"
---
# <span data-ttu-id="d45ba-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d45ba-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="d45ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d45ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d45ba-103">Обновляет набор записей DNS.</span><span class="sxs-lookup"><span data-stu-id="d45ba-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="d45ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d45ba-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d45ba-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d45ba-105">DESCRIPTION</span></span>
<span data-ttu-id="d45ba-106">**Cmdlet Set-AzDnsRecordSet** обновляет набор записей в службе DNS Azure из локального объекта **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="d45ba-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="d45ba-107">Объект **RecordSet** можно передать в качестве параметра или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d45ba-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="d45ba-108">Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d45ba-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d45ba-109">Набор записей не обновляется, если он был изменен в Azure DNS после извлечения локального объекта **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="d45ba-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="d45ba-110">Это обеспечивает защиту от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="d45ba-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="d45ba-111">Вы можете скрыть это поведение с помощью параметра *Overwrite,* который обновляет набор записей независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="d45ba-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="d45ba-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d45ba-112">EXAMPLES</span></span>

### <span data-ttu-id="d45ba-113">Пример 1. Обновление набора записей</span><span class="sxs-lookup"><span data-stu-id="d45ba-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="d45ba-114">Первая команда использует Get-AzDnsRecordSet для получения указанного набора записей, а затем сохраняет его в $RecordSet переменной.</span><span class="sxs-lookup"><span data-stu-id="d45ba-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="d45ba-115">Вторая и третья команды — это внестроковые операции, которые добавляют две записи A в набор.</span><span class="sxs-lookup"><span data-stu-id="d45ba-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="d45ba-116">В последней команде для фиксации обновления используется командлет **Set-AzDnsRecordSet.**</span><span class="sxs-lookup"><span data-stu-id="d45ba-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="d45ba-117">Пример 2. Обновление записи SOA</span><span class="sxs-lookup"><span data-stu-id="d45ba-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="d45ba-118">Первая команда использует командлет **Get-AzDnsRecordset** для получения указанного набора записей, а затем сохраняет его в $RecordSet переменной.</span><span class="sxs-lookup"><span data-stu-id="d45ba-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="d45ba-119">Вторая команда обновляет указанную запись SOA в $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="d45ba-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="d45ba-120">В последней команде для распространения обновления в $RecordSet используется командлет **Set-AzDnsRecordSet.**</span><span class="sxs-lookup"><span data-stu-id="d45ba-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="d45ba-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d45ba-121">PARAMETERS</span></span>

### <span data-ttu-id="d45ba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45ba-122">-DefaultProfile</span></span>
<span data-ttu-id="d45ba-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d45ba-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d45ba-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="d45ba-124">-Overwrite</span></span>
<span data-ttu-id="d45ba-125">Обновление набора записей независимо от изменений.</span><span class="sxs-lookup"><span data-stu-id="d45ba-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="d45ba-126">Набор записей не будет обновляться, если он был изменен в Azure DNS после извлечения локального объекта **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="d45ba-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="d45ba-127">Это обеспечивает защиту от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="d45ba-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="d45ba-128">Чтобы скрыть это поведение, можно использовать параметр *Overwrite,* что приводит к обновлению набора записей независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="d45ba-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="d45ba-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="d45ba-129">-RecordSet</span></span>
<span data-ttu-id="d45ba-130">Набор **записей, который** нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="d45ba-130">Specifies the **RecordSet** to update.</span></span>

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

### <span data-ttu-id="d45ba-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d45ba-131">-Confirm</span></span>
<span data-ttu-id="d45ba-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d45ba-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d45ba-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d45ba-133">-WhatIf</span></span>
<span data-ttu-id="d45ba-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d45ba-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d45ba-135">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d45ba-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d45ba-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d45ba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d45ba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45ba-137">CommonParameters</span></span>
<span data-ttu-id="d45ba-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d45ba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45ba-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d45ba-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45ba-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d45ba-140">INPUTS</span></span>

### <span data-ttu-id="d45ba-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d45ba-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="d45ba-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d45ba-142">OUTPUTS</span></span>

### <span data-ttu-id="d45ba-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d45ba-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="d45ba-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d45ba-144">NOTES</span></span>
<span data-ttu-id="d45ba-145">С помощью параметра *Confirm* (Подтвердить) можно управлять запросом на подтверждение с помощью этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d45ba-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d45ba-146">По умолчанию с помощью cmdlet вы можете получить подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет значение "Средний" или "Ниже".</span><span class="sxs-lookup"><span data-stu-id="d45ba-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="d45ba-147">Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="d45ba-147">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="d45ba-148">Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="d45ba-148">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="d45ba-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d45ba-149">RELATED LINKS</span></span>

[<span data-ttu-id="d45ba-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d45ba-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="d45ba-151">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d45ba-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="d45ba-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d45ba-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)
