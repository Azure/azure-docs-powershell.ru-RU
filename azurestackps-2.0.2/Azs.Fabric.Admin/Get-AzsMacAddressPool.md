---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsmacaddresspool
schema: 2.0.0
ms.openlocfilehash: f7a2ae035ff0985c84dc78a18131c46239bafd1f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076661"
---
# <span data-ttu-id="ccb3b-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="ccb3b-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="ccb3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ccb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb3b-103">Возвращает требуемый пул MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-103">Returns the requested MAC address pool.</span></span>

## <span data-ttu-id="ccb3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ccb3b-104">SYNTAX</span></span>

### <span data-ttu-id="ccb3b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ccb3b-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ccb3b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="ccb3b-106">Get</span></span>
```
Get-AzsMacAddressPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ccb3b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ccb3b-107">GetViaIdentity</span></span>
```
Get-AzsMacAddressPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="ccb3b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccb3b-108">DESCRIPTION</span></span>
<span data-ttu-id="ccb3b-109">Возвращает требуемый пул MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-109">Returns the requested MAC address pool.</span></span>

## <span data-ttu-id="ccb3b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ccb3b-110">EXAMPLES</span></span>

### <span data-ttu-id="ccb3b-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="ccb3b-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsMacAddressPool

A list of all MAC address pools at a location.
```

<span data-ttu-id="ccb3b-112">Возвращает список всех пулов MAC-адресов в местоположении.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-112">Returns a list of all MAC address pools at a location.</span></span>

### <span data-ttu-id="ccb3b-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="ccb3b-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"

A specific MAC address pool at a location based on name.
```

<span data-ttu-id="ccb3b-114">Получение определенного пула MAC-адресов в местоположении на основе имени.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="ccb3b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ccb3b-115">PARAMETERS</span></span>

### <span data-ttu-id="ccb3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb3b-116">-DefaultProfile</span></span>
<span data-ttu-id="ccb3b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccb3b-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="ccb3b-118">-Filter</span></span>
<span data-ttu-id="ccb3b-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="ccb3b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccb3b-120">-InputObject</span></span>
<span data-ttu-id="ccb3b-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ccb3b-122">-Location</span><span class="sxs-lookup"><span data-stu-id="ccb3b-122">-Location</span></span>
<span data-ttu-id="ccb3b-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-123">Location of the resource.</span></span>

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

### <span data-ttu-id="ccb3b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ccb3b-124">-Name</span></span>
<span data-ttu-id="ccb3b-125">Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-125">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="ccb3b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccb3b-126">-PassThru</span></span>
<span data-ttu-id="ccb3b-127">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ccb3b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccb3b-128">-ResourceGroupName</span></span>
<span data-ttu-id="ccb3b-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="ccb3b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ccb3b-130">-SubscriptionId</span></span>
<span data-ttu-id="ccb3b-131">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ccb3b-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ccb3b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb3b-133">CommonParameters</span></span>
<span data-ttu-id="ccb3b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb3b-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccb3b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb3b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ccb3b-136">INPUTS</span></span>

### <span data-ttu-id="ccb3b-137">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ccb3b-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="ccb3b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccb3b-138">OUTPUTS</span></span>

### <span data-ttu-id="ccb3b-139">Microsoft. Azure. PowerShell. командлеты. FabricAdmin. Models. Api20160501. IMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="ccb3b-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IMacAddressPool</span></span>



## <span data-ttu-id="ccb3b-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="ccb3b-140">NOTES</span></span>

<span data-ttu-id="ccb3b-141">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ccb3b-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ccb3b-143">INPUTOBJECT <IFabricAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="ccb3b-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ccb3b-144">`[Drive <String>]`: Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="ccb3b-145">`[EdgeGateway <String>]`: Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="ccb3b-146">`[EdgeGatewayPool <String>]`: Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="ccb3b-147">`[FabricLocation <String>]`: Расположение в структуре.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="ccb3b-148">`[FileShare <String>]`: Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="ccb3b-149">`[IPPool <String>]`: Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="ccb3b-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="ccb3b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ccb3b-151">`[InfraRole <String>]`: Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="ccb3b-152">`[InfraRoleInstance <String>]`: Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="ccb3b-153">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ccb3b-154">`[LogicalNetwork <String>]`: Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="ccb3b-155">`[LogicalSubnet <String>]`: Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="ccb3b-156">`[MacAddressPool <String>]`: Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="ccb3b-157">`[Operation <String>]`: Идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="ccb3b-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ccb3b-159">`[ScaleUnit <String>]`: Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="ccb3b-160">`[ScaleUnitNode <String>]`: Имя узла единица масштабирования.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="ccb3b-161">`[SlbMuxInstance <String>]`: Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="ccb3b-162">`[StoragePool <String>]`: Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="ccb3b-163">`[StorageSubSystem <String>]`: Имя системы хранения.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="ccb3b-164">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ccb3b-165">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ccb3b-166">`[Volume <String>]`: Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="ccb3b-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="ccb3b-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccb3b-167">RELATED LINKS</span></span>

