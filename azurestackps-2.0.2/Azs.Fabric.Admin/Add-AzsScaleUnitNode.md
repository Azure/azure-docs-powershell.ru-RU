---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: fe7726c25ee9dd83ca940b4ac6e47b3cc26a6457
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076713"
---
# <span data-ttu-id="74037-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="74037-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="74037-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74037-102">SYNOPSIS</span></span>
<span data-ttu-id="74037-103">Масштабирование единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="74037-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="74037-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74037-104">SYNTAX</span></span>

### <span data-ttu-id="74037-105">ScaleExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74037-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-BmciPv4Address <String>] [-ComputerName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74037-106">Штаб</span><span class="sxs-lookup"><span data-stu-id="74037-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74037-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="74037-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74037-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="74037-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-BmciPv4Address <String>] [-ComputerName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74037-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74037-109">DESCRIPTION</span></span>
<span data-ttu-id="74037-110">Масштабирование единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="74037-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="74037-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74037-111">EXAMPLES</span></span>

### <span data-ttu-id="74037-112">Пример 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="74037-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -BmciPv4Address $BmciPv4Address -ComputerName $ComputerName -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="74037-113">Добавьте новый узел шкалы масштабирования в кластер единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="74037-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="74037-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74037-114">PARAMETERS</span></span>

### <span data-ttu-id="74037-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74037-115">-AsJob</span></span>
<span data-ttu-id="74037-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="74037-116">Run the command as a job</span></span>

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

### <span data-ttu-id="74037-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="74037-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="74037-118">Флаг указывает, должна ли операция ждать, пока хранилище не будет получено, прежде чем возвращать его.</span><span class="sxs-lookup"><span data-stu-id="74037-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="74037-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74037-119">-DefaultProfile</span></span>
<span data-ttu-id="74037-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74037-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74037-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74037-121">-InputObject</span></span>
<span data-ttu-id="74037-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="74037-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="74037-123">-Location</span><span class="sxs-lookup"><span data-stu-id="74037-123">-Location</span></span>
<span data-ttu-id="74037-124">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="74037-124">Location of the resource.</span></span>

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

### <span data-ttu-id="74037-125">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="74037-125">-BmciPv4Address</span></span> 
<span data-ttu-id="74037-126">BMC адрес физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="74037-126">BMC address of the physical machine.</span></span>

### <span data-ttu-id="74037-127">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="74037-127">-ComputerName</span></span> 
<span data-ttu-id="74037-128">Имя компьютера физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="74037-128">Computer name of the physical machine.</span></span>

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

### <span data-ttu-id="74037-129">-Wait</span><span class="sxs-lookup"><span data-stu-id="74037-129">-NoWait</span></span>
<span data-ttu-id="74037-130">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="74037-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="74037-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74037-131">-PassThru</span></span>
<span data-ttu-id="74037-132">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="74037-132">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="74037-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74037-133">-ResourceGroupName</span></span>
<span data-ttu-id="74037-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74037-134">Name of the resource group.</span></span>

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

### <span data-ttu-id="74037-135">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="74037-135">-ScaleUnit</span></span>
<span data-ttu-id="74037-136">Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="74037-136">Name of the scale units.</span></span>

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

### <span data-ttu-id="74037-137">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="74037-137">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="74037-138">Список входных данных, с помощью которых можно добавить набор узлов единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="74037-138">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="74037-139">Для конструирования ознакомьтесь с разделом "Заметки" для свойств SCALEUNITNODEPARAMETER и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="74037-139">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="74037-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74037-140">-SubscriptionId</span></span>
<span data-ttu-id="74037-141">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="74037-141">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="74037-142">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="74037-142">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="74037-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74037-143">-Confirm</span></span>
<span data-ttu-id="74037-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74037-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74037-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74037-145">-WhatIf</span></span>
<span data-ttu-id="74037-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74037-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74037-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74037-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74037-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74037-148">CommonParameters</span></span>
<span data-ttu-id="74037-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74037-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74037-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74037-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74037-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74037-151">INPUTS</span></span>

### <span data-ttu-id="74037-152">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="74037-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="74037-153">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="74037-153">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="74037-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74037-154">OUTPUTS</span></span>

### <span data-ttu-id="74037-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74037-155">System.Boolean</span></span>

## <span data-ttu-id="74037-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="74037-156">NOTES</span></span>

<span data-ttu-id="74037-157">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="74037-157">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74037-158">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74037-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="74037-159">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="74037-159">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74037-160">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="74037-160">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="74037-161">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="74037-161">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="74037-162">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="74037-162">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="74037-163">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="74037-163">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="74037-164">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="74037-164">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="74037-165">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="74037-165">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="74037-166">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="74037-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74037-167">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="74037-167">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="74037-168">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="74037-168">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="74037-169">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="74037-169">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="74037-170">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="74037-170">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="74037-171">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="74037-171">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="74037-172">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="74037-172">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="74037-173">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="74037-173">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="74037-174">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74037-174">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="74037-175">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="74037-175">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="74037-176">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="74037-176">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="74037-177">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="74037-177">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="74037-178">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="74037-178">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="74037-179">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="74037-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="74037-180">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="74037-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="74037-181">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="74037-181">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="74037-182">NODELIST <IScaleOutScaleUnitParameters [] >: список узлов в единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="74037-182">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="74037-183">`[BmciPv4Address <String>]`: BMC адрес физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="74037-183">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="74037-184">`[ComputerName <String>]`: Имя компьютера для физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="74037-184">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="74037-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : список входных данных, с помощью которых можно добавить набор узлов единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="74037-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="74037-186">`[AwaitStorageConvergence <Boolean?>]`: Флаг указывает, должна ли операция ждать, пока хранилище не будет получено, прежде чем возвращать.</span><span class="sxs-lookup"><span data-stu-id="74037-186">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="74037-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Список узлов в единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="74037-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="74037-188">`[BmciPv4Address <String>]`: BMC адрес физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="74037-188">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="74037-189">`[ComputerName <String>]`: Имя компьютера для физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="74037-189">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="74037-190">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74037-190">RELATED LINKS</span></span>
