---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunit
schema: 2.0.0
ms.openlocfilehash: cef23066fe1bfcd0b428302aab6c8077a8f676b6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075308"
---
# <span data-ttu-id="97ac5-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="97ac5-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="97ac5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="97ac5-103">Возвращает запрашиваемую единицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="97ac5-103">Returns the requested scale unit.</span></span>

## <span data-ttu-id="97ac5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97ac5-104">SYNTAX</span></span>

### <span data-ttu-id="97ac5-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97ac5-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="97ac5-106">Получить</span><span class="sxs-lookup"><span data-stu-id="97ac5-106">Get</span></span>
```
Get-AzsScaleUnit -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="97ac5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97ac5-107">GetViaIdentity</span></span>
```
Get-AzsScaleUnit -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="97ac5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97ac5-108">DESCRIPTION</span></span>
<span data-ttu-id="97ac5-109">Возвращает запрашиваемую единицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="97ac5-109">Returns the requested scale unit.</span></span>

## <span data-ttu-id="97ac5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97ac5-110">EXAMPLES</span></span>

### <span data-ttu-id="97ac5-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="97ac5-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnit

A list of information about scale units.
```

<span data-ttu-id="97ac5-112">Возвращает список сведений о единицах шкалы.</span><span class="sxs-lookup"><span data-stu-id="97ac5-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="97ac5-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="97ac5-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnit -Name "S-Cluster"

The information about a specific scale unit.
```

<span data-ttu-id="97ac5-114">Возвращают сведения о конкретном единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="97ac5-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="97ac5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97ac5-115">PARAMETERS</span></span>

### <span data-ttu-id="97ac5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ac5-116">-DefaultProfile</span></span>
<span data-ttu-id="97ac5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97ac5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97ac5-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="97ac5-118">-Filter</span></span>
<span data-ttu-id="97ac5-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="97ac5-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="97ac5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97ac5-120">-InputObject</span></span>
<span data-ttu-id="97ac5-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="97ac5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97ac5-122">-Location</span><span class="sxs-lookup"><span data-stu-id="97ac5-122">-Location</span></span>
<span data-ttu-id="97ac5-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="97ac5-123">Location of the resource.</span></span>

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

### <span data-ttu-id="97ac5-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97ac5-124">-Name</span></span>
<span data-ttu-id="97ac5-125">Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="97ac5-125">Name of the scale units.</span></span>

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

### <span data-ttu-id="97ac5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97ac5-126">-PassThru</span></span>
<span data-ttu-id="97ac5-127">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="97ac5-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="97ac5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ac5-128">-ResourceGroupName</span></span>
<span data-ttu-id="97ac5-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97ac5-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="97ac5-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97ac5-130">-SubscriptionId</span></span>
<span data-ttu-id="97ac5-131">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97ac5-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="97ac5-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="97ac5-132">The subscription ID forms part of the URI for every service call.</span></span>


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

### <span data-ttu-id="97ac5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ac5-133">CommonParameters</span></span>
<span data-ttu-id="97ac5-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97ac5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ac5-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97ac5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ac5-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97ac5-136">INPUTS</span></span>

### <span data-ttu-id="97ac5-137">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="97ac5-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="97ac5-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97ac5-138">OUTPUTS</span></span>

### <span data-ttu-id="97ac5-139">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IScaleUnit</span><span class="sxs-lookup"><span data-stu-id="97ac5-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnit</span></span>



## <span data-ttu-id="97ac5-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="97ac5-140">NOTES</span></span>

<span data-ttu-id="97ac5-141">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="97ac5-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97ac5-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97ac5-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="97ac5-143">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="97ac5-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97ac5-144">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="97ac5-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="97ac5-145">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="97ac5-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="97ac5-146">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="97ac5-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="97ac5-147">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="97ac5-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="97ac5-148">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="97ac5-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="97ac5-149">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="97ac5-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="97ac5-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="97ac5-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97ac5-151">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="97ac5-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="97ac5-152">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="97ac5-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="97ac5-153">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="97ac5-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="97ac5-154">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="97ac5-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="97ac5-155">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="97ac5-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="97ac5-156">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="97ac5-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="97ac5-157">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="97ac5-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="97ac5-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97ac5-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="97ac5-159">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="97ac5-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="97ac5-160">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="97ac5-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="97ac5-161">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="97ac5-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="97ac5-162">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="97ac5-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="97ac5-163">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="97ac5-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="97ac5-164">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97ac5-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="97ac5-165">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="97ac5-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="97ac5-166">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="97ac5-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="97ac5-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97ac5-167">RELATED LINKS</span></span>

