---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077147"
---
# <span data-ttu-id="f7f28-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="f7f28-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="f7f28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7f28-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f28-103">Восстанавливает узел кластера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="f7f28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7f28-104">SYNTAX</span></span>

### <span data-ttu-id="f7f28-105">RepairExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7f28-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f7f28-106">Чинит</span><span class="sxs-lookup"><span data-stu-id="f7f28-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f7f28-107">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f7f28-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f7f28-108">RepairViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f7f28-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7f28-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7f28-109">DESCRIPTION</span></span>
<span data-ttu-id="f7f28-110">Восстанавливает узел кластера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="f7f28-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7f28-111">EXAMPLES</span></span>

### <span data-ttu-id="f7f28-112">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="f7f28-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="f7f28-113">Восстановите узел масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="f7f28-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="f7f28-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7f28-114">PARAMETERS</span></span>

### <span data-ttu-id="f7f28-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7f28-115">-AsJob</span></span>
<span data-ttu-id="f7f28-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f7f28-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f7f28-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="f7f28-117">-BareMetalNode</span></span>
<span data-ttu-id="f7f28-118">Описание одноэлементного металла, используемого для операции увеличения на кластере.</span><span class="sxs-lookup"><span data-stu-id="f7f28-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="f7f28-119">Для конструирования ознакомьтесь с разделом "Заметки" для свойств BAREMETALNODE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="f7f28-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription
Parameter Sets: Repair, RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-120">-BiosVersion</span><span class="sxs-lookup"><span data-stu-id="f7f28-120">-BiosVersion</span></span>
<span data-ttu-id="f7f28-121">Версия BIOS физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-121">Bios version of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="f7f28-122">-BmciPv4Address</span></span>
<span data-ttu-id="f7f28-123">BMC адрес физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-123">BMC address of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-124">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="f7f28-124">-ClusterName</span></span>
<span data-ttu-id="f7f28-125">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-125">Name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="f7f28-126">-ComputerName</span></span>
<span data-ttu-id="f7f28-127">Имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-127">Name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f28-128">-DefaultProfile</span></span>
<span data-ttu-id="f7f28-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f28-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7f28-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f7f28-130">-Force</span></span>
<span data-ttu-id="f7f28-131">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f7f28-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f7f28-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7f28-132">-InputObject</span></span>
<span data-ttu-id="f7f28-133">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="f7f28-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RepairViaIdentity, RepairViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-134">-Location</span><span class="sxs-lookup"><span data-stu-id="f7f28-134">-Location</span></span>
<span data-ttu-id="f7f28-135">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7f28-135">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-136">-MacAddress</span><span class="sxs-lookup"><span data-stu-id="f7f28-136">-MacAddress</span></span>
<span data-ttu-id="f7f28-137">Имя MAC-адреса узла исходного металла.</span><span class="sxs-lookup"><span data-stu-id="f7f28-137">Name of the MAC address of the bare metal node.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-138">-Model</span><span class="sxs-lookup"><span data-stu-id="f7f28-138">-Model</span></span>
<span data-ttu-id="f7f28-139">Модель физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-139">Model of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7f28-140">-Name</span></span>
<span data-ttu-id="f7f28-141">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f7f28-141">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-142">-Wait</span><span class="sxs-lookup"><span data-stu-id="f7f28-142">-NoWait</span></span>
<span data-ttu-id="f7f28-143">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="f7f28-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f7f28-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7f28-144">-PassThru</span></span>
<span data-ttu-id="f7f28-145">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f7f28-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f7f28-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f28-146">-ResourceGroupName</span></span>
<span data-ttu-id="f7f28-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7f28-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-148">-SerialNumber</span><span class="sxs-lookup"><span data-stu-id="f7f28-148">-SerialNumber</span></span>
<span data-ttu-id="f7f28-149">Серийный номер физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-149">Serial number of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7f28-150">-SubscriptionId</span></span>
<span data-ttu-id="f7f28-151">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f28-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f7f28-152">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="f7f28-152">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-153">-Vendor</span><span class="sxs-lookup"><span data-stu-id="f7f28-153">-Vendor</span></span>
<span data-ttu-id="f7f28-154">Поставщик физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-154">Vendor of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7f28-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7f28-155">-Confirm</span></span>
<span data-ttu-id="f7f28-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7f28-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f28-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f28-157">-WhatIf</span></span>
<span data-ttu-id="f7f28-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7f28-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7f28-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7f28-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f28-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f28-160">CommonParameters</span></span>
<span data-ttu-id="f7f28-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7f28-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f28-162">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7f28-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f28-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7f28-163">INPUTS</span></span>

### <span data-ttu-id="f7f28-164">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IBareMetalNodeDescription</span><span class="sxs-lookup"><span data-stu-id="f7f28-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="f7f28-165">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f7f28-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="f7f28-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7f28-166">OUTPUTS</span></span>

### <span data-ttu-id="f7f28-167">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7f28-167">System.Boolean</span></span>



## <span data-ttu-id="f7f28-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7f28-168">NOTES</span></span>

<span data-ttu-id="f7f28-169">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f7f28-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7f28-170">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7f28-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f7f28-171">BAREMETALNODE <IBareMetalNodeDescription> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="f7f28-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="f7f28-172">`[BiosVersion <String>]`: Версия BIOS физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="f7f28-173">`[BmciPv4Address <String>]`: BMC адрес физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="f7f28-174">`[ClusterName <String>]`: Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="f7f28-175">`[ComputerName <String>]`: Имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="f7f28-176">`[MacAddress <String>]`: Имя MAC-адреса узла исходного металла.</span><span class="sxs-lookup"><span data-stu-id="f7f28-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="f7f28-177">`[Model <String>]`: Модель физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="f7f28-178">`[SerialNumber <String>]`: Серийный номер физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="f7f28-179">`[Vendor <String>]`: Поставщик физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7f28-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="f7f28-180">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="f7f28-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f7f28-181">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="f7f28-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="f7f28-182">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="f7f28-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="f7f28-183">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="f7f28-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="f7f28-184">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="f7f28-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="f7f28-185">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="f7f28-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="f7f28-186">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="f7f28-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="f7f28-187">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="f7f28-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f7f28-188">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="f7f28-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="f7f28-189">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="f7f28-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="f7f28-190">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7f28-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="f7f28-191">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="f7f28-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="f7f28-192">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="f7f28-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="f7f28-193">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="f7f28-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="f7f28-194">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="f7f28-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="f7f28-195">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7f28-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f7f28-196">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="f7f28-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="f7f28-197">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f7f28-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="f7f28-198">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="f7f28-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="f7f28-199">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="f7f28-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="f7f28-200">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="f7f28-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="f7f28-201">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f28-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f7f28-202">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="f7f28-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f7f28-203">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="f7f28-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="f7f28-204">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7f28-204">RELATED LINKS</span></span>

