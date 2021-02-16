---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 04c8153bae884a074a8db10e8f4330f26c4c5502
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213121"
---
# <span data-ttu-id="0da07-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0da07-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0da07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0da07-102">SYNOPSIS</span></span>
<span data-ttu-id="0da07-103">Обновления и набор записей в частной зоне DNS.</span><span class="sxs-lookup"><span data-stu-id="0da07-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="0da07-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0da07-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0da07-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0da07-105">DESCRIPTION</span></span>
<span data-ttu-id="0da07-106">Новый Set-AzPrivateDnsRecordSet обновляет набор записей в частной службе DNS Azure из локального объекта RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0da07-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="0da07-107">Объект RecordSet можно передать в качестве параметра или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0da07-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="0da07-108">Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da07-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="0da07-109">Набор записей не обновляется, если он был изменен в частных DNS Azure после извлечения локального объекта RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0da07-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="0da07-110">Это обеспечивает защиту от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="0da07-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="0da07-111">Вы можете скрыть это поведение с помощью параметра Overwrite, который обновляет набор записей независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="0da07-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="0da07-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0da07-112">EXAMPLES</span></span>

### <span data-ttu-id="0da07-113">Пример 1. Обновление набора записей</span><span class="sxs-lookup"><span data-stu-id="0da07-113">Example 1: Update a record set</span></span>
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

<span data-ttu-id="0da07-114">Первая команда использует Get-AzPrivateDnsRecordSet для получения указанного набора записей, а затем сохраняет его в $RecordSet переменной.</span><span class="sxs-lookup"><span data-stu-id="0da07-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="0da07-115">Вторая и третья команды — это внестроковые операции по добавлению в набор записей A двух записей.</span><span class="sxs-lookup"><span data-stu-id="0da07-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="0da07-116">Конечная команда использует Set-AzPrivateDnsRecordSet командлет для фиксации обновления.</span><span class="sxs-lookup"><span data-stu-id="0da07-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="0da07-117">Пример 2. Обновление записи SOA</span><span class="sxs-lookup"><span data-stu-id="0da07-117">Example 2: Update an SOA record</span></span>
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

<span data-ttu-id="0da07-118">Первая команда использует Get-AzPrivateDnsRecordSet для получения указанного набора записей, а затем сохраняет его в $RecordSet переменной.</span><span class="sxs-lookup"><span data-stu-id="0da07-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="0da07-119">Вторая команда обновляет указанную запись SOA в $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0da07-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="0da07-120">Для распространения обновления в Set-AzPrivateDnsRecordSet используется командлет $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0da07-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="0da07-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0da07-121">PARAMETERS</span></span>

### <span data-ttu-id="0da07-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da07-122">-DefaultProfile</span></span>
<span data-ttu-id="0da07-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0da07-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da07-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="0da07-124">-Overwrite</span></span>
<span data-ttu-id="0da07-125">Не используйте поле ETag параметра RecordSet для оптимистических проверок concurrency.</span><span class="sxs-lookup"><span data-stu-id="0da07-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="0da07-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="0da07-126">-RecordSet</span></span>
<span data-ttu-id="0da07-127">Набор записей, в который нужно добавить запись.</span><span class="sxs-lookup"><span data-stu-id="0da07-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="0da07-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0da07-128">-Confirm</span></span>
<span data-ttu-id="0da07-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da07-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da07-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da07-130">-WhatIf</span></span>
<span data-ttu-id="0da07-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da07-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da07-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0da07-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da07-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da07-133">CommonParameters</span></span>
<span data-ttu-id="0da07-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da07-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da07-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da07-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da07-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0da07-136">INPUTS</span></span>

### <span data-ttu-id="0da07-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0da07-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0da07-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0da07-138">OUTPUTS</span></span>

### <span data-ttu-id="0da07-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0da07-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0da07-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0da07-140">NOTES</span></span>

## <span data-ttu-id="0da07-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0da07-141">RELATED LINKS</span></span>
