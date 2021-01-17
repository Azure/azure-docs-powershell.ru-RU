---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411607"
---
# <span data-ttu-id="473e0-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="473e0-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="473e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="473e0-102">SYNOPSIS</span></span>
<span data-ttu-id="473e0-103">Получить кластер по имени в частном облаке</span><span class="sxs-lookup"><span data-stu-id="473e0-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="473e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="473e0-104">SYNTAX</span></span>

### <span data-ttu-id="473e0-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="473e0-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="473e0-106">Получить</span><span class="sxs-lookup"><span data-stu-id="473e0-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="473e0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="473e0-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="473e0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="473e0-108">DESCRIPTION</span></span>
<span data-ttu-id="473e0-109">Получить кластер по имени в частном облаке</span><span class="sxs-lookup"><span data-stu-id="473e0-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="473e0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="473e0-110">EXAMPLES</span></span>

### <span data-ttu-id="473e0-111">Пример 1. Получить кластер</span><span class="sxs-lookup"><span data-stu-id="473e0-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="473e0-112">Получить кластер</span><span class="sxs-lookup"><span data-stu-id="473e0-112">Get cluster</span></span>

### <span data-ttu-id="473e0-113">Пример 2. Кластеры списков</span><span class="sxs-lookup"><span data-stu-id="473e0-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="473e0-114">Кластеры списков</span><span class="sxs-lookup"><span data-stu-id="473e0-114">List clusters</span></span>

## <span data-ttu-id="473e0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="473e0-115">PARAMETERS</span></span>

### <span data-ttu-id="473e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473e0-116">-DefaultProfile</span></span>
<span data-ttu-id="473e0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="473e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="473e0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="473e0-118">-InputObject</span></span>
<span data-ttu-id="473e0-119">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="473e0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="473e0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="473e0-120">-Name</span></span>
<span data-ttu-id="473e0-121">Название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="473e0-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="473e0-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="473e0-122">-PrivateCloudName</span></span>
<span data-ttu-id="473e0-123">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="473e0-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="473e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="473e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="473e0-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="473e0-125">The name of the resource group.</span></span>
<span data-ttu-id="473e0-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="473e0-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="473e0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="473e0-127">-SubscriptionId</span></span>
<span data-ttu-id="473e0-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="473e0-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="473e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473e0-129">CommonParameters</span></span>
<span data-ttu-id="473e0-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="473e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473e0-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="473e0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473e0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="473e0-132">INPUTS</span></span>

### <span data-ttu-id="473e0-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="473e0-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="473e0-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="473e0-134">OUTPUTS</span></span>

### <span data-ttu-id="473e0-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="473e0-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="473e0-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="473e0-136">NOTES</span></span>

<span data-ttu-id="473e0-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="473e0-137">ALIASES</span></span>

<span data-ttu-id="473e0-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="473e0-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="473e0-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="473e0-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="473e0-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="473e0-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="473e0-141">INPUTOBJECT <IVMWareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="473e0-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="473e0-142">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="473e0-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="473e0-143">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="473e0-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="473e0-144">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в закрытом облаке</span><span class="sxs-lookup"><span data-stu-id="473e0-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="473e0-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="473e0-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="473e0-146">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="473e0-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="473e0-147">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="473e0-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="473e0-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="473e0-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="473e0-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="473e0-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="473e0-150">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="473e0-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="473e0-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="473e0-151">RELATED LINKS</span></span>

