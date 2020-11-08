---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: d6bb118a6b7699672209618e1409fe6a9bed466d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075232"
---
# <span data-ttu-id="35940-101">Disable-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="35940-101">Disable-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="35940-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35940-102">SYNOPSIS</span></span>


## <span data-ttu-id="35940-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35940-103">SYNTAX</span></span>

### <span data-ttu-id="35940-104">Завершение работы (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35940-104">Shutdown (Default)</span></span>
```
Disable-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35940-105">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35940-105">ShutdownViaIdentity</span></span>
```
Disable-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35940-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35940-106">DESCRIPTION</span></span>
<span data-ttu-id="35940-107">Завершение работы с экземпляром роли инфраструктуры для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="35940-107">Shutdown an infrastructure role instance for maintenance.</span></span>

## <span data-ttu-id="35940-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35940-108">EXAMPLES</span></span>

### <span data-ttu-id="35940-109">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="35940-109">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsInfrastructureRoleInstance -Name "n22r0903-Xrp03"

Shutdown an infrastructure role instance for maintenance.
```

<span data-ttu-id="35940-110">Завершение работы с экземпляром роли инфраструктуры для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="35940-110">Shutdown an infrastructure role instance for maintenance.</span></span>


## <span data-ttu-id="35940-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35940-111">PARAMETERS</span></span>

### <span data-ttu-id="35940-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35940-112">-AsJob</span></span>
<span data-ttu-id="35940-113">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="35940-113">Run the command as a job</span></span>

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

### <span data-ttu-id="35940-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35940-114">-DefaultProfile</span></span>
<span data-ttu-id="35940-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35940-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35940-116">-Force</span><span class="sxs-lookup"><span data-stu-id="35940-116">-Force</span></span>
<span data-ttu-id="35940-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="35940-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="35940-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35940-118">-InputObject</span></span>
<span data-ttu-id="35940-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="35940-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="35940-120">-Location</span><span class="sxs-lookup"><span data-stu-id="35940-120">-Location</span></span>
<span data-ttu-id="35940-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="35940-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="35940-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35940-122">-Name</span></span>
<span data-ttu-id="35940-123">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="35940-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="35940-124">-Wait</span><span class="sxs-lookup"><span data-stu-id="35940-124">-NoWait</span></span>
<span data-ttu-id="35940-125">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="35940-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="35940-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35940-126">-PassThru</span></span>
<span data-ttu-id="35940-127">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="35940-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="35940-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35940-128">-ResourceGroupName</span></span>
<span data-ttu-id="35940-129">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35940-129">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="35940-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35940-130">-SubscriptionId</span></span>
<span data-ttu-id="35940-131">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35940-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="35940-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="35940-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="35940-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35940-133">-Confirm</span></span>
<span data-ttu-id="35940-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35940-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35940-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35940-135">-WhatIf</span></span>
<span data-ttu-id="35940-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35940-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35940-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35940-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35940-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35940-138">CommonParameters</span></span>
<span data-ttu-id="35940-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35940-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35940-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35940-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35940-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35940-141">INPUTS</span></span>

### <span data-ttu-id="35940-142">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="35940-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="35940-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35940-143">OUTPUTS</span></span>

### <span data-ttu-id="35940-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35940-144">System.Boolean</span></span>



## <span data-ttu-id="35940-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="35940-145">NOTES</span></span>

<span data-ttu-id="35940-146">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="35940-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35940-147">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35940-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="35940-148">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="35940-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35940-149">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="35940-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="35940-150">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="35940-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="35940-151">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="35940-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="35940-152">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="35940-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="35940-153">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="35940-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="35940-154">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="35940-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="35940-155">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="35940-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35940-156">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="35940-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="35940-157">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="35940-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="35940-158">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="35940-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="35940-159">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="35940-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="35940-160">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="35940-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="35940-161">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="35940-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="35940-162">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="35940-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="35940-163">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35940-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="35940-164">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="35940-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="35940-165">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="35940-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="35940-166">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="35940-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="35940-167">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="35940-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="35940-168">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="35940-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="35940-169">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35940-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="35940-170">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="35940-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="35940-171">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="35940-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="35940-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35940-172">RELATED LINKS</span></span>

