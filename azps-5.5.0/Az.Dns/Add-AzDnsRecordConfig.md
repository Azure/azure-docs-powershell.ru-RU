---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: c9390514ad7680a047ca145c8fe71feda0ab1b51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230428"
---
# <span data-ttu-id="5afd5-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="5afd5-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="5afd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5afd5-102">SYNOPSIS</span></span>
<span data-ttu-id="5afd5-103">Добавляет запись DNS к объекту локального набора записей.</span><span class="sxs-lookup"><span data-stu-id="5afd5-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="5afd5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5afd5-104">SYNTAX</span></span>

### <span data-ttu-id="5afd5-105">A</span><span class="sxs-lookup"><span data-stu-id="5afd5-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5afd5-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="5afd5-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5afd5-107">NS</span><span class="sxs-lookup"><span data-stu-id="5afd5-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5afd5-108">MX</span><span class="sxs-lookup"><span data-stu-id="5afd5-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5afd5-109">PTR</span><span class="sxs-lookup"><span data-stu-id="5afd5-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5afd5-110">TXT</span><span class="sxs-lookup"><span data-stu-id="5afd5-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5afd5-111">SRV</span><span class="sxs-lookup"><span data-stu-id="5afd5-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5afd5-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="5afd5-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5afd5-113">Caa</span><span class="sxs-lookup"><span data-stu-id="5afd5-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5afd5-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5afd5-114">DESCRIPTION</span></span>
<span data-ttu-id="5afd5-115">**Cmdlet Add-AzDnsRecordConfig** добавляет запись DNS системы доменных имен (DNS) к **объекту RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="5afd5-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="5afd5-116">Объект **RecordSet** является автономным объектом, и его изменения не изменяют ответы DNS до запуска Set-AzDnsRecordSet, чтобы сохранить изменение службы DNS Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5afd5-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="5afd5-117">Записи SOA создаются при создания зоны DNS и удаляются при удалении зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="5afd5-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="5afd5-118">Записи SOA нельзя добавлять и удалять, но можно редактировать.</span><span class="sxs-lookup"><span data-stu-id="5afd5-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="5afd5-119">Объект **RecordSet** можно передать этому cmdlet в качестве параметра или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="5afd5-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="5afd5-120">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5afd5-120">EXAMPLES</span></span>

### <span data-ttu-id="5afd5-121">Пример 1. Добавление записи A в набор</span><span class="sxs-lookup"><span data-stu-id="5afd5-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="5afd5-122">В этом примере запись A добавляется в существующий набор.</span><span class="sxs-lookup"><span data-stu-id="5afd5-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="5afd5-123">Пример 2. Добавление записи AAAA в набор</span><span class="sxs-lookup"><span data-stu-id="5afd5-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="5afd5-124">В этом примере запись AAAA добавляется в существующий набор.</span><span class="sxs-lookup"><span data-stu-id="5afd5-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="5afd5-125">Пример 3. Добавление записи CNAME в набор записей</span><span class="sxs-lookup"><span data-stu-id="5afd5-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="5afd5-126">В этом примере запись CNAME добавляется в существующий набор записей.</span><span class="sxs-lookup"><span data-stu-id="5afd5-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="5afd5-127">Так как набор записей CNAME может содержать не более одной записи, сначала он должен быть пустым или удалить существующие записи с помощью remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="5afd5-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="5afd5-128">Пример 4. Добавление записи MX в набор</span><span class="sxs-lookup"><span data-stu-id="5afd5-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="5afd5-129">В этом примере запись MX добавляется в существующий набор.</span><span class="sxs-lookup"><span data-stu-id="5afd5-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="5afd5-130">Имя записи "@" означает набор записей на апексе зоны.</span><span class="sxs-lookup"><span data-stu-id="5afd5-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="5afd5-131">Пример 5. Добавление NS-записи в набор записей</span><span class="sxs-lookup"><span data-stu-id="5afd5-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="5afd5-132">В этом примере NS-запись добавляется в существующий набор.</span><span class="sxs-lookup"><span data-stu-id="5afd5-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="5afd5-133">Пример 6. Добавление записи PTR в набор</span><span class="sxs-lookup"><span data-stu-id="5afd5-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="5afd5-134">В этом примере запись PTR добавляется к существующему набору записей.</span><span class="sxs-lookup"><span data-stu-id="5afd5-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="5afd5-135">Пример 7. Добавление записи SRV в набор записей</span><span class="sxs-lookup"><span data-stu-id="5afd5-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="5afd5-136">В этом примере запись SRV добавляется в существующий набор.</span><span class="sxs-lookup"><span data-stu-id="5afd5-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="5afd5-137">Пример 8. Добавление записи TXT в набор записей</span><span class="sxs-lookup"><span data-stu-id="5afd5-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="5afd5-138">В этом примере запись TXT добавляется в существующий набор.</span><span class="sxs-lookup"><span data-stu-id="5afd5-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="5afd5-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5afd5-139">PARAMETERS</span></span>

