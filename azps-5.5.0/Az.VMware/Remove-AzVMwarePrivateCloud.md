---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 76ad6df6dbbd9b019e4c89fdbca55107264f0406
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241576"
---
# <span data-ttu-id="1a123-101">Remove-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="1a123-101">Remove-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="1a123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a123-102">SYNOPSIS</span></span>
<span data-ttu-id="1a123-103">Удаление закрытого облака</span><span class="sxs-lookup"><span data-stu-id="1a123-103">Delete a private cloud</span></span>

## <span data-ttu-id="1a123-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a123-104">SYNTAX</span></span>

### <span data-ttu-id="1a123-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a123-105">Delete (Default)</span></span>
```
Remove-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1a123-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1a123-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1a123-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a123-107">DESCRIPTION</span></span>
<span data-ttu-id="1a123-108">Удаление закрытого облака</span><span class="sxs-lookup"><span data-stu-id="1a123-108">Delete a private cloud</span></span>

## <span data-ttu-id="1a123-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a123-109">EXAMPLES</span></span>

### <span data-ttu-id="1a123-110">Пример 1. Удаление закрытого облака</span><span class="sxs-lookup"><span data-stu-id="1a123-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="1a123-111">Удаление закрытого облака</span><span class="sxs-lookup"><span data-stu-id="1a123-111">Delete private cloud</span></span>

## <span data-ttu-id="1a123-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a123-112">PARAMETERS</span></span>

### <span data-ttu-id="1a123-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a123-113">-AsJob</span></span>
<span data-ttu-id="1a123-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="1a123-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1a123-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a123-115">-DefaultProfile</span></span>
<span data-ttu-id="1a123-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a123-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a123-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a123-117">-InputObject</span></span>
<span data-ttu-id="1a123-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="1a123-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a123-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1a123-119">-Name</span></span>
<span data-ttu-id="1a123-120">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="1a123-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a123-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1a123-121">-NoWait</span></span>
<span data-ttu-id="1a123-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="1a123-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1a123-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a123-123">-PassThru</span></span>
<span data-ttu-id="1a123-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="1a123-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1a123-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a123-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a123-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a123-126">The name of the resource group.</span></span>
<span data-ttu-id="1a123-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="1a123-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a123-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a123-128">-SubscriptionId</span></span>
<span data-ttu-id="1a123-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1a123-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a123-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a123-130">-Confirm</span></span>
<span data-ttu-id="1a123-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a123-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a123-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a123-132">-WhatIf</span></span>
<span data-ttu-id="1a123-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a123-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a123-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1a123-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a123-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a123-135">CommonParameters</span></span>
<span data-ttu-id="1a123-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a123-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a123-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a123-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a123-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a123-138">INPUTS</span></span>

### <span data-ttu-id="1a123-139">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="1a123-139">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="1a123-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a123-140">OUTPUTS</span></span>

### <span data-ttu-id="1a123-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a123-141">System.Boolean</span></span>

## <span data-ttu-id="1a123-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a123-142">NOTES</span></span>

<span data-ttu-id="1a123-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1a123-143">ALIASES</span></span>

<span data-ttu-id="1a123-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1a123-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1a123-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="1a123-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1a123-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1a123-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1a123-147">INPUTOBJECT <IVMwareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="1a123-147">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1a123-148">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="1a123-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="1a123-149">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="1a123-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="1a123-150">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="1a123-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="1a123-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="1a123-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1a123-152">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="1a123-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="1a123-153">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="1a123-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="1a123-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a123-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1a123-155">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="1a123-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="1a123-156">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1a123-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1a123-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a123-157">RELATED LINKS</span></span>

