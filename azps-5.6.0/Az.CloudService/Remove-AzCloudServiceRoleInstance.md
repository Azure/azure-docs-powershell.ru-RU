---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/remove-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 5a29444c5f6d05ddbf614e86cd13af6818d24d79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956456"
---
# <span data-ttu-id="8b6f5-101">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="8b6f5-101">Remove-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="8b6f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b6f5-103">Удаляет экземпляры ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-103">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="8b6f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b6f5-104">SYNTAX</span></span>

### <span data-ttu-id="8b6f5-105">DeleteExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b6f5-105">DeleteExpanded (Default)</span></span>
```
Remove-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstance <String[]> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8b6f5-106">DeleteViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8b6f5-106">DeleteViaIdentityExpanded</span></span>
```
Remove-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b6f5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b6f5-107">DESCRIPTION</span></span>
<span data-ttu-id="8b6f5-108">Удаляет экземпляры ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-108">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="8b6f5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b6f5-109">EXAMPLES</span></span>

### <span data-ttu-id="8b6f5-110">Пример 1. Удаление экземпляра роли облачной службы</span><span class="sxs-lookup"><span data-stu-id="8b6f5-110">Example 1: Remove a cloud service role instance</span></span>
```powershell
PS C:\> Remove-AzCloudServiceInstance -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="8b6f5-111">Эта команда удаляет экземпляр роли ContosoFrontEnd_IN_0 облачной службы ContosoCS, который принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-111">This command removes the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="8b6f5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b6f5-112">PARAMETERS</span></span>

### <span data-ttu-id="8b6f5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b6f5-113">-AsJob</span></span>
<span data-ttu-id="8b6f5-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="8b6f5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8b6f5-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="8b6f5-115">-CloudServiceName</span></span>
<span data-ttu-id="8b6f5-116">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-116">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b6f5-117">-DefaultProfile</span></span>
<span data-ttu-id="8b6f5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b6f5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b6f5-119">-InputObject</span></span>
<span data-ttu-id="8b6f5-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b6f5-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8b6f5-121">-NoWait</span></span>
<span data-ttu-id="8b6f5-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="8b6f5-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8b6f5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b6f5-123">-PassThru</span></span>
<span data-ttu-id="8b6f5-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8b6f5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b6f5-125">-ResourceGroupName</span></span>
<span data-ttu-id="8b6f5-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6f5-127">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="8b6f5-127">-RoleInstance</span></span>
<span data-ttu-id="8b6f5-128">Список имен экземпляров ролей облачной службы.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-128">List of cloud service role instance names.</span></span>
<span data-ttu-id="8b6f5-129">Значение \*означает все экземпляры ролей облачной службы.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-129">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6f5-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b6f5-130">-SubscriptionId</span></span>
<span data-ttu-id="8b6f5-131">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-131">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8b6f5-132">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6f5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b6f5-133">-Confirm</span></span>
<span data-ttu-id="8b6f5-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b6f5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b6f5-135">-WhatIf</span></span>
<span data-ttu-id="8b6f5-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b6f5-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b6f5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b6f5-138">CommonParameters</span></span>
<span data-ttu-id="8b6f5-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b6f5-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b6f5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b6f5-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b6f5-141">INPUTS</span></span>

### <span data-ttu-id="8b6f5-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="8b6f5-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="8b6f5-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b6f5-143">OUTPUTS</span></span>

### <span data-ttu-id="8b6f5-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8b6f5-144">System.Boolean</span></span>

## <span data-ttu-id="8b6f5-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b6f5-145">NOTES</span></span>

<span data-ttu-id="8b6f5-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8b6f5-146">ALIASES</span></span>

<span data-ttu-id="8b6f5-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8b6f5-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8b6f5-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8b6f5-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8b6f5-150">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="8b6f5-150">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8b6f5-151">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="8b6f5-151">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="8b6f5-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="8b6f5-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8b6f5-153">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="8b6f5-153">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="8b6f5-154">`[RoleInstanceName <String>]`: имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-154">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="8b6f5-155">`[RoleName <String>]`: название роли.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-155">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="8b6f5-156">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8b6f5-157">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8b6f5-158">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-158">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="8b6f5-159">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="8b6f5-159">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="8b6f5-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b6f5-160">RELATED LINKS</span></span>

