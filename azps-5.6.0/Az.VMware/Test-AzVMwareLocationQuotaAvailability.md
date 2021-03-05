---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
ms.openlocfilehash: 61ecab0a22df339af7c790fd51def5a880d9b607
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988630"
---
# <span data-ttu-id="9165c-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="9165c-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="9165c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9165c-102">SYNOPSIS</span></span>
<span data-ttu-id="9165c-103">Квота возврата для подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="9165c-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="9165c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9165c-104">SYNTAX</span></span>

### <span data-ttu-id="9165c-105">Проверка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9165c-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9165c-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9165c-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9165c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9165c-107">DESCRIPTION</span></span>
<span data-ttu-id="9165c-108">Квота возврата для подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="9165c-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="9165c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9165c-109">EXAMPLES</span></span>

### <span data-ttu-id="9165c-110">Пример 1. Проверка доступности квоты</span><span class="sxs-lookup"><span data-stu-id="9165c-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="9165c-111">Проверка доступности квоты</span><span class="sxs-lookup"><span data-stu-id="9165c-111">Check quota availability</span></span>

## <span data-ttu-id="9165c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9165c-112">PARAMETERS</span></span>

### <span data-ttu-id="9165c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9165c-113">-DefaultProfile</span></span>
<span data-ttu-id="9165c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9165c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9165c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9165c-115">-InputObject</span></span>
<span data-ttu-id="9165c-116">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9165c-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9165c-117">-Location</span><span class="sxs-lookup"><span data-stu-id="9165c-117">-Location</span></span>
<span data-ttu-id="9165c-118">Регион Azure</span><span class="sxs-lookup"><span data-stu-id="9165c-118">Azure region</span></span>

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

### <span data-ttu-id="9165c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9165c-119">-SubscriptionId</span></span>
<span data-ttu-id="9165c-120">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9165c-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9165c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9165c-121">-Confirm</span></span>
<span data-ttu-id="9165c-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9165c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9165c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9165c-123">-WhatIf</span></span>
<span data-ttu-id="9165c-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9165c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9165c-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9165c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9165c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9165c-126">CommonParameters</span></span>
<span data-ttu-id="9165c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9165c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9165c-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9165c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9165c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9165c-129">INPUTS</span></span>

### <span data-ttu-id="9165c-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="9165c-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="9165c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9165c-131">OUTPUTS</span></span>

### <span data-ttu-id="9165c-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span><span class="sxs-lookup"><span data-stu-id="9165c-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="9165c-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9165c-133">NOTES</span></span>

<span data-ttu-id="9165c-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9165c-134">ALIASES</span></span>

<span data-ttu-id="9165c-135">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9165c-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9165c-136">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="9165c-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9165c-137">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9165c-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9165c-138">INPUTOBJECT <IVMWareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="9165c-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9165c-139">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="9165c-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="9165c-140">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="9165c-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="9165c-141">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="9165c-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="9165c-142">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="9165c-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9165c-143">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="9165c-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="9165c-144">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="9165c-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="9165c-145">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9165c-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9165c-146">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="9165c-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="9165c-147">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9165c-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="9165c-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9165c-148">RELATED LINKS</span></span>

