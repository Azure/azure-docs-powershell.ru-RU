---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327645"
---
# <span data-ttu-id="dfc0d-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="dfc0d-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="dfc0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfc0d-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc0d-103">Получает указанную службу HSM Azure.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="dfc0d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dfc0d-104">SYNTAX</span></span>

### <span data-ttu-id="dfc0d-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfc0d-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="dfc0d-106">Получить</span><span class="sxs-lookup"><span data-stu-id="dfc0d-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dfc0d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dfc0d-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dfc0d-108">Список</span><span class="sxs-lookup"><span data-stu-id="dfc0d-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dfc0d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfc0d-109">DESCRIPTION</span></span>
<span data-ttu-id="dfc0d-110">Получает указанную службу HSM Azure.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="dfc0d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dfc0d-111">EXAMPLES</span></span>

### <span data-ttu-id="dfc0d-112">Пример 1. Получить весь выделенный HSM в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="dfc0d-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="dfc0d-113">Эта команда получает весь выделенный HSM в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="dfc0d-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="dfc0d-114">Пример 2. Получить весь выделенный HSM в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="dfc0d-115">Эта команда получает все выделенные HSM в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="dfc0d-116">Пример 3. Получить выделенную HSM по имени</span><span class="sxs-lookup"><span data-stu-id="dfc0d-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="dfc0d-117">Эта команда получает выделенную HSM по имени.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="dfc0d-118">Пример 4. Получить выделенную HSM-услугу по объекту</span><span class="sxs-lookup"><span data-stu-id="dfc0d-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="dfc0d-119">Эта команда получает выделенный HSM для объекта.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="dfc0d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfc0d-120">PARAMETERS</span></span>

### <span data-ttu-id="dfc0d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc0d-121">-DefaultProfile</span></span>
<span data-ttu-id="dfc0d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfc0d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfc0d-123">-InputObject</span></span>
<span data-ttu-id="dfc0d-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dfc0d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dfc0d-125">-Name</span></span>
<span data-ttu-id="dfc0d-126">Название выделенной HSM-части.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="dfc0d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfc0d-127">-ResourceGroupName</span></span>
<span data-ttu-id="dfc0d-128">Имя группы ресурсов, к которой принадлежит выделенный hsm.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="dfc0d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfc0d-129">-SubscriptionId</span></span>
<span data-ttu-id="dfc0d-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dfc0d-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dfc0d-132">-Top</span><span class="sxs-lookup"><span data-stu-id="dfc0d-132">-Top</span></span>
<span data-ttu-id="dfc0d-133">Максимальное количество возвращаемых результатов.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="dfc0d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc0d-134">CommonParameters</span></span>
<span data-ttu-id="dfc0d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc0d-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfc0d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc0d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfc0d-137">INPUTS</span></span>

### <span data-ttu-id="dfc0d-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="dfc0d-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="dfc0d-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dfc0d-139">OUTPUTS</span></span>

### <span data-ttu-id="dfc0d-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="dfc0d-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="dfc0d-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dfc0d-141">NOTES</span></span>

<span data-ttu-id="dfc0d-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dfc0d-142">ALIASES</span></span>

<span data-ttu-id="dfc0d-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="dfc0d-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dfc0d-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfc0d-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dfc0d-146">INPUTOBJECT <IDedicatedHsmIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="dfc0d-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dfc0d-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="dfc0d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dfc0d-148">`[Name <String>]`: название выделенного HSM</span><span class="sxs-lookup"><span data-stu-id="dfc0d-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="dfc0d-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="dfc0d-150">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dfc0d-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dfc0d-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfc0d-152">RELATED LINKS</span></span>

