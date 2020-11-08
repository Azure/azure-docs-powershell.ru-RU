---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236744"
---
# <span data-ttu-id="ca8ca-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="ca8ca-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="ca8ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca8ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8ca-103">Создайте или обновите Специальный HSM-аппарат в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="ca8ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca8ca-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ca8ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca8ca-105">DESCRIPTION</span></span>
<span data-ttu-id="ca8ca-106">Создайте или обновите Специальный HSM-аппарат в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="ca8ca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca8ca-107">EXAMPLES</span></span>

### <span data-ttu-id="ca8ca-108">Пример 1: создание выделенного HSM-кода в существующей виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ca8ca-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="ca8ca-109">Эта команда создает выделенный HSM-интерфейс в существующей виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="ca8ca-110">**Примечание.** В настоящее время `New-AzDedicatedHsm` она возвращает ограничение, после которого функция HSM будет полностью подготовлена в Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="ca8ca-111">Поэтому после создания нового HSM-микропрограммы запросите его состояние `Get-AzDedicatedHsm` и убедитесь, `Provisioning State` что `Succeeded` он не используется.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="ca8ca-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca8ca-112">PARAMETERS</span></span>

### <span data-ttu-id="ca8ca-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca8ca-113">-AsJob</span></span>
<span data-ttu-id="ca8ca-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ca8ca-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ca8ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8ca-115">-DefaultProfile</span></span>
<span data-ttu-id="ca8ca-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca8ca-117">-Location</span><span class="sxs-lookup"><span data-stu-id="ca8ca-117">-Location</span></span>
<span data-ttu-id="ca8ca-118">Расположение для Azure, в котором нужно создать выделенный HSM.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="ca8ca-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca8ca-119">-Name</span></span>
<span data-ttu-id="ca8ca-120">Имя выделенного HSM.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="ca8ca-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ca8ca-121">-NetworkInterface</span></span>
<span data-ttu-id="ca8ca-122">Указывает список идентификаторов ресурсов для сетевых интерфейсов, связанных с выделенным HSM.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="ca8ca-123">Для конструирования ознакомьтесь с разделом "Заметки" для свойств NETWORKINTERFACE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca8ca-124">-Wait</span><span class="sxs-lookup"><span data-stu-id="ca8ca-124">-NoWait</span></span>
<span data-ttu-id="ca8ca-125">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="ca8ca-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ca8ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca8ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca8ca-127">Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="ca8ca-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="ca8ca-128">-Sku</span></span>
<span data-ttu-id="ca8ca-129">SKU выделенного HSM</span><span class="sxs-lookup"><span data-stu-id="ca8ca-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="ca8ca-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="ca8ca-130">-StampId</span></span>
<span data-ttu-id="ca8ca-131">Это поле будет использоваться, когда RP не поддерживает зоны доступности.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="ca8ca-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ca8ca-132">-SubnetId</span></span>
<span data-ttu-id="ca8ca-133">Идентификатор ресурса ARM в форме/subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="ca8ca-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="ca8ca-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca8ca-134">-SubscriptionId</span></span>
<span data-ttu-id="ca8ca-135">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ca8ca-136">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ca8ca-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="ca8ca-137">-Tag</span></span>
<span data-ttu-id="ca8ca-138">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="ca8ca-138">Resource tags</span></span>

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

### <span data-ttu-id="ca8ca-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="ca8ca-139">-Zone</span></span>
<span data-ttu-id="ca8ca-140">Выделенные зоны HSM.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="ca8ca-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca8ca-141">-Confirm</span></span>
<span data-ttu-id="ca8ca-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca8ca-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8ca-143">-WhatIf</span></span>
<span data-ttu-id="ca8ca-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca8ca-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca8ca-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8ca-146">CommonParameters</span></span>
<span data-ttu-id="ca8ca-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8ca-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca8ca-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8ca-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca8ca-149">INPUTS</span></span>

## <span data-ttu-id="ca8ca-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca8ca-150">OUTPUTS</span></span>

### <span data-ttu-id="ca8ca-151">Microsoft. Azure. PowerShell. командлеты. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="ca8ca-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="ca8ca-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca8ca-152">NOTES</span></span>

<span data-ttu-id="ca8ca-153">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ca8ca-153">ALIASES</span></span>

<span data-ttu-id="ca8ca-154">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ca8ca-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca8ca-155">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca8ca-156">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca8ca-157">NETWORKINTERFACE <INetworkInterface [] >: указывает список идентификаторов ресурсов для сетевых интерфейсов, связанных с выделенным HSM.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="ca8ca-158">`[PrivateIPAddress <String>]`: Частный IP-адрес интерфейса</span><span class="sxs-lookup"><span data-stu-id="ca8ca-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="ca8ca-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca8ca-159">RELATED LINKS</span></span>

