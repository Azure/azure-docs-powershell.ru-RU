---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505813"
---
# <span data-ttu-id="65782-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="65782-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="65782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65782-102">SYNOPSIS</span></span>
<span data-ttu-id="65782-103">Квота возврата для подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="65782-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="65782-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="65782-104">SYNTAX</span></span>

### <span data-ttu-id="65782-105">Проверка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65782-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="65782-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="65782-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="65782-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65782-107">DESCRIPTION</span></span>
<span data-ttu-id="65782-108">Квота возврата для подписки по регионам</span><span class="sxs-lookup"><span data-stu-id="65782-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="65782-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="65782-109">EXAMPLES</span></span>

### <span data-ttu-id="65782-110">Пример 1. Проверка доступности квоты</span><span class="sxs-lookup"><span data-stu-id="65782-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="65782-111">Проверка доступности квоты</span><span class="sxs-lookup"><span data-stu-id="65782-111">Check quota availability</span></span>

## <span data-ttu-id="65782-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65782-112">PARAMETERS</span></span>

### <span data-ttu-id="65782-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65782-113">-DefaultProfile</span></span>
<span data-ttu-id="65782-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65782-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65782-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65782-115">-InputObject</span></span>
<span data-ttu-id="65782-116">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="65782-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="65782-117">-Location</span><span class="sxs-lookup"><span data-stu-id="65782-117">-Location</span></span>
<span data-ttu-id="65782-118">Регион Azure</span><span class="sxs-lookup"><span data-stu-id="65782-118">Azure region</span></span>

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

### <span data-ttu-id="65782-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65782-119">-SubscriptionId</span></span>
<span data-ttu-id="65782-120">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="65782-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="65782-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65782-121">-Confirm</span></span>
<span data-ttu-id="65782-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65782-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65782-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65782-123">-WhatIf</span></span>
<span data-ttu-id="65782-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65782-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65782-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="65782-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65782-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65782-126">CommonParameters</span></span>
<span data-ttu-id="65782-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65782-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65782-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65782-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65782-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65782-129">INPUTS</span></span>

### <span data-ttu-id="65782-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="65782-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="65782-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65782-131">OUTPUTS</span></span>

### <span data-ttu-id="65782-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span><span class="sxs-lookup"><span data-stu-id="65782-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="65782-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="65782-133">NOTES</span></span>

<span data-ttu-id="65782-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="65782-134">ALIASES</span></span>

<span data-ttu-id="65782-135">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="65782-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="65782-136">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="65782-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="65782-137">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="65782-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="65782-138">INPUTOBJECT <IVMWareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="65782-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="65782-139">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="65782-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="65782-140">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="65782-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="65782-141">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в закрытом облаке</span><span class="sxs-lookup"><span data-stu-id="65782-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="65782-142">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="65782-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="65782-143">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="65782-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="65782-144">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="65782-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="65782-145">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65782-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="65782-146">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="65782-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="65782-147">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="65782-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="65782-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65782-148">RELATED LINKS</span></span>

