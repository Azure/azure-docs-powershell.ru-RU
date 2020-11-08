---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsvolume
schema: 2.0.0
ms.openlocfilehash: a423470454e77c58a8b611a47c737e5d86bfd1cf
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075304"
---
# <span data-ttu-id="60120-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="60120-101">Get-AzsVolume</span></span>

## <span data-ttu-id="60120-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60120-102">SYNOPSIS</span></span>
<span data-ttu-id="60120-103">Возврат запрошенного объема хранилища.</span><span class="sxs-lookup"><span data-stu-id="60120-103">Return the requested a storage volume.</span></span>

## <span data-ttu-id="60120-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60120-104">SYNTAX</span></span>

### <span data-ttu-id="60120-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60120-105">List (Default)</span></span>
```
Get-AzsVolume -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="60120-106">Получить</span><span class="sxs-lookup"><span data-stu-id="60120-106">Get</span></span>
```
Get-AzsVolume -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="60120-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="60120-107">GetViaIdentity</span></span>
```
Get-AzsVolume -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="60120-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60120-108">DESCRIPTION</span></span>
<span data-ttu-id="60120-109">Возврат запрошенного объема хранилища.</span><span class="sxs-lookup"><span data-stu-id="60120-109">Return the requested a storage volume.</span></span>

## <span data-ttu-id="60120-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60120-110">EXAMPLES</span></span>

### <span data-ttu-id="60120-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="60120-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="60120-112">Получение списка всех томов хранилища в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="60120-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="60120-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="60120-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name ee594cf5-cf54-46b4-a641-139553307195
```

<span data-ttu-id="60120-114">Получение тома хранилища по имени в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="60120-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="60120-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60120-115">PARAMETERS</span></span>

### <span data-ttu-id="60120-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60120-116">-DefaultProfile</span></span>
<span data-ttu-id="60120-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60120-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60120-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="60120-118">-Filter</span></span>
<span data-ttu-id="60120-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="60120-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="60120-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60120-120">-InputObject</span></span>
<span data-ttu-id="60120-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="60120-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="60120-122">-Location</span><span class="sxs-lookup"><span data-stu-id="60120-122">-Location</span></span>
<span data-ttu-id="60120-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="60120-123">Location of the resource.</span></span>

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

### <span data-ttu-id="60120-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="60120-124">-Name</span></span>
<span data-ttu-id="60120-125">Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="60120-125">Name of the storage volume.</span></span>

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

### <span data-ttu-id="60120-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60120-126">-PassThru</span></span>
<span data-ttu-id="60120-127">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="60120-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="60120-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60120-128">-ResourceGroupName</span></span>
<span data-ttu-id="60120-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60120-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="60120-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="60120-130">-ScaleUnit</span></span>
<span data-ttu-id="60120-131">Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="60120-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="60120-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="60120-132">-Skip</span></span>
<span data-ttu-id="60120-133">Параметр пропуска OData.</span><span class="sxs-lookup"><span data-stu-id="60120-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="60120-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="60120-134">-StorageSubSystem</span></span>
<span data-ttu-id="60120-135">Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="60120-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="60120-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60120-136">-SubscriptionId</span></span>
<span data-ttu-id="60120-137">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="60120-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="60120-138">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="60120-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="60120-139">-Top</span><span class="sxs-lookup"><span data-stu-id="60120-139">-Top</span></span>
<span data-ttu-id="60120-140">Параметр TOP для OData.</span><span class="sxs-lookup"><span data-stu-id="60120-140">OData top parameter.</span></span>

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

### <span data-ttu-id="60120-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60120-141">CommonParameters</span></span>
<span data-ttu-id="60120-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60120-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60120-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60120-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60120-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60120-144">INPUTS</span></span>

### <span data-ttu-id="60120-145">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="60120-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="60120-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60120-146">OUTPUTS</span></span>

### <span data-ttu-id="60120-147">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20190501. IVolume</span><span class="sxs-lookup"><span data-stu-id="60120-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IVolume</span></span>



## <span data-ttu-id="60120-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="60120-148">NOTES</span></span>

<span data-ttu-id="60120-149">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="60120-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60120-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60120-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="60120-151">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="60120-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60120-152">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="60120-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="60120-153">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="60120-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="60120-154">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="60120-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="60120-155">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="60120-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="60120-156">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="60120-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="60120-157">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="60120-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="60120-158">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="60120-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60120-159">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="60120-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="60120-160">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="60120-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="60120-161">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="60120-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="60120-162">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="60120-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="60120-163">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="60120-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="60120-164">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="60120-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="60120-165">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="60120-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="60120-166">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60120-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="60120-167">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="60120-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="60120-168">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="60120-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="60120-169">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="60120-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="60120-170">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="60120-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="60120-171">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="60120-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="60120-172">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="60120-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="60120-173">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="60120-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="60120-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60120-174">RELATED LINKS</span></span>

