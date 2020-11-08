---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077443"
---
# <span data-ttu-id="aef89-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="aef89-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="aef89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aef89-102">SYNOPSIS</span></span>
<span data-ttu-id="aef89-103">Обновление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="aef89-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="aef89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aef89-104">SYNTAX</span></span>

### <span data-ttu-id="aef89-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aef89-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aef89-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="aef89-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aef89-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aef89-107">DESCRIPTION</span></span>
<span data-ttu-id="aef89-108">Обновление кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="aef89-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="aef89-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aef89-109">EXAMPLES</span></span>

### <span data-ttu-id="aef89-110">Пример 1: Обновление размера кластера по названию</span><span class="sxs-lookup"><span data-stu-id="aef89-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="aef89-111">Обновление размера кластера по названию</span><span class="sxs-lookup"><span data-stu-id="aef89-111">Update cluster size by name</span></span>

### <span data-ttu-id="aef89-112">Пример 2: Обновление размера кластера по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="aef89-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="aef89-113">Обновление размера кластера по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="aef89-113">Update cluster size by input object</span></span>

## <span data-ttu-id="aef89-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aef89-114">PARAMETERS</span></span>

### <span data-ttu-id="aef89-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aef89-115">-AsJob</span></span>
<span data-ttu-id="aef89-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="aef89-116">Run the command as a job</span></span>

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

### <span data-ttu-id="aef89-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="aef89-117">-ClusterSize</span></span>
<span data-ttu-id="aef89-118">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="aef89-118">The cluster size</span></span>

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

### <span data-ttu-id="aef89-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef89-119">-DefaultProfile</span></span>
<span data-ttu-id="aef89-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aef89-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aef89-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aef89-121">-InputObject</span></span>
<span data-ttu-id="aef89-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="aef89-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aef89-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aef89-123">-Name</span></span>
<span data-ttu-id="aef89-124">Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="aef89-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="aef89-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="aef89-125">-NoWait</span></span>
<span data-ttu-id="aef89-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="aef89-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aef89-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="aef89-127">-PrivateCloudName</span></span>
<span data-ttu-id="aef89-128">Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="aef89-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="aef89-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aef89-129">-ResourceGroupName</span></span>
<span data-ttu-id="aef89-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aef89-130">The name of the resource group.</span></span>
<span data-ttu-id="aef89-131">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="aef89-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="aef89-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aef89-132">-SubscriptionId</span></span>
<span data-ttu-id="aef89-133">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="aef89-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="aef89-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aef89-134">-Confirm</span></span>
<span data-ttu-id="aef89-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aef89-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aef89-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aef89-136">-WhatIf</span></span>
<span data-ttu-id="aef89-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aef89-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aef89-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aef89-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aef89-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef89-139">CommonParameters</span></span>
<span data-ttu-id="aef89-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aef89-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef89-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aef89-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef89-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aef89-142">INPUTS</span></span>

### <span data-ttu-id="aef89-143">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="aef89-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="aef89-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aef89-144">OUTPUTS</span></span>

### <span data-ttu-id="aef89-145">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="aef89-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="aef89-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="aef89-146">NOTES</span></span>

<span data-ttu-id="aef89-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="aef89-147">ALIASES</span></span>

<span data-ttu-id="aef89-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="aef89-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aef89-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="aef89-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aef89-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aef89-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aef89-151">INPUTOBJECT <IVMWareIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="aef89-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aef89-152">`[AuthorizationName <String>]`: Имя авторизации канала ExpressRoute в частном облаке.</span><span class="sxs-lookup"><span data-stu-id="aef89-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="aef89-153">`[ClusterName <String>]`: Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="aef89-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="aef89-154">`[HcxEnterpriseSiteName <String>]`: Имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="aef89-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="aef89-155">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="aef89-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aef89-156">`[Location <String>]`: Регион Azure</span><span class="sxs-lookup"><span data-stu-id="aef89-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="aef89-157">`[PrivateCloudName <String>]`: Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="aef89-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="aef89-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aef89-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aef89-159">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="aef89-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="aef89-160">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="aef89-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="aef89-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aef89-161">RELATED LINKS</span></span>

