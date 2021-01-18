---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505805"
---
# <span data-ttu-id="fab83-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="fab83-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="fab83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab83-102">SYNOPSIS</span></span>
<span data-ttu-id="fab83-103">Возврат состояния пробной подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="fab83-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="fab83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fab83-104">SYNTAX</span></span>

### <span data-ttu-id="fab83-105">Проверка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fab83-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fab83-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fab83-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fab83-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fab83-107">DESCRIPTION</span></span>
<span data-ttu-id="fab83-108">Возврат состояния пробной подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="fab83-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="fab83-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fab83-109">EXAMPLES</span></span>

### <span data-ttu-id="fab83-110">Пример 1. Проверка доступности пробной версия</span><span class="sxs-lookup"><span data-stu-id="fab83-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="fab83-111">Проверка доступности пробной версия</span><span class="sxs-lookup"><span data-stu-id="fab83-111">Check trial availability</span></span>

## <span data-ttu-id="fab83-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fab83-112">PARAMETERS</span></span>

### <span data-ttu-id="fab83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab83-113">-DefaultProfile</span></span>
<span data-ttu-id="fab83-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fab83-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fab83-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fab83-115">-InputObject</span></span>
<span data-ttu-id="fab83-116">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fab83-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fab83-117">-Location</span><span class="sxs-lookup"><span data-stu-id="fab83-117">-Location</span></span>
<span data-ttu-id="fab83-118">Регион Azure</span><span class="sxs-lookup"><span data-stu-id="fab83-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab83-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fab83-119">-SubscriptionId</span></span>
<span data-ttu-id="fab83-120">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fab83-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab83-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fab83-121">-Confirm</span></span>
<span data-ttu-id="fab83-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fab83-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab83-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab83-123">-WhatIf</span></span>
<span data-ttu-id="fab83-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fab83-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab83-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fab83-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab83-126">CommonParameters</span></span>
<span data-ttu-id="fab83-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab83-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fab83-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab83-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fab83-129">INPUTS</span></span>

### <span data-ttu-id="fab83-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="fab83-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="fab83-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fab83-131">OUTPUTS</span></span>

### <span data-ttu-id="fab83-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="fab83-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="fab83-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fab83-133">NOTES</span></span>

<span data-ttu-id="fab83-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fab83-134">ALIASES</span></span>

<span data-ttu-id="fab83-135">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fab83-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fab83-136">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="fab83-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fab83-137">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fab83-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fab83-138">INPUTOBJECT <IVMWareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="fab83-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fab83-139">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="fab83-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="fab83-140">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="fab83-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="fab83-141">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="fab83-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="fab83-142">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="fab83-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fab83-143">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="fab83-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="fab83-144">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="fab83-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="fab83-145">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fab83-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fab83-146">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="fab83-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="fab83-147">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fab83-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="fab83-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fab83-148">RELATED LINKS</span></span>

