---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/enable-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4a7140d5162f046377e37b92d4e6931abdbb4cf4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075229"
---
# <span data-ttu-id="57ac6-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="57ac6-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="57ac6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57ac6-102">SYNOPSIS</span></span>


## <span data-ttu-id="57ac6-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57ac6-103">SYNTAX</span></span>

### <span data-ttu-id="57ac6-104">Начало (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57ac6-104">Start (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="57ac6-105">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57ac6-105">StartViaIdentity</span></span>
```
Enable-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57ac6-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57ac6-106">DESCRIPTION</span></span>


## <span data-ttu-id="57ac6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57ac6-107">EXAMPLES</span></span>

### <span data-ttu-id="57ac6-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="57ac6-108">Example 1:</span></span>
```powershell
PS C:\> Enable-AzsScaleUnitNode -Name "HC1n25r2236"

Stop maintenance mode on a scale unit node.
```

<span data-ttu-id="57ac6-109">Отключение режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="57ac6-109">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="57ac6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57ac6-110">PARAMETERS</span></span>

### <span data-ttu-id="57ac6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57ac6-111">-AsJob</span></span>


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

### <span data-ttu-id="57ac6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ac6-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="57ac6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="57ac6-113">-Force</span></span>


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

### <span data-ttu-id="57ac6-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57ac6-114">-InputObject</span></span>
<span data-ttu-id="57ac6-115">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="57ac6-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="57ac6-116">-Location</span><span class="sxs-lookup"><span data-stu-id="57ac6-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57ac6-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="57ac6-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57ac6-118">-Wait</span><span class="sxs-lookup"><span data-stu-id="57ac6-118">-NoWait</span></span>


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

### <span data-ttu-id="57ac6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57ac6-119">-PassThru</span></span>


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

### <span data-ttu-id="57ac6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ac6-120">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57ac6-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57ac6-121">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57ac6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57ac6-122">-Confirm</span></span>
<span data-ttu-id="57ac6-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="57ac6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57ac6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ac6-124">-WhatIf</span></span>
<span data-ttu-id="57ac6-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="57ac6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57ac6-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57ac6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57ac6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ac6-127">CommonParameters</span></span>
<span data-ttu-id="57ac6-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57ac6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ac6-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57ac6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ac6-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57ac6-130">INPUTS</span></span>

### <span data-ttu-id="57ac6-131">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="57ac6-131">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="57ac6-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57ac6-132">OUTPUTS</span></span>

### <span data-ttu-id="57ac6-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="57ac6-133">System.Boolean</span></span>



## <span data-ttu-id="57ac6-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="57ac6-134">NOTES</span></span>

<span data-ttu-id="57ac6-135">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="57ac6-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57ac6-136">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57ac6-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="57ac6-137">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="57ac6-137">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="57ac6-138">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="57ac6-138">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="57ac6-139">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="57ac6-139">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="57ac6-140">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="57ac6-140">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="57ac6-141">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="57ac6-141">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="57ac6-142">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="57ac6-142">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="57ac6-143">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="57ac6-143">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="57ac6-144">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="57ac6-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57ac6-145">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="57ac6-145">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="57ac6-146">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="57ac6-146">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="57ac6-147">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="57ac6-147">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="57ac6-148">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="57ac6-148">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="57ac6-149">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="57ac6-149">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="57ac6-150">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="57ac6-150">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="57ac6-151">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="57ac6-151">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="57ac6-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57ac6-152">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="57ac6-153">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="57ac6-153">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="57ac6-154">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="57ac6-154">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="57ac6-155">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="57ac6-155">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="57ac6-156">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="57ac6-156">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="57ac6-157">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57ac6-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="57ac6-158">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="57ac6-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="57ac6-159">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="57ac6-159">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="57ac6-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57ac6-160">RELATED LINKS</span></span>

