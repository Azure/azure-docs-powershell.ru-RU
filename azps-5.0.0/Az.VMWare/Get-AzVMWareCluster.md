---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248441"
---
# <span data-ttu-id="11871-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="11871-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="11871-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11871-102">SYNOPSIS</span></span>
<span data-ttu-id="11871-103">Получение кластера по имени в частном облаке</span><span class="sxs-lookup"><span data-stu-id="11871-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="11871-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11871-104">SYNTAX</span></span>

### <span data-ttu-id="11871-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11871-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11871-106">Получить</span><span class="sxs-lookup"><span data-stu-id="11871-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11871-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11871-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="11871-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11871-108">DESCRIPTION</span></span>
<span data-ttu-id="11871-109">Получение кластера по имени в частном облаке</span><span class="sxs-lookup"><span data-stu-id="11871-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="11871-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11871-110">EXAMPLES</span></span>

### <span data-ttu-id="11871-111">Пример 1: получение кластера</span><span class="sxs-lookup"><span data-stu-id="11871-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="11871-112">Получить кластер</span><span class="sxs-lookup"><span data-stu-id="11871-112">Get cluster</span></span>

### <span data-ttu-id="11871-113">Пример 2: список кластеров</span><span class="sxs-lookup"><span data-stu-id="11871-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="11871-114">Список кластеров</span><span class="sxs-lookup"><span data-stu-id="11871-114">List clusters</span></span>

## <span data-ttu-id="11871-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11871-115">PARAMETERS</span></span>

### <span data-ttu-id="11871-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11871-116">-DefaultProfile</span></span>
<span data-ttu-id="11871-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11871-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11871-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11871-118">-InputObject</span></span>
<span data-ttu-id="11871-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="11871-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="11871-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11871-120">-Name</span></span>
<span data-ttu-id="11871-121">Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="11871-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="11871-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="11871-122">-PrivateCloudName</span></span>
<span data-ttu-id="11871-123">Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="11871-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="11871-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11871-124">-ResourceGroupName</span></span>
<span data-ttu-id="11871-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11871-125">The name of the resource group.</span></span>
<span data-ttu-id="11871-126">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="11871-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="11871-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11871-127">-SubscriptionId</span></span>
<span data-ttu-id="11871-128">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="11871-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="11871-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11871-129">CommonParameters</span></span>
<span data-ttu-id="11871-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11871-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11871-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11871-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11871-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11871-132">INPUTS</span></span>

### <span data-ttu-id="11871-133">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="11871-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="11871-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11871-134">OUTPUTS</span></span>

### <span data-ttu-id="11871-135">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="11871-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="11871-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="11871-136">NOTES</span></span>

<span data-ttu-id="11871-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="11871-137">ALIASES</span></span>

<span data-ttu-id="11871-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="11871-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11871-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="11871-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11871-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11871-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11871-141">INPUTOBJECT <IVMWareIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="11871-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11871-142">`[AuthorizationName <String>]`: Имя авторизации канала ExpressRoute в частном облаке.</span><span class="sxs-lookup"><span data-stu-id="11871-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="11871-143">`[ClusterName <String>]`: Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="11871-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="11871-144">`[HcxEnterpriseSiteName <String>]`: Имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="11871-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="11871-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="11871-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11871-146">`[Location <String>]`: Регион Azure</span><span class="sxs-lookup"><span data-stu-id="11871-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="11871-147">`[PrivateCloudName <String>]`: Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="11871-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="11871-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11871-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="11871-149">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="11871-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="11871-150">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="11871-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="11871-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11871-151">RELATED LINKS</span></span>

