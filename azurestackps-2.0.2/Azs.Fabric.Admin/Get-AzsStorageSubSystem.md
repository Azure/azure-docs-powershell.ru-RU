---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076668"
---
# <span data-ttu-id="a7df7-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="a7df7-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="a7df7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7df7-102">SYNOPSIS</span></span>
<span data-ttu-id="a7df7-103">Возврат запрошенной подсистемы хранилища.</span><span class="sxs-lookup"><span data-stu-id="a7df7-103">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="a7df7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7df7-104">SYNTAX</span></span>

### <span data-ttu-id="a7df7-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7df7-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a7df7-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a7df7-106">Get</span></span>
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a7df7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a7df7-107">GetViaIdentity</span></span>
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="a7df7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7df7-108">DESCRIPTION</span></span>
<span data-ttu-id="a7df7-109">Возврат запрошенной подсистемы хранилища.</span><span class="sxs-lookup"><span data-stu-id="a7df7-109">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="a7df7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7df7-110">EXAMPLES</span></span>

### <span data-ttu-id="a7df7-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="a7df7-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

<span data-ttu-id="a7df7-112">Получение всех подсистем хранилища из единицы измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="a7df7-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="a7df7-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="a7df7-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

<span data-ttu-id="a7df7-114">Получение подсистемы хранилища с заданными единицей и именем шкалы.</span><span class="sxs-lookup"><span data-stu-id="a7df7-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="a7df7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7df7-115">PARAMETERS</span></span>

### <span data-ttu-id="a7df7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7df7-116">-DefaultProfile</span></span>
<span data-ttu-id="a7df7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7df7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7df7-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="a7df7-118">-Filter</span></span>
<span data-ttu-id="a7df7-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="a7df7-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="a7df7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7df7-120">-InputObject</span></span>
<span data-ttu-id="a7df7-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a7df7-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7df7-122">-Location</span><span class="sxs-lookup"><span data-stu-id="a7df7-122">-Location</span></span>
<span data-ttu-id="a7df7-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7df7-123">Location of the resource.</span></span>

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

### <span data-ttu-id="a7df7-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7df7-124">-Name</span></span>
<span data-ttu-id="a7df7-125">Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="a7df7-125">Name of the storage system.</span></span>

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

### <span data-ttu-id="a7df7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7df7-126">-PassThru</span></span>
<span data-ttu-id="a7df7-127">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a7df7-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a7df7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7df7-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7df7-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7df7-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="a7df7-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a7df7-130">-ScaleUnit</span></span>
<span data-ttu-id="a7df7-131">Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="a7df7-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="a7df7-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="a7df7-132">-Skip</span></span>
<span data-ttu-id="a7df7-133">Параметр пропуска OData.</span><span class="sxs-lookup"><span data-stu-id="a7df7-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="a7df7-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7df7-134">-SubscriptionId</span></span>
<span data-ttu-id="a7df7-135">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a7df7-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a7df7-136">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a7df7-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a7df7-137">-Top</span><span class="sxs-lookup"><span data-stu-id="a7df7-137">-Top</span></span>
<span data-ttu-id="a7df7-138">Параметр TOP для OData.</span><span class="sxs-lookup"><span data-stu-id="a7df7-138">OData top parameter.</span></span>

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

### <span data-ttu-id="a7df7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7df7-139">CommonParameters</span></span>
<span data-ttu-id="a7df7-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7df7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7df7-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7df7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7df7-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7df7-142">INPUTS</span></span>

### <span data-ttu-id="a7df7-143">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a7df7-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="a7df7-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7df7-144">OUTPUTS</span></span>

### <span data-ttu-id="a7df7-145">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20181001. IStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="a7df7-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20181001.IStorageSubSystem</span></span>



## <span data-ttu-id="a7df7-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7df7-146">NOTES</span></span>

<span data-ttu-id="a7df7-147">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a7df7-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7df7-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7df7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a7df7-149">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a7df7-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7df7-150">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="a7df7-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="a7df7-151">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="a7df7-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="a7df7-152">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="a7df7-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="a7df7-153">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="a7df7-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="a7df7-154">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="a7df7-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="a7df7-155">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="a7df7-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="a7df7-156">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="a7df7-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7df7-157">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="a7df7-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="a7df7-158">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="a7df7-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="a7df7-159">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7df7-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a7df7-160">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="a7df7-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="a7df7-161">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="a7df7-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="a7df7-162">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="a7df7-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="a7df7-163">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="a7df7-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="a7df7-164">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7df7-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a7df7-165">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="a7df7-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="a7df7-166">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="a7df7-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="a7df7-167">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="a7df7-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="a7df7-168">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="a7df7-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="a7df7-169">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a7df7-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a7df7-170">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a7df7-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a7df7-171">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="a7df7-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="a7df7-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7df7-172">RELATED LINKS</span></span>
