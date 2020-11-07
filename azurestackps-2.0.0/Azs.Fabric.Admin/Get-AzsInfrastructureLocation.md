---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910530"
---
# <span data-ttu-id="4abbe-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="4abbe-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="4abbe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4abbe-102">SYNOPSIS</span></span>
<span data-ttu-id="4abbe-103">Возвращает указанное расположение структуры.</span><span class="sxs-lookup"><span data-stu-id="4abbe-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="4abbe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4abbe-104">SYNTAX</span></span>

### <span data-ttu-id="4abbe-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4abbe-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4abbe-106">Получить</span><span class="sxs-lookup"><span data-stu-id="4abbe-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4abbe-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4abbe-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4abbe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4abbe-108">DESCRIPTION</span></span>
<span data-ttu-id="4abbe-109">Возвращает указанное расположение структуры.</span><span class="sxs-lookup"><span data-stu-id="4abbe-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="4abbe-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4abbe-110">EXAMPLES</span></span>

### <span data-ttu-id="4abbe-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="4abbe-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="4abbe-112">Получение списка всех структурных местоположений.</span><span class="sxs-lookup"><span data-stu-id="4abbe-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="4abbe-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="4abbe-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="4abbe-114">Получение расположения на основе имени.</span><span class="sxs-lookup"><span data-stu-id="4abbe-114">Get a location based on the name.</span></span>

## <span data-ttu-id="4abbe-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4abbe-115">PARAMETERS</span></span>

### <span data-ttu-id="4abbe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abbe-116">-DefaultProfile</span></span>
<span data-ttu-id="4abbe-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4abbe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4abbe-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="4abbe-118">-FabricLocation</span></span>
<span data-ttu-id="4abbe-119">Расположение структуры.</span><span class="sxs-lookup"><span data-stu-id="4abbe-119">Fabric location.</span></span>

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

### <span data-ttu-id="4abbe-120">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="4abbe-120">-Filter</span></span>
<span data-ttu-id="4abbe-121">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="4abbe-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="4abbe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4abbe-122">-InputObject</span></span>
<span data-ttu-id="4abbe-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4abbe-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4abbe-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4abbe-124">-PassThru</span></span>
<span data-ttu-id="4abbe-125">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4abbe-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4abbe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4abbe-126">-ResourceGroupName</span></span>
<span data-ttu-id="4abbe-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4abbe-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="4abbe-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4abbe-128">-SubscriptionId</span></span>
<span data-ttu-id="4abbe-129">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4abbe-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4abbe-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4abbe-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4abbe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abbe-131">CommonParameters</span></span>
<span data-ttu-id="4abbe-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4abbe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abbe-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4abbe-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abbe-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4abbe-134">INPUTS</span></span>

### <span data-ttu-id="4abbe-135">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4abbe-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="4abbe-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4abbe-136">OUTPUTS</span></span>

### <span data-ttu-id="4abbe-137">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IFabricLocation</span><span class="sxs-lookup"><span data-stu-id="4abbe-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="4abbe-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="4abbe-138">NOTES</span></span>

<span data-ttu-id="4abbe-139">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4abbe-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4abbe-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4abbe-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4abbe-141">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="4abbe-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4abbe-142">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="4abbe-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="4abbe-143">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="4abbe-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="4abbe-144">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="4abbe-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="4abbe-145">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="4abbe-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="4abbe-146">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="4abbe-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="4abbe-147">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="4abbe-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="4abbe-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="4abbe-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4abbe-149">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="4abbe-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="4abbe-150">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="4abbe-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="4abbe-151">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="4abbe-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4abbe-152">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="4abbe-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="4abbe-153">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="4abbe-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="4abbe-154">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="4abbe-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="4abbe-155">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="4abbe-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="4abbe-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4abbe-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4abbe-157">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="4abbe-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="4abbe-158">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="4abbe-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="4abbe-159">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="4abbe-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="4abbe-160">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="4abbe-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="4abbe-161">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4abbe-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4abbe-162">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4abbe-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4abbe-163">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="4abbe-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="4abbe-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4abbe-164">RELATED LINKS</span></span>

