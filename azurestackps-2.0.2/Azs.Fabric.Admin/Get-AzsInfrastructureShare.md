---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076673"
---
# <span data-ttu-id="d0346-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="d0346-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="d0346-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0346-102">SYNOPSIS</span></span>
<span data-ttu-id="d0346-103">Возвращает запрашиваемую общую структуру файла.</span><span class="sxs-lookup"><span data-stu-id="d0346-103">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="d0346-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0346-104">SYNTAX</span></span>

### <span data-ttu-id="d0346-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0346-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="d0346-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d0346-106">Get</span></span>
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d0346-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d0346-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="d0346-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0346-108">DESCRIPTION</span></span>
<span data-ttu-id="d0346-109">Возвращает запрашиваемую общую структуру файла.</span><span class="sxs-lookup"><span data-stu-id="d0346-109">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="d0346-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0346-110">EXAMPLES</span></span>

### <span data-ttu-id="d0346-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="d0346-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare
```

<span data-ttu-id="d0346-112">Возвращает список всех общих файловых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0346-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="d0346-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="d0346-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

<span data-ttu-id="d0346-114">Возвращает общую файловую систему на основе имени.</span><span class="sxs-lookup"><span data-stu-id="d0346-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="d0346-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0346-115">PARAMETERS</span></span>

### <span data-ttu-id="d0346-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0346-116">-DefaultProfile</span></span>
<span data-ttu-id="d0346-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0346-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0346-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="d0346-118">-Filter</span></span>
<span data-ttu-id="d0346-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="d0346-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="d0346-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0346-120">-InputObject</span></span>
<span data-ttu-id="d0346-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d0346-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d0346-122">-Location</span><span class="sxs-lookup"><span data-stu-id="d0346-122">-Location</span></span>
<span data-ttu-id="d0346-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d0346-123">Location of the resource.</span></span>

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

### <span data-ttu-id="d0346-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d0346-124">-Name</span></span>
<span data-ttu-id="d0346-125">Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="d0346-125">Fabric file share name.</span></span>

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

### <span data-ttu-id="d0346-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0346-126">-PassThru</span></span>
<span data-ttu-id="d0346-127">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d0346-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d0346-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0346-128">-ResourceGroupName</span></span>
<span data-ttu-id="d0346-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0346-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="d0346-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="d0346-130">-Skip</span></span>
<span data-ttu-id="d0346-131">Параметр пропуска OData.</span><span class="sxs-lookup"><span data-stu-id="d0346-131">OData skip parameter.</span></span>

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

### <span data-ttu-id="d0346-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0346-132">-SubscriptionId</span></span>
<span data-ttu-id="d0346-133">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d0346-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d0346-134">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d0346-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d0346-135">-Top</span><span class="sxs-lookup"><span data-stu-id="d0346-135">-Top</span></span>
<span data-ttu-id="d0346-136">Параметр TOP для OData.</span><span class="sxs-lookup"><span data-stu-id="d0346-136">OData top parameter.</span></span>

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

### <span data-ttu-id="d0346-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0346-137">CommonParameters</span></span>
<span data-ttu-id="d0346-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0346-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0346-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0346-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0346-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0346-140">INPUTS</span></span>

### <span data-ttu-id="d0346-141">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d0346-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="d0346-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0346-142">OUTPUTS</span></span>

### <span data-ttu-id="d0346-143">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IFileShare</span><span class="sxs-lookup"><span data-stu-id="d0346-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFileShare</span></span>



## <span data-ttu-id="d0346-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0346-144">NOTES</span></span>

<span data-ttu-id="d0346-145">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d0346-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d0346-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d0346-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d0346-147">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d0346-147">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d0346-148">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="d0346-148">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="d0346-149">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="d0346-149">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="d0346-150">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="d0346-150">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="d0346-151">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="d0346-151">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="d0346-152">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="d0346-152">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="d0346-153">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d0346-153">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="d0346-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d0346-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d0346-155">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="d0346-155">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="d0346-156">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="d0346-156">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="d0346-157">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d0346-157">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d0346-158">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="d0346-158">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="d0346-159">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="d0346-159">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="d0346-160">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="d0346-160">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="d0346-161">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="d0346-161">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="d0346-162">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0346-162">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d0346-163">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="d0346-163">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="d0346-164">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d0346-164">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="d0346-165">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="d0346-165">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="d0346-166">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="d0346-166">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="d0346-167">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d0346-167">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d0346-168">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d0346-168">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d0346-169">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="d0346-169">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="d0346-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0346-170">RELATED LINKS</span></span>
