---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d1534c7cfacbcc70c2fe822676d67142401f9ff9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910527"
---
# <span data-ttu-id="ab2d7-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="ab2d7-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="ab2d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab2d7-102">SYNOPSIS</span></span>


## <span data-ttu-id="ab2d7-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab2d7-103">SYNTAX</span></span>

### <span data-ttu-id="ab2d7-104">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab2d7-104">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ab2d7-105">Получить</span><span class="sxs-lookup"><span data-stu-id="ab2d7-105">Get</span></span>
```
Get-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ab2d7-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ab2d7-106">GetViaIdentity</span></span>
```
Get-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="ab2d7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab2d7-107">DESCRIPTION</span></span>


## <span data-ttu-id="ab2d7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab2d7-108">EXAMPLES</span></span>

### <span data-ttu-id="ab2d7-109">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="ab2d7-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode

A list of all scale unit nodes at a location.
```

<span data-ttu-id="ab2d7-110">Получить все узлы единиц измерения шкалы в местоположении.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-110">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="ab2d7-111">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="ab2d7-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode -Name "HC1n25r2231"

A specific scale unit node at a location given a name.
```

<span data-ttu-id="ab2d7-112">Получение определенного узла единиц измерения на месте с определенным именем.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-112">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="ab2d7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab2d7-113">PARAMETERS</span></span>

### <span data-ttu-id="ab2d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2d7-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="ab2d7-115">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="ab2d7-115">-Filter</span></span>


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

### <span data-ttu-id="ab2d7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab2d7-116">-InputObject</span></span>
<span data-ttu-id="ab2d7-117">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ab2d7-118">-Location</span><span class="sxs-lookup"><span data-stu-id="ab2d7-118">-Location</span></span>


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

### <span data-ttu-id="ab2d7-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ab2d7-119">-Name</span></span>


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

### <span data-ttu-id="ab2d7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab2d7-120">-PassThru</span></span>


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

### <span data-ttu-id="ab2d7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab2d7-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="ab2d7-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab2d7-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="ab2d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2d7-123">CommonParameters</span></span>
<span data-ttu-id="ab2d7-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2d7-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab2d7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2d7-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab2d7-126">INPUTS</span></span>

### <span data-ttu-id="ab2d7-127">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ab2d7-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="ab2d7-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab2d7-128">OUTPUTS</span></span>

### <span data-ttu-id="ab2d7-129">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="ab2d7-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnitNode</span></span>



## <span data-ttu-id="ab2d7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab2d7-130">NOTES</span></span>

<span data-ttu-id="ab2d7-131">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab2d7-132">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ab2d7-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="ab2d7-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="ab2d7-134">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="ab2d7-135">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="ab2d7-136">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="ab2d7-137">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="ab2d7-138">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="ab2d7-139">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="ab2d7-140">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="ab2d7-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ab2d7-141">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="ab2d7-142">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="ab2d7-143">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ab2d7-144">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="ab2d7-145">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="ab2d7-146">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="ab2d7-147">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="ab2d7-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ab2d7-149">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="ab2d7-150">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="ab2d7-151">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="ab2d7-152">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="ab2d7-153">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ab2d7-154">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ab2d7-155">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="ab2d7-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="ab2d7-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab2d7-156">RELATED LINKS</span></span>

