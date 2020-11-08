---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244558"
---
# <span data-ttu-id="39d15-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="39d15-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="39d15-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39d15-102">SYNOPSIS</span></span>
<span data-ttu-id="39d15-103">Получает указанный специальный HSM службы Azure.</span><span class="sxs-lookup"><span data-stu-id="39d15-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="39d15-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39d15-104">SYNTAX</span></span>

### <span data-ttu-id="39d15-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39d15-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="39d15-106">Получить</span><span class="sxs-lookup"><span data-stu-id="39d15-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="39d15-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39d15-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="39d15-108">Список</span><span class="sxs-lookup"><span data-stu-id="39d15-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="39d15-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39d15-109">DESCRIPTION</span></span>
<span data-ttu-id="39d15-110">Получает указанный специальный HSM службы Azure.</span><span class="sxs-lookup"><span data-stu-id="39d15-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="39d15-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39d15-111">EXAMPLES</span></span>

### <span data-ttu-id="39d15-112">Пример 1: получение всех выделенных HSM-аппаратных продуктов в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="39d15-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="39d15-113">Эта команда получает все выделенные HSM-данные в подписке</span><span class="sxs-lookup"><span data-stu-id="39d15-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="39d15-114">Пример 2: получение всех выделенных HSM-аппаратных продуктов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39d15-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="39d15-115">Эта команда получает все выделенный HSM-список в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39d15-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="39d15-116">Пример 3: получение специального имени HSM</span><span class="sxs-lookup"><span data-stu-id="39d15-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="39d15-117">Эта команда получает выделенный HSM-объект по имени.</span><span class="sxs-lookup"><span data-stu-id="39d15-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="39d15-118">Пример 4: получение выделенного HSM-кода с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="39d15-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="39d15-119">Эта команда получает выделенный HSM-объект по объекту.</span><span class="sxs-lookup"><span data-stu-id="39d15-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="39d15-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39d15-120">PARAMETERS</span></span>

### <span data-ttu-id="39d15-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d15-121">-DefaultProfile</span></span>
<span data-ttu-id="39d15-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39d15-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d15-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39d15-123">-InputObject</span></span>
<span data-ttu-id="39d15-124">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="39d15-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="39d15-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="39d15-125">-Name</span></span>
<span data-ttu-id="39d15-126">Имя выделенного HSM.</span><span class="sxs-lookup"><span data-stu-id="39d15-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="39d15-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d15-127">-ResourceGroupName</span></span>
<span data-ttu-id="39d15-128">Имя группы ресурсов, к которой принадлежит выделенный HSM.</span><span class="sxs-lookup"><span data-stu-id="39d15-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="39d15-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39d15-129">-SubscriptionId</span></span>
<span data-ttu-id="39d15-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="39d15-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="39d15-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="39d15-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="39d15-132">-Top</span><span class="sxs-lookup"><span data-stu-id="39d15-132">-Top</span></span>
<span data-ttu-id="39d15-133">Максимальное количество возвращаемых результатов.</span><span class="sxs-lookup"><span data-stu-id="39d15-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="39d15-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d15-134">CommonParameters</span></span>
<span data-ttu-id="39d15-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39d15-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d15-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39d15-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d15-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39d15-137">INPUTS</span></span>

### <span data-ttu-id="39d15-138">Microsoft. Azure. PowerShell. командлеты. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="39d15-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="39d15-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39d15-139">OUTPUTS</span></span>

### <span data-ttu-id="39d15-140">Microsoft. Azure. PowerShell. командлеты. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="39d15-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="39d15-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="39d15-141">NOTES</span></span>

<span data-ttu-id="39d15-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="39d15-142">ALIASES</span></span>

<span data-ttu-id="39d15-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="39d15-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39d15-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="39d15-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39d15-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39d15-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39d15-146">INPUTOBJECT <IDedicatedHsmIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="39d15-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39d15-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="39d15-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39d15-148">`[Name <String>]`: Имя выделенного HSM.</span><span class="sxs-lookup"><span data-stu-id="39d15-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="39d15-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="39d15-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="39d15-150">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="39d15-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="39d15-151">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="39d15-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="39d15-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39d15-152">RELATED LINKS</span></span>

