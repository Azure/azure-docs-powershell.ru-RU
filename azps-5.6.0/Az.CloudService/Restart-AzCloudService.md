---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
ms.openlocfilehash: e61eea1d00468937a46f90fdd6a995f5f53ff468
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956440"
---
# <span data-ttu-id="11040-101">Restart-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="11040-101">Restart-AzCloudService</span></span>

## <span data-ttu-id="11040-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11040-102">SYNOPSIS</span></span>
<span data-ttu-id="11040-103">Перезапуск одного или несколько экземпляров ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="11040-103">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="11040-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11040-104">SYNTAX</span></span>

### <span data-ttu-id="11040-105">RestartExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11040-105">RestartExpanded (Default)</span></span>
```
Restart-AzCloudService -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="11040-106">RestartViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="11040-106">RestartViaIdentityExpanded</span></span>
```
Restart-AzCloudService -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="11040-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11040-107">DESCRIPTION</span></span>
<span data-ttu-id="11040-108">Перезапуск одного или несколько экземпляров ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="11040-108">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="11040-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11040-109">EXAMPLES</span></span>

### <span data-ttu-id="11040-110">Пример 1. Перезапуск экземпляров ролей облачной службы</span><span class="sxs-lookup"><span data-stu-id="11040-110">Example 1: Restart role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="11040-111">Эта команда перезапускет 2 экземпляра ролей ContosoFrontEnd_IN_0 и ContosoBackEnd_IN_1 облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="11040-111">This command restarts 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="11040-112">Пример 2. Перезапуск всех ролей облачной службы</span><span class="sxs-lookup"><span data-stu-id="11040-112">Example 2: Restart all roles of cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="11040-113">Эта команда перезапустит все экземпляры ролей облачной службы ContosoCS, которые принадлежат группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="11040-113">This command restarts all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="11040-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11040-114">PARAMETERS</span></span>

### <span data-ttu-id="11040-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11040-115">-AsJob</span></span>
<span data-ttu-id="11040-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="11040-116">Run the command as a job</span></span>

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

### <span data-ttu-id="11040-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11040-117">-DefaultProfile</span></span>
<span data-ttu-id="11040-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11040-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11040-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11040-119">-InputObject</span></span>
<span data-ttu-id="11040-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="11040-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11040-121">-Name</span><span class="sxs-lookup"><span data-stu-id="11040-121">-Name</span></span>
<span data-ttu-id="11040-122">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="11040-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11040-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="11040-123">-NoWait</span></span>
<span data-ttu-id="11040-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="11040-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="11040-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11040-125">-PassThru</span></span>
<span data-ttu-id="11040-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="11040-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="11040-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11040-127">-ResourceGroupName</span></span>
<span data-ttu-id="11040-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11040-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11040-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="11040-129">-RoleInstance</span></span>
<span data-ttu-id="11040-130">Список имен экземпляров ролей облачной службы.</span><span class="sxs-lookup"><span data-stu-id="11040-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="11040-131">Значение \*означает все экземпляры ролей облачной службы.</span><span class="sxs-lookup"><span data-stu-id="11040-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="11040-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11040-132">-SubscriptionId</span></span>
<span data-ttu-id="11040-133">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="11040-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="11040-134">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="11040-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11040-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11040-135">-Confirm</span></span>
<span data-ttu-id="11040-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="11040-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11040-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11040-137">-WhatIf</span></span>
<span data-ttu-id="11040-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11040-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11040-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="11040-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11040-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11040-140">CommonParameters</span></span>
<span data-ttu-id="11040-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11040-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11040-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11040-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11040-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11040-143">INPUTS</span></span>

### <span data-ttu-id="11040-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="11040-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="11040-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11040-145">OUTPUTS</span></span>

### <span data-ttu-id="11040-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11040-146">System.Boolean</span></span>

## <span data-ttu-id="11040-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11040-147">NOTES</span></span>

<span data-ttu-id="11040-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="11040-148">ALIASES</span></span>

<span data-ttu-id="11040-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="11040-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11040-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="11040-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11040-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11040-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11040-152">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="11040-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11040-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="11040-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="11040-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="11040-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11040-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="11040-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="11040-156">`[RoleInstanceName <String>]`: имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="11040-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="11040-157">`[RoleName <String>]`: Название роли.</span><span class="sxs-lookup"><span data-stu-id="11040-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="11040-158">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="11040-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="11040-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="11040-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="11040-160">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="11040-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="11040-161">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="11040-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="11040-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11040-162">RELATED LINKS</span></span>

