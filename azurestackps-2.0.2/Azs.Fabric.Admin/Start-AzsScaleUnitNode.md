---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: c8b1ed8ea0be65e92022cf1ac759024a07fc76c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076698"
---
# <span data-ttu-id="2dc83-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="2dc83-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="2dc83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2dc83-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc83-103">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="2dc83-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="2dc83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2dc83-104">SYNTAX</span></span>

### <span data-ttu-id="2dc83-105">PowerOn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2dc83-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2dc83-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2dc83-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2dc83-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dc83-107">DESCRIPTION</span></span>
<span data-ttu-id="2dc83-108">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="2dc83-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="2dc83-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2dc83-109">EXAMPLES</span></span>

### <span data-ttu-id="2dc83-110">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="2dc83-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="2dc83-111">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="2dc83-111">Power on a scale unit node.</span></span>

### <span data-ttu-id="2dc83-112">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="2dc83-112">Example 2:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="2dc83-113">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="2dc83-113">Power on a scale unit node.</span></span> <span data-ttu-id="2dc83-114">Как задание.</span><span class="sxs-lookup"><span data-stu-id="2dc83-114">As a job.</span></span>

## <span data-ttu-id="2dc83-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2dc83-115">PARAMETERS</span></span>

### <span data-ttu-id="2dc83-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dc83-116">-AsJob</span></span>
<span data-ttu-id="2dc83-117">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="2dc83-117">Run the command as a job</span></span>

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

### <span data-ttu-id="2dc83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc83-118">-DefaultProfile</span></span>
<span data-ttu-id="2dc83-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2dc83-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dc83-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2dc83-120">-Force</span></span>
<span data-ttu-id="2dc83-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2dc83-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2dc83-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dc83-122">-InputObject</span></span>
<span data-ttu-id="2dc83-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="2dc83-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOnViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2dc83-124">-Location</span><span class="sxs-lookup"><span data-stu-id="2dc83-124">-Location</span></span>
<span data-ttu-id="2dc83-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2dc83-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dc83-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2dc83-126">-Name</span></span>
<span data-ttu-id="2dc83-127">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2dc83-127">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dc83-128">-Wait</span><span class="sxs-lookup"><span data-stu-id="2dc83-128">-NoWait</span></span>
<span data-ttu-id="2dc83-129">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="2dc83-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2dc83-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dc83-130">-PassThru</span></span>
<span data-ttu-id="2dc83-131">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2dc83-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2dc83-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc83-132">-ResourceGroupName</span></span>
<span data-ttu-id="2dc83-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2dc83-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dc83-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2dc83-134">-SubscriptionId</span></span>
<span data-ttu-id="2dc83-135">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2dc83-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2dc83-136">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="2dc83-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dc83-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2dc83-137">-Confirm</span></span>
<span data-ttu-id="2dc83-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2dc83-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dc83-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dc83-139">-WhatIf</span></span>
<span data-ttu-id="2dc83-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2dc83-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dc83-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2dc83-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dc83-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc83-142">CommonParameters</span></span>
<span data-ttu-id="2dc83-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2dc83-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc83-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dc83-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc83-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2dc83-145">INPUTS</span></span>

### <span data-ttu-id="2dc83-146">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2dc83-146">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="2dc83-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dc83-147">OUTPUTS</span></span>

### <span data-ttu-id="2dc83-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2dc83-148">System.Boolean</span></span>

## <span data-ttu-id="2dc83-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="2dc83-149">NOTES</span></span>

<span data-ttu-id="2dc83-150">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2dc83-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2dc83-151">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2dc83-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2dc83-152">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="2dc83-152">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2dc83-153">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="2dc83-153">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="2dc83-154">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="2dc83-154">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="2dc83-155">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="2dc83-155">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="2dc83-156">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="2dc83-156">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="2dc83-157">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="2dc83-157">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="2dc83-158">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2dc83-158">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="2dc83-159">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="2dc83-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2dc83-160">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="2dc83-160">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="2dc83-161">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="2dc83-161">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="2dc83-162">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2dc83-162">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2dc83-163">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="2dc83-163">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="2dc83-164">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="2dc83-164">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="2dc83-165">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="2dc83-165">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="2dc83-166">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="2dc83-166">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="2dc83-167">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2dc83-167">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2dc83-168">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="2dc83-168">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="2dc83-169">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2dc83-169">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="2dc83-170">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="2dc83-170">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="2dc83-171">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="2dc83-171">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="2dc83-172">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="2dc83-172">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="2dc83-173">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2dc83-173">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2dc83-174">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="2dc83-174">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2dc83-175">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="2dc83-175">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="2dc83-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dc83-176">RELATED LINKS</span></span>