### <span data-ttu-id="5afd5-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="5afd5-140">-CaaFlags</span></span>
<span data-ttu-id="5afd5-141">Флаги для добавляемой записи CAA.</span><span class="sxs-lookup"><span data-stu-id="5afd5-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="5afd5-142">Должен быть числом от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="5afd5-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="5afd5-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="5afd5-143">-CaaTag</span></span>
<span data-ttu-id="5afd5-144">Поле тега добавляемой записи CAA.</span><span class="sxs-lookup"><span data-stu-id="5afd5-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="5afd5-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="5afd5-145">-CaaValue</span></span>
<span data-ttu-id="5afd5-146">Поле значения для добавляемой записи CAA.</span><span class="sxs-lookup"><span data-stu-id="5afd5-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="5afd5-147">-Cname</span><span class="sxs-lookup"><span data-stu-id="5afd5-147">-Cname</span></span>
<span data-ttu-id="5afd5-148">Указывает доменное имя для канонической записи (CNAME).</span><span class="sxs-lookup"><span data-stu-id="5afd5-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="5afd5-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5afd5-149">-DefaultProfile</span></span>
<span data-ttu-id="5afd5-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5afd5-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5afd5-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="5afd5-151">-Exchange</span></span>
<span data-ttu-id="5afd5-152">Имя сервера обмена электронной почтой для записи обмена электронной почтой (MX).</span><span class="sxs-lookup"><span data-stu-id="5afd5-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="5afd5-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="5afd5-153">-Ipv4Address</span></span>
<span data-ttu-id="5afd5-154">Определяет IPv4-адрес для записи A.</span><span class="sxs-lookup"><span data-stu-id="5afd5-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="5afd5-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="5afd5-155">-Ipv6Address</span></span>
<span data-ttu-id="5afd5-156">Определяет IPv6-адрес для записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="5afd5-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="5afd5-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="5afd5-157">-Nsdname</span></span>
<span data-ttu-id="5afd5-158">Указывает имя сервера доменных имен для записи сервера доменных имен.</span><span class="sxs-lookup"><span data-stu-id="5afd5-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="5afd5-159">-Port</span><span class="sxs-lookup"><span data-stu-id="5afd5-159">-Port</span></span>
<span data-ttu-id="5afd5-160">Порт для записи службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="5afd5-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="5afd5-161">-Preference</span><span class="sxs-lookup"><span data-stu-id="5afd5-161">-Preference</span></span>
<span data-ttu-id="5afd5-162">Указывает параметр для записи MX.</span><span class="sxs-lookup"><span data-stu-id="5afd5-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="5afd5-163">-Priority</span><span class="sxs-lookup"><span data-stu-id="5afd5-163">-Priority</span></span>
<span data-ttu-id="5afd5-164">Определяет приоритет для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="5afd5-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="5afd5-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="5afd5-165">-Ptrdname</span></span>
<span data-ttu-id="5afd5-166">Указывает целевое доменное имя записи ресурса указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="5afd5-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="5afd5-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="5afd5-167">-RecordSet</span></span>
<span data-ttu-id="5afd5-168">Определяет объект **RecordSet,** который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="5afd5-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="5afd5-169">-Target</span><span class="sxs-lookup"><span data-stu-id="5afd5-169">-Target</span></span>
<span data-ttu-id="5afd5-170">Указывает целевой объект для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="5afd5-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="5afd5-171">-Value</span><span class="sxs-lookup"><span data-stu-id="5afd5-171">-Value</span></span>
<span data-ttu-id="5afd5-172">Определяет значение для записи TXT.</span><span class="sxs-lookup"><span data-stu-id="5afd5-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="5afd5-173">-Weight</span><span class="sxs-lookup"><span data-stu-id="5afd5-173">-Weight</span></span>
<span data-ttu-id="5afd5-174">Определяет вес записи SRV.</span><span class="sxs-lookup"><span data-stu-id="5afd5-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="5afd5-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5afd5-175">CommonParameters</span></span>
<span data-ttu-id="5afd5-176">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5afd5-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5afd5-177">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5afd5-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5afd5-178">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5afd5-178">INPUTS</span></span>

### <span data-ttu-id="5afd5-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5afd5-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="5afd5-180">System.String</span><span class="sxs-lookup"><span data-stu-id="5afd5-180">System.String</span></span>

### <span data-ttu-id="5afd5-181">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="5afd5-181">System.UInt16</span></span>

### <span data-ttu-id="5afd5-182">System.Byte</span><span class="sxs-lookup"><span data-stu-id="5afd5-182">System.Byte</span></span>

## <span data-ttu-id="5afd5-183">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5afd5-183">OUTPUTS</span></span>

### <span data-ttu-id="5afd5-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5afd5-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="5afd5-185">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5afd5-185">NOTES</span></span>

## <span data-ttu-id="5afd5-186">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5afd5-186">RELATED LINKS</span></span>

[<span data-ttu-id="5afd5-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5afd5-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="5afd5-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="5afd5-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="5afd5-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5afd5-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
