---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 5762cbd1c972f5500a15be8fea8595165add3afc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911644"
---
# <span data-ttu-id="92054-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="92054-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="92054-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92054-102">SYNOPSIS</span></span>
<span data-ttu-id="92054-103">Перезагрузите экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="92054-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="92054-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92054-104">SYNTAX</span></span>

### <span data-ttu-id="92054-105">Перезагрузка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92054-105">Reboot (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="92054-106">RebootViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92054-106">RebootViaIdentity</span></span>
```
Restart-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92054-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92054-107">DESCRIPTION</span></span>
<span data-ttu-id="92054-108">Перезагрузите экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="92054-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="92054-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92054-109">EXAMPLES</span></span>

### <span data-ttu-id="92054-110">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="92054-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="92054-111">Перезагрузите экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="92054-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="92054-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92054-112">PARAMETERS</span></span>

### <span data-ttu-id="92054-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92054-113">-AsJob</span></span>
<span data-ttu-id="92054-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="92054-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="92054-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92054-115">-DefaultProfile</span></span>
<span data-ttu-id="92054-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92054-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="92054-117">-Force</span><span class="sxs-lookup"><span data-stu-id="92054-117">-Force</span></span>
<span data-ttu-id="92054-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="92054-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="92054-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92054-119">-InputObject</span></span>
<span data-ttu-id="92054-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="92054-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RebootViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="92054-121">-Location</span><span class="sxs-lookup"><span data-stu-id="92054-121">-Location</span></span>
<span data-ttu-id="92054-122">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="92054-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92054-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92054-123">-Name</span></span>
<span data-ttu-id="92054-124">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="92054-124">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92054-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="92054-125">-NoWait</span></span>
<span data-ttu-id="92054-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="92054-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="92054-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92054-127">-PassThru</span></span>
<span data-ttu-id="92054-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="92054-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="92054-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92054-129">-ResourceGroupName</span></span>
<span data-ttu-id="92054-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92054-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```
### <span data-ttu-id="92054-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92054-131">-SubscriptionId</span></span>
<span data-ttu-id="92054-132">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="92054-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="92054-133">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="92054-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92054-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92054-134">-Confirm</span></span>
<span data-ttu-id="92054-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92054-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92054-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92054-136">-WhatIf</span></span>
<span data-ttu-id="92054-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="92054-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92054-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="92054-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92054-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92054-139">CommonParameters</span></span>
<span data-ttu-id="92054-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92054-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92054-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92054-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92054-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92054-142">INPUTS</span></span>

### <span data-ttu-id="92054-143">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="92054-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="92054-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92054-144">OUTPUTS</span></span>

### <span data-ttu-id="92054-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92054-145">System.Boolean</span></span>



## <span data-ttu-id="92054-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="92054-146">NOTES</span></span>

<span data-ttu-id="92054-147">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="92054-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92054-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92054-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="92054-149">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="92054-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92054-150">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="92054-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="92054-151">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="92054-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="92054-152">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="92054-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="92054-153">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="92054-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="92054-154">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="92054-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="92054-155">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="92054-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="92054-156">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="92054-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92054-157">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="92054-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="92054-158">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="92054-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="92054-159">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="92054-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="92054-160">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="92054-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="92054-161">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="92054-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="92054-162">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="92054-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="92054-163">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="92054-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="92054-164">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92054-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="92054-165">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="92054-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="92054-166">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="92054-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="92054-167">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="92054-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="92054-168">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="92054-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="92054-169">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="92054-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="92054-170">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="92054-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="92054-171">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="92054-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="92054-172">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="92054-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="92054-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92054-173">RELATED LINKS</span></span>

