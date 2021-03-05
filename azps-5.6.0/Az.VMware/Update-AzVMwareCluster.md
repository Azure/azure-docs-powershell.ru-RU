---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: f708d1b752c0d8106d7a8f9f7613fa74b6b19937
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988588"
---
# <span data-ttu-id="5eb4d-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="5eb4d-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="5eb4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eb4d-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb4d-103">Обновление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="5eb4d-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="5eb4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5eb4d-104">SYNTAX</span></span>

### <span data-ttu-id="5eb4d-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5eb4d-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5eb4d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5eb4d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5eb4d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5eb4d-107">DESCRIPTION</span></span>
<span data-ttu-id="5eb4d-108">Обновление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="5eb4d-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="5eb4d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5eb4d-109">EXAMPLES</span></span>

### <span data-ttu-id="5eb4d-110">Пример 1. Обновление размера кластера по имени</span><span class="sxs-lookup"><span data-stu-id="5eb4d-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="5eb4d-111">Обновление размера кластера по имени</span><span class="sxs-lookup"><span data-stu-id="5eb4d-111">Update cluster size by name</span></span>

### <span data-ttu-id="5eb4d-112">Пример 2. Обновление размера кластера по входным объектам</span><span class="sxs-lookup"><span data-stu-id="5eb4d-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="5eb4d-113">Обновление размера кластера по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="5eb4d-113">Update cluster size by input object</span></span>

## <span data-ttu-id="5eb4d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5eb4d-114">PARAMETERS</span></span>

### <span data-ttu-id="5eb4d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5eb4d-115">-AsJob</span></span>
<span data-ttu-id="5eb4d-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="5eb4d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5eb4d-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="5eb4d-117">-ClusterSize</span></span>
<span data-ttu-id="5eb4d-118">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="5eb4d-118">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb4d-119">-DefaultProfile</span></span>
<span data-ttu-id="5eb4d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eb4d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eb4d-121">-InputObject</span></span>
<span data-ttu-id="5eb4d-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb4d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5eb4d-123">-Name</span></span>
<span data-ttu-id="5eb4d-124">Название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="5eb4d-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb4d-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5eb4d-125">-NoWait</span></span>
<span data-ttu-id="5eb4d-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="5eb4d-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5eb4d-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="5eb4d-127">-PrivateCloudName</span></span>
<span data-ttu-id="5eb4d-128">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="5eb4d-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb4d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb4d-129">-ResourceGroupName</span></span>
<span data-ttu-id="5eb4d-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-130">The name of the resource group.</span></span>
<span data-ttu-id="5eb4d-131">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb4d-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5eb4d-132">-SubscriptionId</span></span>
<span data-ttu-id="5eb4d-133">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb4d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5eb4d-134">-Confirm</span></span>
<span data-ttu-id="5eb4d-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eb4d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eb4d-136">-WhatIf</span></span>
<span data-ttu-id="5eb4d-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eb4d-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eb4d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb4d-139">CommonParameters</span></span>
<span data-ttu-id="5eb4d-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb4d-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5eb4d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb4d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5eb4d-142">INPUTS</span></span>

### <span data-ttu-id="5eb4d-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="5eb4d-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="5eb4d-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5eb4d-144">OUTPUTS</span></span>

### <span data-ttu-id="5eb4d-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="5eb4d-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="5eb4d-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5eb4d-146">NOTES</span></span>

<span data-ttu-id="5eb4d-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5eb4d-147">ALIASES</span></span>

<span data-ttu-id="5eb4d-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5eb4d-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5eb4d-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5eb4d-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5eb4d-151">INPUTOBJECT <IVMWareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="5eb4d-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5eb4d-152">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="5eb4d-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="5eb4d-153">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="5eb4d-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="5eb4d-154">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="5eb4d-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="5eb4d-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="5eb4d-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5eb4d-156">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="5eb4d-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="5eb4d-157">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="5eb4d-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="5eb4d-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5eb4d-159">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="5eb4d-160">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5eb4d-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="5eb4d-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5eb4d-161">RELATED LINKS</span></span>

