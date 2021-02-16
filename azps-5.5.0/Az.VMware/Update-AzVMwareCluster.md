---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: cfe9a8aa16803433055eb0cec5993cedcbcb5874
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216596"
---
# <span data-ttu-id="1ec71-101">Update-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="1ec71-101">Update-AzVMwareCluster</span></span>

## <span data-ttu-id="1ec71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ec71-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec71-103">Обновление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="1ec71-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="1ec71-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ec71-104">SYNTAX</span></span>

### <span data-ttu-id="1ec71-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1ec71-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1ec71-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1ec71-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwareCluster -InputObject <IVMwareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ec71-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ec71-107">DESCRIPTION</span></span>
<span data-ttu-id="1ec71-108">Обновление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="1ec71-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="1ec71-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ec71-109">EXAMPLES</span></span>

### <span data-ttu-id="1ec71-110">Пример 1. Обновление размера кластера по имени</span><span class="sxs-lookup"><span data-stu-id="1ec71-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="1ec71-111">Обновление размера кластера по имени</span><span class="sxs-lookup"><span data-stu-id="1ec71-111">Update cluster size by name</span></span>

### <span data-ttu-id="1ec71-112">Пример 2. Обновление размера кластера по входным объектам</span><span class="sxs-lookup"><span data-stu-id="1ec71-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMwareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="1ec71-113">Обновление размера кластера по входным объектам</span><span class="sxs-lookup"><span data-stu-id="1ec71-113">Update cluster size by input object</span></span>

## <span data-ttu-id="1ec71-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ec71-114">PARAMETERS</span></span>

### <span data-ttu-id="1ec71-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ec71-115">-AsJob</span></span>
<span data-ttu-id="1ec71-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="1ec71-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1ec71-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="1ec71-117">-ClusterSize</span></span>
<span data-ttu-id="1ec71-118">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="1ec71-118">The cluster size</span></span>

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

### <span data-ttu-id="1ec71-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec71-119">-DefaultProfile</span></span>
<span data-ttu-id="1ec71-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec71-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec71-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ec71-121">-InputObject</span></span>
<span data-ttu-id="1ec71-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="1ec71-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec71-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1ec71-123">-Name</span></span>
<span data-ttu-id="1ec71-124">Название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="1ec71-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="1ec71-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1ec71-125">-NoWait</span></span>
<span data-ttu-id="1ec71-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="1ec71-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1ec71-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="1ec71-127">-PrivateCloudName</span></span>
<span data-ttu-id="1ec71-128">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="1ec71-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="1ec71-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec71-129">-ResourceGroupName</span></span>
<span data-ttu-id="1ec71-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ec71-130">The name of the resource group.</span></span>
<span data-ttu-id="1ec71-131">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="1ec71-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1ec71-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ec71-132">-SubscriptionId</span></span>
<span data-ttu-id="1ec71-133">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1ec71-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1ec71-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ec71-134">-Confirm</span></span>
<span data-ttu-id="1ec71-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec71-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec71-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec71-136">-WhatIf</span></span>
<span data-ttu-id="1ec71-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec71-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec71-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1ec71-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec71-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec71-139">CommonParameters</span></span>
<span data-ttu-id="1ec71-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec71-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec71-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ec71-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec71-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ec71-142">INPUTS</span></span>

### <span data-ttu-id="1ec71-143">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="1ec71-143">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="1ec71-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ec71-144">OUTPUTS</span></span>

### <span data-ttu-id="1ec71-145">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="1ec71-145">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="1ec71-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ec71-146">NOTES</span></span>

<span data-ttu-id="1ec71-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1ec71-147">ALIASES</span></span>

<span data-ttu-id="1ec71-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1ec71-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ec71-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="1ec71-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ec71-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1ec71-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ec71-151">INPUTOBJECT <IVMwareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="1ec71-151">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ec71-152">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="1ec71-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="1ec71-153">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="1ec71-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="1ec71-154">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="1ec71-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="1ec71-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="1ec71-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ec71-156">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="1ec71-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="1ec71-157">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="1ec71-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="1ec71-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ec71-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1ec71-159">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="1ec71-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="1ec71-160">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1ec71-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1ec71-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ec71-161">RELATED LINKS</span></span>

