---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsdrive
schema: 2.0.0
ms.openlocfilehash: ec2216a9234086702e8a9331888c04034d13a99f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076629"
---
# <span data-ttu-id="cc4fe-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="cc4fe-101">Get-AzsDrive</span></span>

## <span data-ttu-id="cc4fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="cc4fe-103">Возврат запрошенного диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-103">Return the requested a storage drive.</span></span>

## <span data-ttu-id="cc4fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc4fe-104">SYNTAX</span></span>

### <span data-ttu-id="cc4fe-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc4fe-105">List (Default)</span></span>
```
Get-AzsDrive -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cc4fe-106">Получить</span><span class="sxs-lookup"><span data-stu-id="cc4fe-106">Get</span></span>
```
Get-AzsDrive -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="cc4fe-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cc4fe-107">GetViaIdentity</span></span>
```
Get-AzsDrive -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="cc4fe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc4fe-108">DESCRIPTION</span></span>
<span data-ttu-id="cc4fe-109">Возврат запрошенного диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-109">Return the requested a storage drive.</span></span>

## <span data-ttu-id="cc4fe-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc4fe-110">EXAMPLES</span></span>

### <span data-ttu-id="cc4fe-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="cc4fe-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="cc4fe-112">Получение списка всех дисков хранилища для данного кластера.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="cc4fe-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="cc4fe-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name '{a185d466-4d21-4c1f-9489-7c9c66b6b172}:PD:{fd389cf7-2115-2144-5afe-27910562d6b3}'
```

<span data-ttu-id="cc4fe-114">Получение имени диска хранилища для данного кластера.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="cc4fe-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc4fe-115">PARAMETERS</span></span>

### <span data-ttu-id="cc4fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc4fe-116">-DefaultProfile</span></span>
<span data-ttu-id="cc4fe-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="cc4fe-118">-Filter</span></span>
<span data-ttu-id="cc4fe-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc4fe-120">-InputObject</span></span>
<span data-ttu-id="cc4fe-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-122">-Location</span><span class="sxs-lookup"><span data-stu-id="cc4fe-122">-Location</span></span>
<span data-ttu-id="cc4fe-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc4fe-124">-Name</span></span>
<span data-ttu-id="cc4fe-125">Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-125">Name of the storage drive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc4fe-126">-PassThru</span></span>
<span data-ttu-id="cc4fe-127">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cc4fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc4fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="cc4fe-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-129">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="cc4fe-130">-ScaleUnit</span></span>
<span data-ttu-id="cc4fe-131">Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-131">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="cc4fe-132">-Skip</span></span>
<span data-ttu-id="cc4fe-133">Параметр пропуска OData.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-133">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="cc4fe-134">-StorageSubSystem</span></span>
<span data-ttu-id="cc4fe-135">Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-135">Name of the storage system.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc4fe-136">-SubscriptionId</span></span>
<span data-ttu-id="cc4fe-137">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cc4fe-138">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-139">-Top</span><span class="sxs-lookup"><span data-stu-id="cc4fe-139">-Top</span></span>
<span data-ttu-id="cc4fe-140">Параметр TOP для OData.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-140">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc4fe-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc4fe-141">CommonParameters</span></span>
<span data-ttu-id="cc4fe-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc4fe-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc4fe-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc4fe-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc4fe-144">INPUTS</span></span>

### <span data-ttu-id="cc4fe-145">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cc4fe-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cc4fe-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc4fe-146">OUTPUTS</span></span>

### <span data-ttu-id="cc4fe-147">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20190501. IDrive</span><span class="sxs-lookup"><span data-stu-id="cc4fe-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IDrive</span></span>



## <span data-ttu-id="cc4fe-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc4fe-148">NOTES</span></span>

<span data-ttu-id="cc4fe-149">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc4fe-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cc4fe-151">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="cc4fe-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cc4fe-152">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cc4fe-153">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cc4fe-154">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cc4fe-155">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cc4fe-156">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cc4fe-157">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cc4fe-158">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="cc4fe-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc4fe-159">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cc4fe-160">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cc4fe-161">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cc4fe-162">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cc4fe-163">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cc4fe-164">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cc4fe-165">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cc4fe-166">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cc4fe-167">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cc4fe-168">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cc4fe-169">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cc4fe-170">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cc4fe-171">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cc4fe-172">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cc4fe-173">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc4fe-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cc4fe-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc4fe-174">RELATED LINKS</span></span>

