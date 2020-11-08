---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075356"
---
# <span data-ttu-id="a62f3-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="a62f3-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="a62f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a62f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a62f3-103">Возвращает запрашиваемый шлюз Edge.</span><span class="sxs-lookup"><span data-stu-id="a62f3-103">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="a62f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a62f3-104">SYNTAX</span></span>

### <span data-ttu-id="a62f3-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a62f3-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a62f3-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a62f3-106">Get</span></span>
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a62f3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a62f3-107">GetViaIdentity</span></span>
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="a62f3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a62f3-108">DESCRIPTION</span></span>
<span data-ttu-id="a62f3-109">Возвращает запрашиваемый шлюз Edge.</span><span class="sxs-lookup"><span data-stu-id="a62f3-109">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="a62f3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a62f3-110">EXAMPLES</span></span>

### <span data-ttu-id="a62f3-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="a62f3-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

<span data-ttu-id="a62f3-112">Возвращает список всех шлюзов EDGE в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="a62f3-112">Returns the list of all edge gateways at a certain location.</span></span>


## <span data-ttu-id="a62f3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a62f3-113">PARAMETERS</span></span>

### <span data-ttu-id="a62f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62f3-114">-DefaultProfile</span></span>
<span data-ttu-id="a62f3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a62f3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a62f3-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="a62f3-116">-Filter</span></span>
<span data-ttu-id="a62f3-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="a62f3-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a62f3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a62f3-118">-InputObject</span></span>
<span data-ttu-id="a62f3-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a62f3-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a62f3-120">-Location</span><span class="sxs-lookup"><span data-stu-id="a62f3-120">-Location</span></span>
<span data-ttu-id="a62f3-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a62f3-121">Location of the resource.</span></span>

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

### <span data-ttu-id="a62f3-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a62f3-122">-Name</span></span>
<span data-ttu-id="a62f3-123">Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="a62f3-123">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="a62f3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a62f3-124">-PassThru</span></span>
<span data-ttu-id="a62f3-125">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a62f3-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a62f3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a62f3-126">-ResourceGroupName</span></span>
<span data-ttu-id="a62f3-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a62f3-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="a62f3-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a62f3-128">-SubscriptionId</span></span>
<span data-ttu-id="a62f3-129">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a62f3-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a62f3-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a62f3-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a62f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62f3-131">CommonParameters</span></span>
<span data-ttu-id="a62f3-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a62f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62f3-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a62f3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62f3-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a62f3-134">INPUTS</span></span>

### <span data-ttu-id="a62f3-135">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a62f3-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="a62f3-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a62f3-136">OUTPUTS</span></span>

### <span data-ttu-id="a62f3-137">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="a62f3-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGateway</span></span>



## <span data-ttu-id="a62f3-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a62f3-138">NOTES</span></span>

<span data-ttu-id="a62f3-139">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a62f3-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a62f3-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a62f3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a62f3-141">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a62f3-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a62f3-142">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="a62f3-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="a62f3-143">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="a62f3-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="a62f3-144">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="a62f3-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="a62f3-145">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="a62f3-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="a62f3-146">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="a62f3-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="a62f3-147">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="a62f3-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="a62f3-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="a62f3-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a62f3-149">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="a62f3-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="a62f3-150">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="a62f3-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="a62f3-151">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a62f3-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a62f3-152">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="a62f3-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="a62f3-153">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="a62f3-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="a62f3-154">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="a62f3-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="a62f3-155">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="a62f3-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="a62f3-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a62f3-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a62f3-157">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="a62f3-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="a62f3-158">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="a62f3-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="a62f3-159">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="a62f3-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="a62f3-160">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="a62f3-160">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="a62f3-161">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="a62f3-161">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="a62f3-162">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a62f3-162">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a62f3-163">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a62f3-163">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a62f3-164">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="a62f3-164">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="a62f3-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a62f3-165">RELATED LINKS</span></span>

