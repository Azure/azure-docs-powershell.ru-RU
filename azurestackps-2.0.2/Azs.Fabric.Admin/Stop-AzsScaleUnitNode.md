---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 3f5adef6382038fdaf8c17620508b4a450ff74bc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076809"
---
# <span data-ttu-id="784e9-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="784e9-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="784e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="784e9-102">SYNOPSIS</span></span>
<span data-ttu-id="784e9-103">Включите или выключите узел шкалной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="784e9-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="784e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="784e9-104">SYNTAX</span></span>

### <span data-ttu-id="784e9-105">PowerOff (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="784e9-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="784e9-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="784e9-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="784e9-107">Остановлен</span><span class="sxs-lookup"><span data-stu-id="784e9-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="784e9-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="784e9-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="784e9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="784e9-109">DESCRIPTION</span></span>
<span data-ttu-id="784e9-110">Включите или выключите узел шкалной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="784e9-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="784e9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="784e9-111">EXAMPLES</span></span>

### <span data-ttu-id="784e9-112">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="784e9-112">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="784e9-113">Включите или выключите узел масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="784e9-113">Power down a scale unit node.</span></span>

### <span data-ttu-id="784e9-114">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="784e9-114">Example 2:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="784e9-115">Включите или выключите узел масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="784e9-115">Power down a scale unit node.</span></span> <span data-ttu-id="784e9-116">Как задание.</span><span class="sxs-lookup"><span data-stu-id="784e9-116">As a job.</span></span>

## <span data-ttu-id="784e9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="784e9-117">PARAMETERS</span></span>

### <span data-ttu-id="784e9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="784e9-118">-AsJob</span></span>
<span data-ttu-id="784e9-119">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="784e9-119">Run the command as a job</span></span>

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

### <span data-ttu-id="784e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="784e9-120">-DefaultProfile</span></span>
<span data-ttu-id="784e9-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="784e9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="784e9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="784e9-122">-Force</span></span>
<span data-ttu-id="784e9-123">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="784e9-123">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="784e9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="784e9-124">-InputObject</span></span>
<span data-ttu-id="784e9-125">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="784e9-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="784e9-126">-Location</span><span class="sxs-lookup"><span data-stu-id="784e9-126">-Location</span></span>
<span data-ttu-id="784e9-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="784e9-127">Location of the resource.</span></span>

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

### <span data-ttu-id="784e9-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="784e9-128">-Name</span></span>
<span data-ttu-id="784e9-129">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="784e9-129">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="784e9-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="784e9-130">-NoWait</span></span>
<span data-ttu-id="784e9-131">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="784e9-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="784e9-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="784e9-132">-PassThru</span></span>
<span data-ttu-id="784e9-133">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="784e9-133">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="784e9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="784e9-134">-ResourceGroupName</span></span>
<span data-ttu-id="784e9-135">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="784e9-135">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="784e9-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="784e9-136">-SubscriptionId</span></span>
<span data-ttu-id="784e9-137">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="784e9-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="784e9-138">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="784e9-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="784e9-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="784e9-139">-Confirm</span></span>
<span data-ttu-id="784e9-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="784e9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="784e9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="784e9-141">-WhatIf</span></span>
<span data-ttu-id="784e9-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="784e9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="784e9-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="784e9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="784e9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784e9-144">CommonParameters</span></span>
<span data-ttu-id="784e9-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="784e9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784e9-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="784e9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784e9-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="784e9-147">INPUTS</span></span>

### <span data-ttu-id="784e9-148">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="784e9-148">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="784e9-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="784e9-149">OUTPUTS</span></span>

### <span data-ttu-id="784e9-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="784e9-150">System.Boolean</span></span>

## <span data-ttu-id="784e9-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="784e9-151">NOTES</span></span>

<span data-ttu-id="784e9-152">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="784e9-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="784e9-153">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="784e9-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="784e9-154">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="784e9-154">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="784e9-155">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="784e9-155">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="784e9-156">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="784e9-156">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="784e9-157">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="784e9-157">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="784e9-158">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="784e9-158">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="784e9-159">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="784e9-159">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="784e9-160">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="784e9-160">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="784e9-161">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="784e9-161">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="784e9-162">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="784e9-162">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="784e9-163">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="784e9-163">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="784e9-164">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="784e9-164">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="784e9-165">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="784e9-165">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="784e9-166">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="784e9-166">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="784e9-167">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="784e9-167">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="784e9-168">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="784e9-168">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="784e9-169">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="784e9-169">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="784e9-170">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="784e9-170">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="784e9-171">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="784e9-171">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="784e9-172">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="784e9-172">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="784e9-173">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="784e9-173">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="784e9-174">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="784e9-174">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="784e9-175">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="784e9-175">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="784e9-176">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="784e9-176">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="784e9-177">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="784e9-177">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="784e9-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="784e9-178">RELATED LINKS</span></span>
