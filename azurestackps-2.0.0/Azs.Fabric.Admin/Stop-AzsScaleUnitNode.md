---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911617"
---
# <span data-ttu-id="9bd1d-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9bd1d-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="9bd1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bd1d-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd1d-103">Включите или выключите узел шкалной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="9bd1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bd1d-104">SYNTAX</span></span>

### <span data-ttu-id="9bd1d-105">PowerOff (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9bd1d-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9bd1d-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9bd1d-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9bd1d-107">Остановлен</span><span class="sxs-lookup"><span data-stu-id="9bd1d-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9bd1d-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9bd1d-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9bd1d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bd1d-109">DESCRIPTION</span></span>
<span data-ttu-id="9bd1d-110">Включите или выключите узел шкалной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="9bd1d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bd1d-111">EXAMPLES</span></span>

### <span data-ttu-id="9bd1d-112">Пример 1: {{добавьте заголовок}}</span><span class="sxs-lookup"><span data-stu-id="9bd1d-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="9bd1d-113">Выключите экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="9bd1d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bd1d-114">PARAMETERS</span></span>

### <span data-ttu-id="9bd1d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bd1d-115">-AsJob</span></span>
<span data-ttu-id="9bd1d-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9bd1d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9bd1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd1d-117">-DefaultProfile</span></span>
<span data-ttu-id="9bd1d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd1d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9bd1d-119">-Force</span></span>
<span data-ttu-id="9bd1d-120">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9bd1d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bd1d-121">-InputObject</span></span>
<span data-ttu-id="9bd1d-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity, ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9bd1d-123">-Location</span><span class="sxs-lookup"><span data-stu-id="9bd1d-123">-Location</span></span>
<span data-ttu-id="9bd1d-124">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9bd1d-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9bd1d-125">-Name</span></span>
<span data-ttu-id="9bd1d-126">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-126">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9bd1d-127">-Wait</span><span class="sxs-lookup"><span data-stu-id="9bd1d-127">-NoWait</span></span>
<span data-ttu-id="9bd1d-128">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="9bd1d-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9bd1d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bd1d-129">-PassThru</span></span>
<span data-ttu-id="9bd1d-130">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9bd1d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd1d-131">-ResourceGroupName</span></span>
<span data-ttu-id="9bd1d-132">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-132">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9bd1d-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9bd1d-133">-SubscriptionId</span></span>
<span data-ttu-id="9bd1d-134">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9bd1d-135">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9bd1d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bd1d-136">-Confirm</span></span>
<span data-ttu-id="9bd1d-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd1d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd1d-138">-WhatIf</span></span>
<span data-ttu-id="9bd1d-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bd1d-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bd1d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd1d-141">CommonParameters</span></span>
<span data-ttu-id="9bd1d-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd1d-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bd1d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd1d-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bd1d-144">INPUTS</span></span>

### <span data-ttu-id="9bd1d-145">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9bd1d-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="9bd1d-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bd1d-146">OUTPUTS</span></span>

### <span data-ttu-id="9bd1d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bd1d-147">System.Boolean</span></span>



## <span data-ttu-id="9bd1d-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bd1d-148">NOTES</span></span>

<span data-ttu-id="9bd1d-149">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9bd1d-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9bd1d-151">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="9bd1d-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9bd1d-152">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="9bd1d-153">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="9bd1d-154">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="9bd1d-155">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="9bd1d-156">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="9bd1d-157">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="9bd1d-158">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="9bd1d-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9bd1d-159">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="9bd1d-160">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="9bd1d-161">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9bd1d-162">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="9bd1d-163">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="9bd1d-164">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="9bd1d-165">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="9bd1d-166">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9bd1d-167">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="9bd1d-168">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="9bd1d-169">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="9bd1d-170">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="9bd1d-171">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="9bd1d-172">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9bd1d-173">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9bd1d-174">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="9bd1d-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="9bd1d-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bd1d-175">RELATED LINKS</span></span>

