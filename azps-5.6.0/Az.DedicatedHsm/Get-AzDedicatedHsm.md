---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: b4e00745655be6eb050141bb04dcef4797bde256
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966408"
---
# <span data-ttu-id="aaf26-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="aaf26-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="aaf26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaf26-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf26-103">Получает указанную службу HSM Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf26-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="aaf26-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aaf26-104">SYNTAX</span></span>

### <span data-ttu-id="aaf26-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aaf26-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="aaf26-106">Получить</span><span class="sxs-lookup"><span data-stu-id="aaf26-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aaf26-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aaf26-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aaf26-108">Список</span><span class="sxs-lookup"><span data-stu-id="aaf26-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="aaf26-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaf26-109">DESCRIPTION</span></span>
<span data-ttu-id="aaf26-110">Получает указанную службу HSM Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf26-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="aaf26-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aaf26-111">EXAMPLES</span></span>

### <span data-ttu-id="aaf26-112">Пример 1. Получить весь выделенный HSM в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="aaf26-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="aaf26-113">Эта команда получает весь выделенный HSM в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="aaf26-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="aaf26-114">Пример 2. Получить весь выделенный HSM в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aaf26-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="aaf26-115">Эта команда получает весь выделенный HSM в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aaf26-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="aaf26-116">Пример 3. Получить выделенную HSM по имени</span><span class="sxs-lookup"><span data-stu-id="aaf26-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="aaf26-117">Эта команда получает выделенную HSM по имени.</span><span class="sxs-lookup"><span data-stu-id="aaf26-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="aaf26-118">Пример 4. Получить выделенную HSM-услугу по объекту</span><span class="sxs-lookup"><span data-stu-id="aaf26-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="aaf26-119">Эта команда получает выделенный HSM-объект.</span><span class="sxs-lookup"><span data-stu-id="aaf26-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="aaf26-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaf26-120">PARAMETERS</span></span>

### <span data-ttu-id="aaf26-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf26-121">-DefaultProfile</span></span>
<span data-ttu-id="aaf26-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf26-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaf26-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaf26-123">-InputObject</span></span>
<span data-ttu-id="aaf26-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="aaf26-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaf26-125">-Name</span><span class="sxs-lookup"><span data-stu-id="aaf26-125">-Name</span></span>
<span data-ttu-id="aaf26-126">Название выделенной HSM-части.</span><span class="sxs-lookup"><span data-stu-id="aaf26-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="aaf26-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf26-127">-ResourceGroupName</span></span>
<span data-ttu-id="aaf26-128">Имя группы ресурсов, к которой принадлежит выделенный hsm.</span><span class="sxs-lookup"><span data-stu-id="aaf26-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="aaf26-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aaf26-129">-SubscriptionId</span></span>
<span data-ttu-id="aaf26-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf26-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aaf26-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="aaf26-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf26-132">-Top</span><span class="sxs-lookup"><span data-stu-id="aaf26-132">-Top</span></span>
<span data-ttu-id="aaf26-133">Максимальное количество возвращаемых результатов.</span><span class="sxs-lookup"><span data-stu-id="aaf26-133">Maximum number of results to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf26-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf26-134">CommonParameters</span></span>
<span data-ttu-id="aaf26-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf26-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf26-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aaf26-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf26-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaf26-137">INPUTS</span></span>

### <span data-ttu-id="aaf26-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="aaf26-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="aaf26-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aaf26-139">OUTPUTS</span></span>

### <span data-ttu-id="aaf26-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="aaf26-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="aaf26-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aaf26-141">NOTES</span></span>

<span data-ttu-id="aaf26-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="aaf26-142">ALIASES</span></span>

<span data-ttu-id="aaf26-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="aaf26-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aaf26-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="aaf26-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aaf26-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aaf26-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aaf26-146">INPUTOBJECT <IDedicatedHsmIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="aaf26-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aaf26-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="aaf26-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aaf26-148">`[Name <String>]`: название выделенного HSM</span><span class="sxs-lookup"><span data-stu-id="aaf26-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="aaf26-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="aaf26-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="aaf26-150">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf26-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="aaf26-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="aaf26-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="aaf26-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaf26-152">RELATED LINKS</span></span>

