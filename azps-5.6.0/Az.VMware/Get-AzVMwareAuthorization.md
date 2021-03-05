---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
ms.openlocfilehash: dad73292e6875e2cf38244ed74e0519490860c4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991822"
---
# <span data-ttu-id="f98bf-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="f98bf-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="f98bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f98bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f98bf-103">Получить авторизацию каналов ExpressRoute по имени в закрытом облаке</span><span class="sxs-lookup"><span data-stu-id="f98bf-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="f98bf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f98bf-104">SYNTAX</span></span>

### <span data-ttu-id="f98bf-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f98bf-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f98bf-106">Получить</span><span class="sxs-lookup"><span data-stu-id="f98bf-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f98bf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f98bf-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f98bf-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f98bf-108">DESCRIPTION</span></span>
<span data-ttu-id="f98bf-109">Получить авторизацию каналов ExpressRoute по имени в закрытом облаке</span><span class="sxs-lookup"><span data-stu-id="f98bf-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="f98bf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f98bf-110">EXAMPLES</span></span>

### <span data-ttu-id="f98bf-111">Пример 1. Получить авторизацию</span><span class="sxs-lookup"><span data-stu-id="f98bf-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="f98bf-112">Этот cmdlet получает авторизацию `azps-test-auth` в закрытом облаке `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="f98bf-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="f98bf-113">Пример 2. Авторизация списка</span><span class="sxs-lookup"><span data-stu-id="f98bf-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="f98bf-114">Этот cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="f98bf-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="f98bf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f98bf-115">PARAMETERS</span></span>

### <span data-ttu-id="f98bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98bf-116">-DefaultProfile</span></span>
<span data-ttu-id="f98bf-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f98bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f98bf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f98bf-118">-InputObject</span></span>
<span data-ttu-id="f98bf-119">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="f98bf-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f98bf-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f98bf-120">-Name</span></span>
<span data-ttu-id="f98bf-121">Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="f98bf-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98bf-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="f98bf-122">-PrivateCloudName</span></span>
<span data-ttu-id="f98bf-123">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="f98bf-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="f98bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="f98bf-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f98bf-125">The name of the resource group.</span></span>
<span data-ttu-id="f98bf-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="f98bf-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f98bf-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f98bf-127">-SubscriptionId</span></span>
<span data-ttu-id="f98bf-128">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="f98bf-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f98bf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98bf-129">CommonParameters</span></span>
<span data-ttu-id="f98bf-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f98bf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98bf-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f98bf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98bf-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f98bf-132">INPUTS</span></span>

### <span data-ttu-id="f98bf-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="f98bf-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="f98bf-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f98bf-134">OUTPUTS</span></span>

### <span data-ttu-id="f98bf-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="f98bf-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="f98bf-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f98bf-136">NOTES</span></span>

<span data-ttu-id="f98bf-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f98bf-137">ALIASES</span></span>

<span data-ttu-id="f98bf-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f98bf-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f98bf-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f98bf-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f98bf-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f98bf-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f98bf-141">INPUTOBJECT <IVMWareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="f98bf-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f98bf-142">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="f98bf-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="f98bf-143">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="f98bf-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="f98bf-144">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="f98bf-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="f98bf-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="f98bf-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f98bf-146">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="f98bf-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="f98bf-147">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="f98bf-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="f98bf-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f98bf-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f98bf-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="f98bf-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="f98bf-150">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="f98bf-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f98bf-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f98bf-151">RELATED LINKS</span></span>

