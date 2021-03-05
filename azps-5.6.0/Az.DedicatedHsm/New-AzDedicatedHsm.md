---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: 9d2d1ee1dd17b9d1783ba267b2f656be6adce05b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966376"
---
# <span data-ttu-id="f42c9-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="f42c9-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="f42c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f42c9-102">SYNOPSIS</span></span>
<span data-ttu-id="f42c9-103">Создание или обновление выделенной службы HSM в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="f42c9-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="f42c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f42c9-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f42c9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f42c9-105">DESCRIPTION</span></span>
<span data-ttu-id="f42c9-106">Создание или обновление выделенной службы HSM в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="f42c9-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="f42c9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f42c9-107">EXAMPLES</span></span>

### <span data-ttu-id="f42c9-108">Пример 1. Создание выделенной системы HSM в существующей виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f42c9-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="f42c9-109">Эта команда создает выделенную HSM в существующую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="f42c9-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="f42c9-110">**ПРИМЕЧАНИЕ.** В настоящее время существует ограничение, которое возвращается до полного предоставления `New-AzDedicatedHsm` службы HSM в Azure.</span><span class="sxs-lookup"><span data-stu-id="f42c9-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="f42c9-111">Поэтому после создания HSM следует запросить состояние системы и убедиться в том, что она `Get-AzDedicatedHsm` `Provisioning State` находится перед `Succeeded` использованием.</span><span class="sxs-lookup"><span data-stu-id="f42c9-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="f42c9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f42c9-112">PARAMETERS</span></span>

### <span data-ttu-id="f42c9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f42c9-113">-AsJob</span></span>
<span data-ttu-id="f42c9-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f42c9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f42c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f42c9-115">-DefaultProfile</span></span>
<span data-ttu-id="f42c9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f42c9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f42c9-117">-Location</span><span class="sxs-lookup"><span data-stu-id="f42c9-117">-Location</span></span>
<span data-ttu-id="f42c9-118">Поддерживаемая служба Azure, в которой нужно создать выделенную службу поддержки HSM.</span><span class="sxs-lookup"><span data-stu-id="f42c9-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="f42c9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f42c9-119">-Name</span></span>
<span data-ttu-id="f42c9-120">Название выделенного HSM</span><span class="sxs-lookup"><span data-stu-id="f42c9-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="f42c9-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f42c9-121">-NetworkInterface</span></span>
<span data-ttu-id="f42c9-122">Определяет список ИД ресурсов для сетевых интерфейсов, связанных со выделенной службой управления (HSM).</span><span class="sxs-lookup"><span data-stu-id="f42c9-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="f42c9-123">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств NETWORKINTERFACE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="f42c9-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f42c9-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f42c9-124">-NoWait</span></span>
<span data-ttu-id="f42c9-125">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="f42c9-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f42c9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f42c9-126">-ResourceGroupName</span></span>
<span data-ttu-id="f42c9-127">Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="f42c9-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="f42c9-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="f42c9-128">-Sku</span></span>
<span data-ttu-id="f42c9-129">SKU выделенной HSM</span><span class="sxs-lookup"><span data-stu-id="f42c9-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="f42c9-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="f42c9-130">-StampId</span></span>
<span data-ttu-id="f42c9-131">Это поле будет использоваться, если зоны доступности не поддерживаются средством "RP".</span><span class="sxs-lookup"><span data-stu-id="f42c9-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="f42c9-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f42c9-132">-SubnetId</span></span>
<span data-ttu-id="f42c9-133">Код ARM ресурса в формате /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="f42c9-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="f42c9-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f42c9-134">-SubscriptionId</span></span>
<span data-ttu-id="f42c9-135">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f42c9-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f42c9-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="f42c9-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f42c9-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="f42c9-137">-Tag</span></span>
<span data-ttu-id="f42c9-138">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="f42c9-138">Resource tags</span></span>

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

### <span data-ttu-id="f42c9-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="f42c9-139">-Zone</span></span>
<span data-ttu-id="f42c9-140">Выделенные зоны HSM.</span><span class="sxs-lookup"><span data-stu-id="f42c9-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="f42c9-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f42c9-141">-Confirm</span></span>
<span data-ttu-id="f42c9-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f42c9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f42c9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f42c9-143">-WhatIf</span></span>
<span data-ttu-id="f42c9-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f42c9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f42c9-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f42c9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f42c9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f42c9-146">CommonParameters</span></span>
<span data-ttu-id="f42c9-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f42c9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f42c9-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f42c9-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f42c9-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f42c9-149">INPUTS</span></span>

## <span data-ttu-id="f42c9-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f42c9-150">OUTPUTS</span></span>

### <span data-ttu-id="f42c9-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="f42c9-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="f42c9-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f42c9-152">NOTES</span></span>

<span data-ttu-id="f42c9-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f42c9-153">ALIASES</span></span>

<span data-ttu-id="f42c9-154">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f42c9-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f42c9-155">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f42c9-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f42c9-156">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f42c9-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f42c9-157">NETWORKINTERFACE <INetworkInterface[]>: определяет список ИД ресурсов для сетевых интерфейсов, связанных со выделенным HSM.</span><span class="sxs-lookup"><span data-stu-id="f42c9-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="f42c9-158">`[PrivateIPAddress <String>]`: личный IP-адрес интерфейса</span><span class="sxs-lookup"><span data-stu-id="f42c9-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="f42c9-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f42c9-159">RELATED LINKS</span></span>

