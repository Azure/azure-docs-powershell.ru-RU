---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: b5eb59c1f2ad631e8cbb9fdffbf65bee00425d43
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076767"
---
# <span data-ttu-id="d9456-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="d9456-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="d9456-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9456-102">SYNOPSIS</span></span>
<span data-ttu-id="d9456-103">Возврат запрашиваемого экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="d9456-103">Return the requested infrastructure role instance.</span></span>

## <span data-ttu-id="d9456-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9456-104">SYNTAX</span></span>

### <span data-ttu-id="d9456-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9456-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d9456-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d9456-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d9456-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d9456-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="d9456-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9456-108">DESCRIPTION</span></span>
<span data-ttu-id="d9456-109">Возврат запрашиваемого экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="d9456-109">Return the requested infrastructure role instance.</span></span>

## <span data-ttu-id="d9456-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9456-110">EXAMPLES</span></span>

### <span data-ttu-id="d9456-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="d9456-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance

A list of all infrastructure role instances.
```

<span data-ttu-id="d9456-112">Возвращают список всех экземпляров ролей инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="d9456-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="d9456-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="d9456-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

A single infrastructure role instance based on name.
```

<span data-ttu-id="d9456-114">Возвращают единственный экземпляр роли инфраструктуры на основе имени.</span><span class="sxs-lookup"><span data-stu-id="d9456-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="d9456-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9456-115">PARAMETERS</span></span>

### <span data-ttu-id="d9456-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9456-116">-DefaultProfile</span></span>
<span data-ttu-id="d9456-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9456-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9456-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="d9456-118">-Filter</span></span>
<span data-ttu-id="d9456-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="d9456-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="d9456-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9456-120">-InputObject</span></span>
<span data-ttu-id="d9456-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d9456-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d9456-122">-Location</span><span class="sxs-lookup"><span data-stu-id="d9456-122">-Location</span></span>
<span data-ttu-id="d9456-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d9456-123">Location of the resource.</span></span>

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

### <span data-ttu-id="d9456-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9456-124">-Name</span></span>
<span data-ttu-id="d9456-125">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="d9456-125">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="d9456-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9456-126">-PassThru</span></span>
<span data-ttu-id="d9456-127">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d9456-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d9456-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9456-128">-ResourceGroupName</span></span>
<span data-ttu-id="d9456-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9456-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="d9456-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9456-130">-SubscriptionId</span></span>
<span data-ttu-id="d9456-131">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9456-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9456-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d9456-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d9456-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9456-133">CommonParameters</span></span>
<span data-ttu-id="d9456-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9456-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9456-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9456-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9456-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9456-136">INPUTS</span></span>

### <span data-ttu-id="d9456-137">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d9456-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="d9456-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9456-138">OUTPUTS</span></span>

### <span data-ttu-id="d9456-139">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IInfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="d9456-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IInfraRoleInstance</span></span>



## <span data-ttu-id="d9456-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9456-140">NOTES</span></span>

<span data-ttu-id="d9456-141">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d9456-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9456-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9456-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d9456-143">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d9456-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d9456-144">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="d9456-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="d9456-145">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="d9456-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="d9456-146">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="d9456-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="d9456-147">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="d9456-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="d9456-148">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="d9456-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="d9456-149">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d9456-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="d9456-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d9456-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d9456-151">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="d9456-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="d9456-152">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="d9456-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="d9456-153">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d9456-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d9456-154">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="d9456-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="d9456-155">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="d9456-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="d9456-156">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="d9456-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="d9456-157">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="d9456-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="d9456-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9456-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d9456-159">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="d9456-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="d9456-160">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d9456-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="d9456-161">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="d9456-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="d9456-162">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="d9456-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="d9456-163">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="d9456-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="d9456-164">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9456-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d9456-165">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d9456-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d9456-166">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="d9456-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="d9456-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9456-167">RELATED LINKS</span></span>

