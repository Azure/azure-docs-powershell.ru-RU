---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
ms.openlocfilehash: 707e7e4e702912d4d838913cb7ca030fef914e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231324"
---
# <span data-ttu-id="ff037-101">Get-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="ff037-101">Get-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="ff037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff037-102">SYNOPSIS</span></span>
<span data-ttu-id="ff037-103">Получите частное облако</span><span class="sxs-lookup"><span data-stu-id="ff037-103">Get a private cloud</span></span>

## <span data-ttu-id="ff037-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff037-104">SYNTAX</span></span>

### <span data-ttu-id="ff037-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff037-105">List1 (Default)</span></span>
```
Get-AzVMwarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff037-106">Получить</span><span class="sxs-lookup"><span data-stu-id="ff037-106">Get</span></span>
```
Get-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff037-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ff037-107">GetViaIdentity</span></span>
```
Get-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff037-108">Список</span><span class="sxs-lookup"><span data-stu-id="ff037-108">List</span></span>
```
Get-AzVMwarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff037-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff037-109">DESCRIPTION</span></span>
<span data-ttu-id="ff037-110">Получите частное облако</span><span class="sxs-lookup"><span data-stu-id="ff037-110">Get a private cloud</span></span>

## <span data-ttu-id="ff037-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff037-111">EXAMPLES</span></span>

### <span data-ttu-id="ff037-112">Пример 1. Список частного облака в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="ff037-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ff037-113">Перечислить частное облако в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="ff037-113">List private cloud under subscription</span></span>

### <span data-ttu-id="ff037-114">Пример 2. Список закрытого облака в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="ff037-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ff037-115">Список закрытого облака в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="ff037-115">List private cloud under resource group</span></span>

### <span data-ttu-id="ff037-116">Пример 3. Получить частное облако</span><span class="sxs-lookup"><span data-stu-id="ff037-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ff037-117">Получить частное облако</span><span class="sxs-lookup"><span data-stu-id="ff037-117">Get private cloud</span></span>

## <span data-ttu-id="ff037-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff037-118">PARAMETERS</span></span>

### <span data-ttu-id="ff037-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff037-119">-DefaultProfile</span></span>
<span data-ttu-id="ff037-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff037-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff037-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff037-121">-InputObject</span></span>
<span data-ttu-id="ff037-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ff037-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff037-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ff037-123">-Name</span></span>
<span data-ttu-id="ff037-124">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="ff037-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff037-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff037-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff037-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff037-126">The name of the resource group.</span></span>
<span data-ttu-id="ff037-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ff037-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ff037-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff037-128">-SubscriptionId</span></span>
<span data-ttu-id="ff037-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ff037-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ff037-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff037-130">CommonParameters</span></span>
<span data-ttu-id="ff037-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff037-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff037-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff037-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff037-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff037-133">INPUTS</span></span>

### <span data-ttu-id="ff037-134">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="ff037-134">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="ff037-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff037-135">OUTPUTS</span></span>

### <span data-ttu-id="ff037-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="ff037-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="ff037-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff037-137">NOTES</span></span>

<span data-ttu-id="ff037-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ff037-138">ALIASES</span></span>

<span data-ttu-id="ff037-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ff037-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff037-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ff037-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff037-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff037-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff037-142">INPUTOBJECT <IVMwareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ff037-142">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff037-143">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="ff037-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ff037-144">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="ff037-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ff037-145">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="ff037-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ff037-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ff037-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff037-147">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="ff037-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ff037-148">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="ff037-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ff037-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff037-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ff037-150">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ff037-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="ff037-151">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ff037-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ff037-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff037-152">RELATED LINKS</span></span>

