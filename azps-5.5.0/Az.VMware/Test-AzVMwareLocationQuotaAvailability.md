---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
ms.openlocfilehash: 93ede93fc47d5afcabeda8a38a4d8c5fc57c30c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216604"
---
# <span data-ttu-id="e09e5-101">Test-AzVMwareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="e09e5-101">Test-AzVMwareLocationQuotaAvailability</span></span>

## <span data-ttu-id="e09e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e09e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e09e5-103">Квота возврата для подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="e09e5-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="e09e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e09e5-104">SYNTAX</span></span>

### <span data-ttu-id="e09e5-105">Проверка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e09e5-105">Check (Default)</span></span>
```
Test-AzVMwareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e09e5-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e09e5-106">CheckViaIdentity</span></span>
```
Test-AzVMwareLocationQuotaAvailability -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e09e5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e09e5-107">DESCRIPTION</span></span>
<span data-ttu-id="e09e5-108">Квота возврата для подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="e09e5-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="e09e5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e09e5-109">EXAMPLES</span></span>

### <span data-ttu-id="e09e5-110">Пример 1. Проверка доступности квоты</span><span class="sxs-lookup"><span data-stu-id="e09e5-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMwareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="e09e5-111">Проверка доступности квоты</span><span class="sxs-lookup"><span data-stu-id="e09e5-111">Check quota availability</span></span>

## <span data-ttu-id="e09e5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e09e5-112">PARAMETERS</span></span>

### <span data-ttu-id="e09e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e09e5-113">-DefaultProfile</span></span>
<span data-ttu-id="e09e5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e09e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e09e5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e09e5-115">-InputObject</span></span>
<span data-ttu-id="e09e5-116">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="e09e5-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e09e5-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e09e5-117">-Location</span></span>
<span data-ttu-id="e09e5-118">Регион Azure</span><span class="sxs-lookup"><span data-stu-id="e09e5-118">Azure region</span></span>

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

### <span data-ttu-id="e09e5-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e09e5-119">-SubscriptionId</span></span>
<span data-ttu-id="e09e5-120">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e09e5-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e09e5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e09e5-121">-Confirm</span></span>
<span data-ttu-id="e09e5-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e09e5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e09e5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e09e5-123">-WhatIf</span></span>
<span data-ttu-id="e09e5-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e09e5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e09e5-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e09e5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e09e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e09e5-126">CommonParameters</span></span>
<span data-ttu-id="e09e5-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e09e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e09e5-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e09e5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e09e5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e09e5-129">INPUTS</span></span>

### <span data-ttu-id="e09e5-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="e09e5-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="e09e5-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e09e5-131">OUTPUTS</span></span>

### <span data-ttu-id="e09e5-132">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IQuota</span><span class="sxs-lookup"><span data-stu-id="e09e5-132">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="e09e5-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e09e5-133">NOTES</span></span>

<span data-ttu-id="e09e5-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e09e5-134">ALIASES</span></span>

<span data-ttu-id="e09e5-135">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e09e5-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e09e5-136">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="e09e5-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e09e5-137">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e09e5-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e09e5-138">INPUTOBJECT <IVMwareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="e09e5-138">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e09e5-139">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="e09e5-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="e09e5-140">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="e09e5-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="e09e5-141">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="e09e5-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="e09e5-142">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="e09e5-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e09e5-143">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="e09e5-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="e09e5-144">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="e09e5-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="e09e5-145">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e09e5-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e09e5-146">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e09e5-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="e09e5-147">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e09e5-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="e09e5-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e09e5-148">RELATED LINKS</span></span>

