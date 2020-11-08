---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075379"
---
# <span data-ttu-id="25008-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="25008-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="25008-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25008-102">SYNOPSIS</span></span>
<span data-ttu-id="25008-103">Масштабирование единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="25008-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="25008-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25008-104">SYNTAX</span></span>

### <span data-ttu-id="25008-105">ScaleExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25008-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25008-106">Штаб</span><span class="sxs-lookup"><span data-stu-id="25008-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25008-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25008-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25008-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="25008-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25008-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25008-109">DESCRIPTION</span></span>
<span data-ttu-id="25008-110">Масштабирование единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="25008-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="25008-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25008-111">EXAMPLES</span></span>

### <span data-ttu-id="25008-112">Пример 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="25008-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="25008-113">Добавьте новый узел шкалы масштабирования в кластер единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="25008-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="25008-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25008-114">PARAMETERS</span></span>

### <span data-ttu-id="25008-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25008-115">-AsJob</span></span>
<span data-ttu-id="25008-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="25008-116">Run the command as a job</span></span>

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

### <span data-ttu-id="25008-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="25008-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="25008-118">Флаг указывает, должна ли операция ждать, пока хранилище не будет получено, прежде чем возвращать его.</span><span class="sxs-lookup"><span data-stu-id="25008-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25008-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25008-119">-DefaultProfile</span></span>
<span data-ttu-id="25008-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25008-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25008-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25008-121">-InputObject</span></span>
<span data-ttu-id="25008-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="25008-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="25008-123">-Location</span><span class="sxs-lookup"><span data-stu-id="25008-123">-Location</span></span>
<span data-ttu-id="25008-124">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="25008-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25008-125">-NodeList</span><span class="sxs-lookup"><span data-stu-id="25008-125">-NodeList</span></span>
<span data-ttu-id="25008-126">Список узлов в единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="25008-126">List of nodes in the scale unit.</span></span>
<span data-ttu-id="25008-127">Для конструирования ознакомьтесь с разделом "Заметки" для свойств NODELIST и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="25008-127">To construct, see NOTES section for NODELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25008-128">-Wait</span><span class="sxs-lookup"><span data-stu-id="25008-128">-NoWait</span></span>
<span data-ttu-id="25008-129">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="25008-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="25008-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25008-130">-PassThru</span></span>
<span data-ttu-id="25008-131">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="25008-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="25008-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25008-132">-ResourceGroupName</span></span>
<span data-ttu-id="25008-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25008-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25008-134">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="25008-134">-ScaleUnit</span></span>
<span data-ttu-id="25008-135">Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="25008-135">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25008-136">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="25008-136">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="25008-137">Список входных данных, с помощью которых можно добавить набор узлов единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="25008-137">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="25008-138">Для конструирования ознакомьтесь с разделом "Заметки" для свойств SCALEUNITNODEPARAMETER и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="25008-138">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="25008-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25008-139">-SubscriptionId</span></span>
<span data-ttu-id="25008-140">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25008-140">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="25008-141">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="25008-141">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25008-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25008-142">-Confirm</span></span>
<span data-ttu-id="25008-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25008-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25008-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25008-144">-WhatIf</span></span>
<span data-ttu-id="25008-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25008-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25008-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25008-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25008-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25008-147">CommonParameters</span></span>
<span data-ttu-id="25008-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25008-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25008-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25008-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25008-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25008-150">INPUTS</span></span>

### <span data-ttu-id="25008-151">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="25008-151">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="25008-152">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="25008-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="25008-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25008-153">OUTPUTS</span></span>

### <span data-ttu-id="25008-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25008-154">System.Boolean</span></span>



## <span data-ttu-id="25008-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="25008-155">NOTES</span></span>

<span data-ttu-id="25008-156">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="25008-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25008-157">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25008-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="25008-158">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="25008-158">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25008-159">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="25008-159">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="25008-160">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="25008-160">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="25008-161">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="25008-161">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="25008-162">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="25008-162">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="25008-163">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="25008-163">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="25008-164">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="25008-164">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="25008-165">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="25008-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25008-166">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="25008-166">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="25008-167">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="25008-167">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="25008-168">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="25008-168">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="25008-169">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="25008-169">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="25008-170">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="25008-170">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="25008-171">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="25008-171">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="25008-172">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="25008-172">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="25008-173">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25008-173">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="25008-174">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="25008-174">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="25008-175">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="25008-175">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="25008-176">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="25008-176">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="25008-177">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="25008-177">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="25008-178">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25008-178">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="25008-179">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="25008-179">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="25008-180">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="25008-180">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="25008-181">NODELIST <IScaleOutScaleUnitParameters [] >: список узлов в единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="25008-181">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="25008-182">`[BmciPv4Address <String>]`: BMC адрес физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="25008-182">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="25008-183">`[ComputerName <String>]`: Имя компьютера для физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="25008-183">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="25008-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : список входных данных, с помощью которых можно добавить набор узлов единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="25008-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="25008-185">`[AwaitStorageConvergence <Boolean?>]`: Флаг указывает, должна ли операция ждать, пока хранилище не будет получено, прежде чем возвращать.</span><span class="sxs-lookup"><span data-stu-id="25008-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="25008-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Список узлов в единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="25008-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="25008-187">`[BmciPv4Address <String>]`: BMC адрес физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="25008-187">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="25008-188">`[ComputerName <String>]`: Имя компьютера для физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="25008-188">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="25008-189">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25008-189">RELATED LINKS</span></span>

