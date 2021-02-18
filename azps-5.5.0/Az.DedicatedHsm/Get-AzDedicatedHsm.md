---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232097"
---
# <span data-ttu-id="724b3-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="724b3-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="724b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="724b3-102">SYNOPSIS</span></span>
<span data-ttu-id="724b3-103">Получает указанную службу HSM Azure.</span><span class="sxs-lookup"><span data-stu-id="724b3-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="724b3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="724b3-104">SYNTAX</span></span>

### <span data-ttu-id="724b3-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="724b3-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="724b3-106">Получить</span><span class="sxs-lookup"><span data-stu-id="724b3-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="724b3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="724b3-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="724b3-108">Список</span><span class="sxs-lookup"><span data-stu-id="724b3-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="724b3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="724b3-109">DESCRIPTION</span></span>
<span data-ttu-id="724b3-110">Получает указанную службу HSM Azure.</span><span class="sxs-lookup"><span data-stu-id="724b3-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="724b3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="724b3-111">EXAMPLES</span></span>

### <span data-ttu-id="724b3-112">Пример 1. Получить весь выделенный HSM в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="724b3-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="724b3-113">Эта команда получает весь выделенный HSM в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="724b3-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="724b3-114">Пример 2. Получить весь выделенный HSM в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="724b3-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="724b3-115">Эта команда получает весь выделенный HSM в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="724b3-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="724b3-116">Пример 3. Получить выделенную HSM по имени</span><span class="sxs-lookup"><span data-stu-id="724b3-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="724b3-117">Эта команда получает выделенную HSM по имени.</span><span class="sxs-lookup"><span data-stu-id="724b3-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="724b3-118">Пример 4. Получить выделенную HSM по объекту</span><span class="sxs-lookup"><span data-stu-id="724b3-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="724b3-119">Эта команда получает выделенный HSM для объекта.</span><span class="sxs-lookup"><span data-stu-id="724b3-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="724b3-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="724b3-120">PARAMETERS</span></span>

### <span data-ttu-id="724b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724b3-121">-DefaultProfile</span></span>
<span data-ttu-id="724b3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="724b3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="724b3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="724b3-123">-InputObject</span></span>
<span data-ttu-id="724b3-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="724b3-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="724b3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="724b3-125">-Name</span></span>
<span data-ttu-id="724b3-126">Название выделенной HSM-части.</span><span class="sxs-lookup"><span data-stu-id="724b3-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="724b3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="724b3-127">-ResourceGroupName</span></span>
<span data-ttu-id="724b3-128">Имя группы ресурсов, к которой принадлежит выделенный hsm.</span><span class="sxs-lookup"><span data-stu-id="724b3-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="724b3-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="724b3-129">-SubscriptionId</span></span>
<span data-ttu-id="724b3-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="724b3-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="724b3-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="724b3-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="724b3-132">-Top</span><span class="sxs-lookup"><span data-stu-id="724b3-132">-Top</span></span>
<span data-ttu-id="724b3-133">Максимальное количество возвращаемых результатов.</span><span class="sxs-lookup"><span data-stu-id="724b3-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="724b3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724b3-134">CommonParameters</span></span>
<span data-ttu-id="724b3-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="724b3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724b3-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="724b3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724b3-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="724b3-137">INPUTS</span></span>

### <span data-ttu-id="724b3-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="724b3-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="724b3-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="724b3-139">OUTPUTS</span></span>

### <span data-ttu-id="724b3-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="724b3-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="724b3-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="724b3-141">NOTES</span></span>

<span data-ttu-id="724b3-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="724b3-142">ALIASES</span></span>

<span data-ttu-id="724b3-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="724b3-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="724b3-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="724b3-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="724b3-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="724b3-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="724b3-146">INPUTOBJECT <IDedicatedHsmIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="724b3-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="724b3-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="724b3-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="724b3-148">`[Name <String>]`: название выделенного HSM</span><span class="sxs-lookup"><span data-stu-id="724b3-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="724b3-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="724b3-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="724b3-150">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="724b3-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="724b3-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="724b3-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="724b3-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="724b3-152">RELATED LINKS</span></span>

