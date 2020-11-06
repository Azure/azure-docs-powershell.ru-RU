---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/add-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: cc1f4186d63b67619734cbfad807d114e2be5463
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566819"
---
# <span data-ttu-id="13c3a-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="13c3a-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="13c3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="13c3a-103">Добавляет запись DNS в локальный объект локального множества записей.</span><span class="sxs-lookup"><span data-stu-id="13c3a-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13c3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13c3a-104">SYNTAX</span></span>

### <span data-ttu-id="13c3a-105">Помощью</span><span class="sxs-lookup"><span data-stu-id="13c3a-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13c3a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="13c3a-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13c3a-107">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="13c3a-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13c3a-108">МХ</span><span class="sxs-lookup"><span data-stu-id="13c3a-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13c3a-109">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="13c3a-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13c3a-110">ТХТ</span><span class="sxs-lookup"><span data-stu-id="13c3a-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13c3a-111">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="13c3a-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13c3a-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="13c3a-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13c3a-113">Caa</span><span class="sxs-lookup"><span data-stu-id="13c3a-113">Caa</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13c3a-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13c3a-114">DESCRIPTION</span></span>
<span data-ttu-id="13c3a-115">Командлет **Add-AzureRmDnsRecordConfig** добавляет запись DNS (Domain Name System) в объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="13c3a-115">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="13c3a-116">Объект **Recordset** является автономным объектом, и изменения в нем не изменяют ответы DNS, пока не будет запущен командлет Set-AzureRmDnsRecordSet, чтобы сохранить изменения в службе Microsoft Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="13c3a-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="13c3a-117">Записи SOA создаются при создании зоны DNS и удаляются при удалении зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="13c3a-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="13c3a-118">Вы не можете добавлять и удалять записи SOA, но можете редактировать их.</span><span class="sxs-lookup"><span data-stu-id="13c3a-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="13c3a-119">Вы можете передать объект **набора записей** в этот командлет как параметр или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="13c3a-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="13c3a-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13c3a-120">EXAMPLES</span></span>

### <span data-ttu-id="13c3a-121">Пример 1: Добавление записи A в набор записей</span><span class="sxs-lookup"><span data-stu-id="13c3a-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="13c3a-122">В этом примере к существующему набору записей добавляется запись A.</span><span class="sxs-lookup"><span data-stu-id="13c3a-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="13c3a-123">Пример 2: Добавление записи AAAA в набор записей</span><span class="sxs-lookup"><span data-stu-id="13c3a-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="13c3a-124">В этом примере добавляется запись AAAA в существующий наборы записей.</span><span class="sxs-lookup"><span data-stu-id="13c3a-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="13c3a-125">Пример 3: Добавление записи CNAME в набор записей</span><span class="sxs-lookup"><span data-stu-id="13c3a-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="13c3a-126">В этом примере добавляется запись CNAME к существующему набору записей.</span><span class="sxs-lookup"><span data-stu-id="13c3a-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="13c3a-127">Так как набор записей CNAME может содержать не более одной записи, сначала должна быть пустая набор записей, или существующие записи должны быть удалены с помощью Remove-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="13c3a-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="13c3a-128">Пример 4: Добавление записи MX в набор записей</span><span class="sxs-lookup"><span data-stu-id="13c3a-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="13c3a-129">В этом примере добавляется запись MX в существующий наборы записей.</span><span class="sxs-lookup"><span data-stu-id="13c3a-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="13c3a-130">Имя записи "@" обозначает набор записей на Апексе зоны.</span><span class="sxs-lookup"><span data-stu-id="13c3a-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="13c3a-131">Пример 5: Добавление записи NS в набор записей</span><span class="sxs-lookup"><span data-stu-id="13c3a-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="13c3a-132">В этом примере добавляется запись NS для существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="13c3a-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="13c3a-133">Пример 6: Добавление записи PTR в набор записей</span><span class="sxs-lookup"><span data-stu-id="13c3a-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="13c3a-134">В этом примере к существующему набору записей добавляется запись PTR.</span><span class="sxs-lookup"><span data-stu-id="13c3a-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="13c3a-135">Пример 7: Добавление записи SRV в набор записей</span><span class="sxs-lookup"><span data-stu-id="13c3a-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="13c3a-136">В этом примере добавляется запись SRV для существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="13c3a-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="13c3a-137">Пример 8: Добавление записи TXT в набор записей</span><span class="sxs-lookup"><span data-stu-id="13c3a-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="13c3a-138">В этом примере к существующему набору записей добавляется запись TXT.</span><span class="sxs-lookup"><span data-stu-id="13c3a-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="13c3a-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13c3a-139">PARAMETERS</span></span>

