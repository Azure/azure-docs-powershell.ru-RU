---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076626"
---
# <span data-ttu-id="cf4aa-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="cf4aa-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="cf4aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf4aa-102">SYNOPSIS</span></span>


## <span data-ttu-id="cf4aa-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf4aa-103">SYNTAX</span></span>

### <span data-ttu-id="cf4aa-104">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf4aa-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cf4aa-105">Получить</span><span class="sxs-lookup"><span data-stu-id="cf4aa-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cf4aa-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf4aa-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="cf4aa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf4aa-107">DESCRIPTION</span></span>


## <span data-ttu-id="cf4aa-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf4aa-108">EXAMPLES</span></span>

### <span data-ttu-id="cf4aa-109">Пример 1: получение списка всех пулов шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="cf4aa-110">Получение списка всех пулов шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="cf4aa-111">Пример 2: получение пула определенного шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="cf4aa-112">Получение пула шлюзов с определенным краем.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="cf4aa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf4aa-113">PARAMETERS</span></span>

### <span data-ttu-id="cf4aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf4aa-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="cf4aa-115">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="cf4aa-115">-Filter</span></span>


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

### <span data-ttu-id="cf4aa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf4aa-116">-InputObject</span></span>
<span data-ttu-id="cf4aa-117">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf4aa-118">-Location</span><span class="sxs-lookup"><span data-stu-id="cf4aa-118">-Location</span></span>


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

### <span data-ttu-id="cf4aa-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf4aa-119">-Name</span></span>


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

### <span data-ttu-id="cf4aa-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf4aa-120">-PassThru</span></span>


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

### <span data-ttu-id="cf4aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf4aa-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="cf4aa-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf4aa-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="cf4aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf4aa-123">CommonParameters</span></span>
<span data-ttu-id="cf4aa-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf4aa-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf4aa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf4aa-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf4aa-126">INPUTS</span></span>

### <span data-ttu-id="cf4aa-127">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cf4aa-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cf4aa-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf4aa-128">OUTPUTS</span></span>

### <span data-ttu-id="cf4aa-129">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="cf4aa-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="cf4aa-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf4aa-130">NOTES</span></span>

<span data-ttu-id="cf4aa-131">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf4aa-132">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cf4aa-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="cf4aa-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="cf4aa-134">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cf4aa-135">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cf4aa-136">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cf4aa-137">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cf4aa-138">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cf4aa-139">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cf4aa-140">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="cf4aa-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf4aa-141">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cf4aa-142">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cf4aa-143">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cf4aa-144">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cf4aa-145">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cf4aa-146">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cf4aa-147">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cf4aa-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cf4aa-149">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cf4aa-150">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cf4aa-151">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cf4aa-152">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cf4aa-153">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cf4aa-154">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cf4aa-155">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="cf4aa-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cf4aa-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf4aa-156">RELATED LINKS</span></span>
