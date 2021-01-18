---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516905"
---
# <span data-ttu-id="3f62a-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="3f62a-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="3f62a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f62a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f62a-103">Создание или обновление выделенной службы HSM в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="3f62a-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="3f62a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f62a-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3f62a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f62a-105">DESCRIPTION</span></span>
<span data-ttu-id="3f62a-106">Создание или обновление выделенной службы HSM в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="3f62a-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="3f62a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f62a-107">EXAMPLES</span></span>

### <span data-ttu-id="3f62a-108">Пример 1. Создание выделенной системы HSM в существующей виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3f62a-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="3f62a-109">Эта команда создает специальную HSM в существующую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="3f62a-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="3f62a-110">**ПРИМЕЧАНИЕ.** В настоящее время существует ограничение, которое возвращается до полного предоставления `New-AzDedicatedHsm` службы HSM в Azure.</span><span class="sxs-lookup"><span data-stu-id="3f62a-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="3f62a-111">Поэтому после создания HSM следует запросить состояние системы и убедиться в том, что она `Get-AzDedicatedHsm` `Provisioning State` находится перед `Succeeded` использованием.</span><span class="sxs-lookup"><span data-stu-id="3f62a-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="3f62a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f62a-112">PARAMETERS</span></span>

### <span data-ttu-id="3f62a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f62a-113">-AsJob</span></span>
<span data-ttu-id="3f62a-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3f62a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3f62a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f62a-115">-DefaultProfile</span></span>
<span data-ttu-id="3f62a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f62a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f62a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3f62a-117">-Location</span></span>
<span data-ttu-id="3f62a-118">Поддерживаемая служба Azure, в которой нужно создать выделенную службу поддержки HSM.</span><span class="sxs-lookup"><span data-stu-id="3f62a-118">The supported Azure location where the dedicated HSM should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3f62a-119">-Name</span></span>
<span data-ttu-id="3f62a-120">Название выделенного HSM</span><span class="sxs-lookup"><span data-stu-id="3f62a-120">Name of the dedicated Hsm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3f62a-121">-NetworkInterface</span></span>
<span data-ttu-id="3f62a-122">Определяет список ИД ресурсов для сетевых интерфейсов, связанных со выделенной службой управления (HSM).</span><span class="sxs-lookup"><span data-stu-id="3f62a-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="3f62a-123">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств NETWORKINTERFACE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3f62a-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.INetworkInterface[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3f62a-124">-NoWait</span></span>
<span data-ttu-id="3f62a-125">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="3f62a-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3f62a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f62a-126">-ResourceGroupName</span></span>
<span data-ttu-id="3f62a-127">Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="3f62a-127">The name of the Resource Group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="3f62a-128">-Sku</span></span>
<span data-ttu-id="3f62a-129">SKU выделенной HSM</span><span class="sxs-lookup"><span data-stu-id="3f62a-129">SKU of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="3f62a-130">-StampId</span></span>
<span data-ttu-id="3f62a-131">Это поле будет использоваться, если зоны доступности не поддерживаются средством "RP".</span><span class="sxs-lookup"><span data-stu-id="3f62a-131">This field will be used when RP does not support Availability zones.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3f62a-132">-SubnetId</span></span>
<span data-ttu-id="3f62a-133">Код ARM ресурса в формате /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="3f62a-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f62a-134">-SubscriptionId</span></span>
<span data-ttu-id="3f62a-135">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f62a-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3f62a-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="3f62a-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f62a-137">-Tag</span></span>
<span data-ttu-id="3f62a-138">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f62a-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="3f62a-139">-Zone</span></span>
<span data-ttu-id="3f62a-140">Зоны Dedicated HSM.</span><span class="sxs-lookup"><span data-stu-id="3f62a-140">The Dedicated Hsm zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f62a-141">-Confirm</span></span>
<span data-ttu-id="3f62a-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f62a-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f62a-143">-WhatIf</span></span>
<span data-ttu-id="3f62a-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f62a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f62a-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f62a-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f62a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f62a-146">CommonParameters</span></span>
<span data-ttu-id="3f62a-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f62a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f62a-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f62a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f62a-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f62a-149">INPUTS</span></span>

## <span data-ttu-id="3f62a-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f62a-150">OUTPUTS</span></span>

### <span data-ttu-id="3f62a-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="3f62a-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="3f62a-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f62a-152">NOTES</span></span>

<span data-ttu-id="3f62a-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3f62a-153">ALIASES</span></span>

<span data-ttu-id="3f62a-154">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3f62a-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f62a-155">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3f62a-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f62a-156">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3f62a-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f62a-157">NETWORKINTERFACE <INetworkInterface[]>: определяет список ИД ресурсов для сетевых интерфейсов, связанных со выделенным HSM.</span><span class="sxs-lookup"><span data-stu-id="3f62a-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="3f62a-158">`[PrivateIPAddress <String>]`: личный IP-адрес интерфейса</span><span class="sxs-lookup"><span data-stu-id="3f62a-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="3f62a-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f62a-159">RELATED LINKS</span></span>

