---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalsubnet
schema: 2.0.0
ms.openlocfilehash: eae4d8e861b6b229cfa3e5fe9b4e424a69c487c2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076674"
---
# <span data-ttu-id="64783-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="64783-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="64783-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64783-102">SYNOPSIS</span></span>
<span data-ttu-id="64783-103">Возвращает запрошенную логическую подсеть.</span><span class="sxs-lookup"><span data-stu-id="64783-103">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="64783-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64783-104">SYNTAX</span></span>

### <span data-ttu-id="64783-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64783-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="64783-106">Получить</span><span class="sxs-lookup"><span data-stu-id="64783-106">Get</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="64783-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64783-107">GetViaIdentity</span></span>
```
Get-AzsLogicalSubnet -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="64783-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64783-108">DESCRIPTION</span></span>
<span data-ttu-id="64783-109">Возвращает запрошенную логическую подсеть.</span><span class="sxs-lookup"><span data-stu-id="64783-109">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="64783-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64783-110">EXAMPLES</span></span>

### <span data-ttu-id="64783-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="64783-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="64783-112">Получение всех логических сетей в расположении.</span><span class="sxs-lookup"><span data-stu-id="64783-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="64783-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="64783-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A a specific logical networks at a location based on a name.
```

<span data-ttu-id="64783-114">Получение конкретных логических сетей в местоположении на основе имени.</span><span class="sxs-lookup"><span data-stu-id="64783-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="64783-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64783-115">PARAMETERS</span></span>

### <span data-ttu-id="64783-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64783-116">-DefaultProfile</span></span>
<span data-ttu-id="64783-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64783-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64783-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="64783-118">-Filter</span></span>
<span data-ttu-id="64783-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="64783-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="64783-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64783-120">-InputObject</span></span>
<span data-ttu-id="64783-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="64783-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="64783-122">-Location</span><span class="sxs-lookup"><span data-stu-id="64783-122">-Location</span></span>
<span data-ttu-id="64783-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="64783-123">Location of the resource.</span></span>

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

### <span data-ttu-id="64783-124">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="64783-124">-LogicalNetwork</span></span>
<span data-ttu-id="64783-125">Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="64783-125">Name of the logical network.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="64783-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="64783-126">-Name</span></span>
<span data-ttu-id="64783-127">Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="64783-127">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="64783-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64783-128">-PassThru</span></span>
<span data-ttu-id="64783-129">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="64783-129">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64783-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64783-130">-ResourceGroupName</span></span>
<span data-ttu-id="64783-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64783-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="64783-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64783-132">-SubscriptionId</span></span>
<span data-ttu-id="64783-133">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64783-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="64783-134">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="64783-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="64783-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64783-135">CommonParameters</span></span>
<span data-ttu-id="64783-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64783-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64783-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64783-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64783-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64783-138">INPUTS</span></span>

### <span data-ttu-id="64783-139">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="64783-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="64783-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64783-140">OUTPUTS</span></span>

### <span data-ttu-id="64783-141">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. ILogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="64783-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalSubnet</span></span>



## <span data-ttu-id="64783-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="64783-142">NOTES</span></span>

<span data-ttu-id="64783-143">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="64783-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64783-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64783-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="64783-145">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="64783-145">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64783-146">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="64783-146">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="64783-147">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="64783-147">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="64783-148">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="64783-148">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="64783-149">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="64783-149">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="64783-150">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="64783-150">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="64783-151">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="64783-151">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="64783-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="64783-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64783-153">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="64783-153">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="64783-154">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="64783-154">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="64783-155">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="64783-155">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="64783-156">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="64783-156">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="64783-157">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="64783-157">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="64783-158">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="64783-158">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="64783-159">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="64783-159">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="64783-160">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64783-160">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="64783-161">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="64783-161">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="64783-162">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="64783-162">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="64783-163">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="64783-163">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="64783-164">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="64783-164">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="64783-165">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="64783-165">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="64783-166">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64783-166">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="64783-167">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="64783-167">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="64783-168">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="64783-168">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="64783-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64783-169">RELATED LINKS</span></span>

