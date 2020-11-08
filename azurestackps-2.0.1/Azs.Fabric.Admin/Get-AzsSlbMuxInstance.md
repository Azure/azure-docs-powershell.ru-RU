---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsslbmuxinstance
schema: 2.0.0
ms.openlocfilehash: 64e33236bbdd3f07969f6633356c98b593ee672f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075307"
---
# <span data-ttu-id="2a8f4-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="2a8f4-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="2a8f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8f4-103">Возвращает запрошенный экземпляр мультиплексора подсистемы балансировки нагрузки программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-103">Returns the requested software load balancer multiplexer instance.</span></span>

## <span data-ttu-id="2a8f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a8f4-104">SYNTAX</span></span>

### <span data-ttu-id="2a8f4-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a8f4-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="2a8f4-106">Получить</span><span class="sxs-lookup"><span data-stu-id="2a8f4-106">Get</span></span>
```
Get-AzsSlbMuxInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="2a8f4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2a8f4-107">GetViaIdentity</span></span>
```
Get-AzsSlbMuxInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="2a8f4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a8f4-108">DESCRIPTION</span></span>
<span data-ttu-id="2a8f4-109">Возвращает запрошенный экземпляр мультиплексора подсистемы балансировки нагрузки программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-109">Returns the requested software load balancer multiplexer instance.</span></span>

## <span data-ttu-id="2a8f4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a8f4-110">EXAMPLES</span></span>

### <span data-ttu-id="2a8f4-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="2a8f4-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsSlbMuxInstance

A list of all software load balancer multiplexer instance at a location.
```

<span data-ttu-id="2a8f4-112">Получить весь экземпляр мультиплексора подсистемы балансировки нагрузки программного обеспечения в местоположении.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="2a8f4-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="2a8f4-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsSlbMuxInstance -Name "AzS-SLB01"

A specific software load balancer multiplexer instance at a location given a name.
```

<span data-ttu-id="2a8f4-114">Получение определенного экземпляра мультиплексора подсистемы балансировки нагрузки программного обеспечения на месте с определенным именем.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="2a8f4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a8f4-115">PARAMETERS</span></span>

### <span data-ttu-id="2a8f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8f4-116">-DefaultProfile</span></span>
<span data-ttu-id="2a8f4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2a8f4-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="2a8f4-118">-Filter</span></span>
<span data-ttu-id="2a8f4-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="2a8f4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a8f4-120">-InputObject</span></span>
<span data-ttu-id="2a8f4-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a8f4-122">-Location</span><span class="sxs-lookup"><span data-stu-id="2a8f4-122">-Location</span></span>
<span data-ttu-id="2a8f4-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-123">Location of the resource.</span></span>

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

### <span data-ttu-id="2a8f4-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a8f4-124">-Name</span></span>
<span data-ttu-id="2a8f4-125">Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-125">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="2a8f4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a8f4-126">-PassThru</span></span>
<span data-ttu-id="2a8f4-127">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2a8f4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a8f4-128">-ResourceGroupName</span></span>
<span data-ttu-id="2a8f4-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="2a8f4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a8f4-130">-SubscriptionId</span></span>
<span data-ttu-id="2a8f4-131">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2a8f4-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2a8f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8f4-133">CommonParameters</span></span>
<span data-ttu-id="2a8f4-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8f4-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a8f4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8f4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a8f4-136">INPUTS</span></span>

### <span data-ttu-id="2a8f4-137">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2a8f4-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="2a8f4-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a8f4-138">OUTPUTS</span></span>

### <span data-ttu-id="2a8f4-139">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. ISlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="2a8f4-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ISlbMuxInstance</span></span>



## <span data-ttu-id="2a8f4-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a8f4-140">NOTES</span></span>

<span data-ttu-id="2a8f4-141">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a8f4-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2a8f4-143">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="2a8f4-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2a8f4-144">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="2a8f4-145">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="2a8f4-146">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="2a8f4-147">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="2a8f4-148">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="2a8f4-149">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="2a8f4-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="2a8f4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2a8f4-151">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="2a8f4-152">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="2a8f4-153">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2a8f4-154">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="2a8f4-155">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="2a8f4-156">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="2a8f4-157">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="2a8f4-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2a8f4-159">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="2a8f4-160">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="2a8f4-161">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="2a8f4-162">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="2a8f4-163">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="2a8f4-164">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2a8f4-165">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2a8f4-166">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="2a8f4-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="2a8f4-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a8f4-167">RELATED LINKS</span></span>

