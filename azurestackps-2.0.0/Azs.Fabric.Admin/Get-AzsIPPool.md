---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910533"
---
# <span data-ttu-id="e3987-101">Get-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="e3987-101">Get-AzsIPPool</span></span>

## <span data-ttu-id="e3987-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3987-102">SYNOPSIS</span></span>
<span data-ttu-id="e3987-103">Возврат запрашиваемого пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="e3987-103">Return the requested IP pool.</span></span>

## <span data-ttu-id="e3987-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3987-104">SYNTAX</span></span>

### <span data-ttu-id="e3987-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3987-105">List (Default)</span></span>
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e3987-106">Получить</span><span class="sxs-lookup"><span data-stu-id="e3987-106">Get</span></span>
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e3987-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3987-107">GetViaIdentity</span></span>
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="e3987-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3987-108">DESCRIPTION</span></span>
<span data-ttu-id="e3987-109">Возврат запрашиваемого пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="e3987-109">Return the requested IP pool.</span></span>

## <span data-ttu-id="e3987-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3987-110">EXAMPLES</span></span>

### <span data-ttu-id="e3987-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="e3987-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

<span data-ttu-id="e3987-112">Получение всех пулов IP-адресов инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="e3987-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="e3987-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="e3987-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

<span data-ttu-id="e3987-114">Получение пула IP-адресов инфраструктуры на основе имени.</span><span class="sxs-lookup"><span data-stu-id="e3987-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="e3987-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3987-115">PARAMETERS</span></span>

### <span data-ttu-id="e3987-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3987-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="e3987-117">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="e3987-117">-Filter</span></span>
<span data-ttu-id="e3987-118">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="e3987-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="e3987-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3987-119">-InputObject</span></span>
<span data-ttu-id="e3987-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e3987-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e3987-121">-Location</span><span class="sxs-lookup"><span data-stu-id="e3987-121">-Location</span></span>
<span data-ttu-id="e3987-122">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="e3987-122">Location of the resource.</span></span>

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

### <span data-ttu-id="e3987-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3987-123">-Name</span></span>
<span data-ttu-id="e3987-124">Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="e3987-124">IP pool name.</span></span>

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

### <span data-ttu-id="e3987-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3987-125">-PassThru</span></span>
<span data-ttu-id="e3987-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e3987-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e3987-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3987-127">-ResourceGroupName</span></span>
<span data-ttu-id="e3987-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3987-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="e3987-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3987-129">-SubscriptionId</span></span>
<span data-ttu-id="e3987-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e3987-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e3987-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e3987-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e3987-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3987-132">CommonParameters</span></span>
<span data-ttu-id="e3987-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3987-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3987-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3987-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3987-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3987-135">INPUTS</span></span>

### <span data-ttu-id="e3987-136">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e3987-136">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="e3987-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3987-137">OUTPUTS</span></span>

### <span data-ttu-id="e3987-138">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="e3987-138">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="e3987-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3987-139">NOTES</span></span>

<span data-ttu-id="e3987-140">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e3987-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3987-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3987-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e3987-142">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e3987-142">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3987-143">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="e3987-143">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="e3987-144">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="e3987-144">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="e3987-145">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="e3987-145">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="e3987-146">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="e3987-146">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="e3987-147">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="e3987-147">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="e3987-148">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="e3987-148">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="e3987-149">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e3987-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3987-150">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="e3987-150">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="e3987-151">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="e3987-151">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="e3987-152">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="e3987-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e3987-153">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="e3987-153">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="e3987-154">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="e3987-154">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="e3987-155">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="e3987-155">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="e3987-156">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="e3987-156">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="e3987-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3987-157">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e3987-158">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="e3987-158">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="e3987-159">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="e3987-159">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="e3987-160">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="e3987-160">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="e3987-161">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="e3987-161">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="e3987-162">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="e3987-162">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="e3987-163">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e3987-163">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e3987-164">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e3987-164">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e3987-165">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="e3987-165">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="e3987-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3987-166">RELATED LINKS</span></span>