### <span data-ttu-id="13c3a-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="13c3a-140">-CaaFlags</span></span>
<span data-ttu-id="13c3a-141">Флаги для записи CAA, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="13c3a-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="13c3a-142">Должно быть числом от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="13c3a-142">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="13c3a-143">-CaaTag</span></span>
<span data-ttu-id="13c3a-144">Поле тега записи CAA, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="13c3a-144">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="13c3a-145">-CaaValue</span></span>
<span data-ttu-id="13c3a-146">Поле значения для записи CAA, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="13c3a-146">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-147">-CNAME</span><span class="sxs-lookup"><span data-stu-id="13c3a-147">-Cname</span></span>
<span data-ttu-id="13c3a-148">Задает доменное имя для записи канонического имени (CNAME).</span><span class="sxs-lookup"><span data-stu-id="13c3a-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c3a-149">-DefaultProfile</span></span>
<span data-ttu-id="13c3a-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="13c3a-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13c3a-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="13c3a-151">-Exchange</span></span>
<span data-ttu-id="13c3a-152">Указывает имя почтового сервера для записи почтового обменника (MX).</span><span class="sxs-lookup"><span data-stu-id="13c3a-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="13c3a-153">-Ipv4Address</span></span>
<span data-ttu-id="13c3a-154">Задает IPv4-адрес для записи A.</span><span class="sxs-lookup"><span data-stu-id="13c3a-154">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="13c3a-155">-Ipv6Address</span></span>
<span data-ttu-id="13c3a-156">Задает IPv6-адрес для записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="13c3a-156">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="13c3a-157">-Nsdname</span></span>
<span data-ttu-id="13c3a-158">Указывает имя сервера доменных имен для записи сервера доменных имен (NS).</span><span class="sxs-lookup"><span data-stu-id="13c3a-158">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-159">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="13c3a-159">-Port</span></span>
<span data-ttu-id="13c3a-160">Указывает порт для записи службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="13c3a-160">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-161">-Предпочтения</span><span class="sxs-lookup"><span data-stu-id="13c3a-161">-Preference</span></span>
<span data-ttu-id="13c3a-162">Задает приоритет MX-записи.</span><span class="sxs-lookup"><span data-stu-id="13c3a-162">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-163">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="13c3a-163">-Priority</span></span>
<span data-ttu-id="13c3a-164">Указывает приоритет записи SRV.</span><span class="sxs-lookup"><span data-stu-id="13c3a-164">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="13c3a-165">-Ptrdname</span></span>
<span data-ttu-id="13c3a-166">Указывает целевое доменное имя записи ресурса указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="13c3a-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-167">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="13c3a-167">-RecordSet</span></span>
<span data-ttu-id="13c3a-168">Указывает объект **набора записей** , который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="13c3a-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="13c3a-169">-Target</span><span class="sxs-lookup"><span data-stu-id="13c3a-169">-Target</span></span>
<span data-ttu-id="13c3a-170">Указывает целевой объект для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="13c3a-170">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-171">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="13c3a-171">-Value</span></span>
<span data-ttu-id="13c3a-172">Задает значение для записи TXT.</span><span class="sxs-lookup"><span data-stu-id="13c3a-172">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-173">-Weight</span><span class="sxs-lookup"><span data-stu-id="13c3a-173">-Weight</span></span>
<span data-ttu-id="13c3a-174">Определяет вес записи SRV.</span><span class="sxs-lookup"><span data-stu-id="13c3a-174">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c3a-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c3a-175">CommonParameters</span></span>
<span data-ttu-id="13c3a-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13c3a-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c3a-177">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13c3a-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c3a-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13c3a-178">INPUTS</span></span>

### <span data-ttu-id="13c3a-179">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="13c3a-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="13c3a-180">Параметры: набор записей (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13c3a-180">Parameters: RecordSet (ByValue)</span></span>

### <span data-ttu-id="13c3a-181">System. String</span><span class="sxs-lookup"><span data-stu-id="13c3a-181">System.String</span></span>

### <span data-ttu-id="13c3a-182">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="13c3a-182">System.UInt16</span></span>

### <span data-ttu-id="13c3a-183">System. Byte</span><span class="sxs-lookup"><span data-stu-id="13c3a-183">System.Byte</span></span>

## <span data-ttu-id="13c3a-184">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13c3a-184">OUTPUTS</span></span>

### <span data-ttu-id="13c3a-185">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="13c3a-185">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="13c3a-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="13c3a-186">NOTES</span></span>

## <span data-ttu-id="13c3a-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13c3a-187">RELATED LINKS</span></span>

[<span data-ttu-id="13c3a-188">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="13c3a-188">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="13c3a-189">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="13c3a-189">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="13c3a-190">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="13c3a-190">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
