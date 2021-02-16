---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 51a889abe0d1842f66a0ed9b17f3b07acd85a54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242968"
---
# <span data-ttu-id="36971-101">Get-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="36971-101">Get-AzVMwareCluster</span></span>

## <span data-ttu-id="36971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36971-102">SYNOPSIS</span></span>
<span data-ttu-id="36971-103">Получить кластер по имени в частном облаке</span><span class="sxs-lookup"><span data-stu-id="36971-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="36971-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36971-104">SYNTAX</span></span>

### <span data-ttu-id="36971-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36971-105">List (Default)</span></span>
```
Get-AzVMwareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36971-106">Получить</span><span class="sxs-lookup"><span data-stu-id="36971-106">Get</span></span>
```
Get-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36971-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="36971-107">GetViaIdentity</span></span>
```
Get-AzVMwareCluster -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="36971-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36971-108">DESCRIPTION</span></span>
<span data-ttu-id="36971-109">Получить кластер по имени в частном облаке</span><span class="sxs-lookup"><span data-stu-id="36971-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="36971-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36971-110">EXAMPLES</span></span>

### <span data-ttu-id="36971-111">Пример 1. Получить кластер</span><span class="sxs-lookup"><span data-stu-id="36971-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="36971-112">Получить кластер</span><span class="sxs-lookup"><span data-stu-id="36971-112">Get cluster</span></span>

### <span data-ttu-id="36971-113">Пример 2. Кластеры списков</span><span class="sxs-lookup"><span data-stu-id="36971-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="36971-114">Кластеры списков</span><span class="sxs-lookup"><span data-stu-id="36971-114">List clusters</span></span>

## <span data-ttu-id="36971-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36971-115">PARAMETERS</span></span>

### <span data-ttu-id="36971-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36971-116">-DefaultProfile</span></span>
<span data-ttu-id="36971-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36971-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36971-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36971-118">-InputObject</span></span>
<span data-ttu-id="36971-119">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="36971-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36971-120">-Name</span><span class="sxs-lookup"><span data-stu-id="36971-120">-Name</span></span>
<span data-ttu-id="36971-121">Название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="36971-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36971-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="36971-122">-PrivateCloudName</span></span>
<span data-ttu-id="36971-123">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="36971-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="36971-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36971-124">-ResourceGroupName</span></span>
<span data-ttu-id="36971-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36971-125">The name of the resource group.</span></span>
<span data-ttu-id="36971-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="36971-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="36971-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36971-127">-SubscriptionId</span></span>
<span data-ttu-id="36971-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="36971-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36971-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36971-129">CommonParameters</span></span>
<span data-ttu-id="36971-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36971-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36971-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36971-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36971-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36971-132">INPUTS</span></span>

### <span data-ttu-id="36971-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="36971-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="36971-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36971-134">OUTPUTS</span></span>

### <span data-ttu-id="36971-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="36971-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="36971-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36971-136">NOTES</span></span>

<span data-ttu-id="36971-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="36971-137">ALIASES</span></span>

<span data-ttu-id="36971-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="36971-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36971-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="36971-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36971-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36971-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36971-141">INPUTOBJECT <IVMwareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="36971-141">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36971-142">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="36971-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="36971-143">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="36971-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="36971-144">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в закрытом облаке</span><span class="sxs-lookup"><span data-stu-id="36971-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="36971-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="36971-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36971-146">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="36971-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="36971-147">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="36971-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="36971-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36971-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="36971-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="36971-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="36971-150">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="36971-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="36971-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36971-151">RELATED LINKS</span></span>

