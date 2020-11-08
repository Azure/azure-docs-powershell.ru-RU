---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 04c8153bae884a074a8db10e8f4330f26c4c5502
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065475"
---
# <span data-ttu-id="0e005-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0e005-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0e005-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e005-102">SYNOPSIS</span></span>
<span data-ttu-id="0e005-103">Обновляет или устанавливает набор записей в частной зоне DNS.</span><span class="sxs-lookup"><span data-stu-id="0e005-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="0e005-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e005-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e005-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e005-105">DESCRIPTION</span></span>
<span data-ttu-id="0e005-106">Командлет Set-AzPrivateDnsRecordSet обновляет набор записей в частной службе DNS службы Azure из локального объекта набора записей.</span><span class="sxs-lookup"><span data-stu-id="0e005-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="0e005-107">Вы можете передать объект набора записей как параметр или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0e005-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="0e005-108">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0e005-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="0e005-109">Набор записей не обновляется, если он был изменен в службе Azure Private DNS, так как был получен объект локального набора записей.</span><span class="sxs-lookup"><span data-stu-id="0e005-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="0e005-110">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="0e005-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="0e005-111">Это поведение можно отключить с помощью параметра перезаписи, который обновляет набор записей независимо от количества параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="0e005-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="0e005-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e005-112">EXAMPLES</span></span>

### <span data-ttu-id="0e005-113">Пример 1: обновление набор записей</span><span class="sxs-lookup"><span data-stu-id="0e005-113">Example 1: Update a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0e005-114">Первая команда использует командлет Get-AzPrivateDnsRecordSet для получения указанного множества записей и сохраняет его в переменной $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0e005-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="0e005-115">Вторая и третья команды — это автономные операции, позволяющие добавить в набор записей две записи.</span><span class="sxs-lookup"><span data-stu-id="0e005-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="0e005-116">В последней команде используется командлет Set-AzPrivateDnsRecordSet, чтобы зафиксировать обновление.</span><span class="sxs-lookup"><span data-stu-id="0e005-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="0e005-117">Пример 2: Обновление записи SOA</span><span class="sxs-lookup"><span data-stu-id="0e005-117">Example 2: Update an SOA record</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0e005-118">Первая команда использует командлет Get-AzPrivateDnsRecordSet для получения указанного множества записей и сохраняет его в переменной $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0e005-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="0e005-119">Вторая команда обновляет указанную запись SOA в $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0e005-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="0e005-120">В последней команде используется командлет Set-AzPrivateDnsRecordSet для распространения обновления в $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0e005-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="0e005-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e005-121">PARAMETERS</span></span>

### <span data-ttu-id="0e005-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e005-122">-DefaultProfile</span></span>
<span data-ttu-id="0e005-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e005-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e005-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="0e005-124">-Overwrite</span></span>
<span data-ttu-id="0e005-125">Не используйте поле ETag в параметре RecordSet для проверки оптимистического параллелизма.</span><span class="sxs-lookup"><span data-stu-id="0e005-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="0e005-126">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="0e005-126">-RecordSet</span></span>
<span data-ttu-id="0e005-127">Настройка записи, в которую нужно добавить запись.</span><span class="sxs-lookup"><span data-stu-id="0e005-127">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e005-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e005-128">-Confirm</span></span>
<span data-ttu-id="0e005-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e005-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e005-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e005-130">-WhatIf</span></span>
<span data-ttu-id="0e005-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e005-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e005-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e005-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e005-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e005-133">CommonParameters</span></span>
<span data-ttu-id="0e005-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e005-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e005-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e005-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e005-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e005-136">INPUTS</span></span>

### <span data-ttu-id="0e005-137">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0e005-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0e005-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e005-138">OUTPUTS</span></span>

### <span data-ttu-id="0e005-139">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0e005-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0e005-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e005-140">NOTES</span></span>

## <span data-ttu-id="0e005-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e005-141">RELATED LINKS</span></span>
