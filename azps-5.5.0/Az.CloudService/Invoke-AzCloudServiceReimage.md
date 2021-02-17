---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudservicereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
ms.openlocfilehash: 51fa4faa9491e4d119f3c14b1c5b44bee6fdd15e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234817"
---
# <span data-ttu-id="e840a-101">Invoke-AzCloudServiceReimage</span><span class="sxs-lookup"><span data-stu-id="e840a-101">Invoke-AzCloudServiceReimage</span></span>

## <span data-ttu-id="e840a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e840a-102">SYNOPSIS</span></span>
<span data-ttu-id="e840a-103">Асинхронная операция reimage переустановит операционную систему для экземпляров ролей веб-ролей или сотрудников.</span><span class="sxs-lookup"><span data-stu-id="e840a-103">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="e840a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e840a-104">SYNTAX</span></span>

### <span data-ttu-id="e840a-105">ReimageExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e840a-105">ReimageExpanded (Default)</span></span>
```
Invoke-AzCloudServiceReimage -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e840a-106">ReimageViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e840a-106">ReimageViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceReimage -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e840a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e840a-107">DESCRIPTION</span></span>
<span data-ttu-id="e840a-108">Асинхронная операция reimage переустановит операционную систему для экземпляров ролей веб-ролей или сотрудников.</span><span class="sxs-lookup"><span data-stu-id="e840a-108">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="e840a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e840a-109">EXAMPLES</span></span>

### <span data-ttu-id="e840a-110">Пример 1. Повторное экземпляры роли облачной службы</span><span class="sxs-lookup"><span data-stu-id="e840a-110">Example 1: Reimage role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="e840a-111">Эта команда переимежает два экземпляра ролей ContosoFrontEnd_IN_0 и ContosoBackEnd_IN_1 облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="e840a-111">This command reimages 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="e840a-112">Пример 2. Повторное переимяние всех ролей облачной службы</span><span class="sxs-lookup"><span data-stu-id="e840a-112">Example 2: Reimage all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="e840a-113">Эта команда переимежает все экземпляры ролей облачной службы ContosoCS, которые принадлежат к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="e840a-113">This command reimages all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="e840a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e840a-114">PARAMETERS</span></span>

### <span data-ttu-id="e840a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e840a-115">-AsJob</span></span>
<span data-ttu-id="e840a-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e840a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e840a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e840a-117">-DefaultProfile</span></span>
<span data-ttu-id="e840a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e840a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e840a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e840a-119">-InputObject</span></span>
<span data-ttu-id="e840a-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="e840a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e840a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e840a-121">-Name</span></span>
<span data-ttu-id="e840a-122">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="e840a-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e840a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e840a-123">-NoWait</span></span>
<span data-ttu-id="e840a-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="e840a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e840a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e840a-125">-PassThru</span></span>
<span data-ttu-id="e840a-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="e840a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e840a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e840a-127">-ResourceGroupName</span></span>
<span data-ttu-id="e840a-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e840a-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e840a-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="e840a-129">-RoleInstance</span></span>
<span data-ttu-id="e840a-130">Список имен экземпляров ролей облачной службы.</span><span class="sxs-lookup"><span data-stu-id="e840a-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="e840a-131">Значение \*означает все экземпляры ролей облачной службы.</span><span class="sxs-lookup"><span data-stu-id="e840a-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="e840a-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e840a-132">-SubscriptionId</span></span>
<span data-ttu-id="e840a-133">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e840a-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e840a-134">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="e840a-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e840a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e840a-135">-Confirm</span></span>
<span data-ttu-id="e840a-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e840a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e840a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e840a-137">-WhatIf</span></span>
<span data-ttu-id="e840a-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e840a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e840a-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e840a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e840a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e840a-140">CommonParameters</span></span>
<span data-ttu-id="e840a-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e840a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e840a-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e840a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e840a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e840a-143">INPUTS</span></span>

### <span data-ttu-id="e840a-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e840a-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="e840a-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e840a-145">OUTPUTS</span></span>

### <span data-ttu-id="e840a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e840a-146">System.Boolean</span></span>

## <span data-ttu-id="e840a-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e840a-147">NOTES</span></span>

<span data-ttu-id="e840a-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e840a-148">ALIASES</span></span>

<span data-ttu-id="e840a-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e840a-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e840a-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="e840a-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e840a-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e840a-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e840a-152">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="e840a-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e840a-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e840a-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="e840a-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="e840a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e840a-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e840a-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="e840a-156">`[RoleInstanceName <String>]`: имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="e840a-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="e840a-157">`[RoleName <String>]`: название роли.</span><span class="sxs-lookup"><span data-stu-id="e840a-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="e840a-158">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e840a-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e840a-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="e840a-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e840a-160">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="e840a-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="e840a-161">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="e840a-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="e840a-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e840a-162">RELATED LINKS</span></span>

