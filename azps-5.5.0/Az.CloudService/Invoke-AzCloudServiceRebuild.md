---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudservicerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
ms.openlocfilehash: 1efeb45704898588c7ba8f08148f88d0eaf3e5c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233508"
---
# <span data-ttu-id="729a6-101">Invoke-AzCloudServiceRebuild</span><span class="sxs-lookup"><span data-stu-id="729a6-101">Invoke-AzCloudServiceRebuild</span></span>

## <span data-ttu-id="729a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="729a6-102">SYNOPSIS</span></span>
<span data-ttu-id="729a6-103">Перестроение экземпляров ролей переустановит операционную систему с экземплярами ролей веб-ролей или сотрудников и инициализирует используемые ими ресурсы хранилища.</span><span class="sxs-lookup"><span data-stu-id="729a6-103">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="729a6-104">Если вы не хотите инициализировать ресурсы хранилища, используйте экземпляры ролей Reimage.</span><span class="sxs-lookup"><span data-stu-id="729a6-104">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="729a6-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="729a6-105">SYNTAX</span></span>

### <span data-ttu-id="729a6-106">RebuildExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="729a6-106">RebuildExpanded (Default)</span></span>
```
Invoke-AzCloudServiceRebuild -CloudServiceName <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="729a6-107">RebuildViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="729a6-107">RebuildViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceRebuild -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="729a6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="729a6-108">DESCRIPTION</span></span>
<span data-ttu-id="729a6-109">Перестроение экземпляров ролей переустановит операционную систему с экземплярами ролей веб-ролей или сотрудников и инициализирует используемые ими ресурсы хранилища.</span><span class="sxs-lookup"><span data-stu-id="729a6-109">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="729a6-110">Если вы не хотите инициализировать ресурсы хранилища, используйте экземпляры ролей Reimage.</span><span class="sxs-lookup"><span data-stu-id="729a6-110">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="729a6-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="729a6-111">EXAMPLES</span></span>

### <span data-ttu-id="729a6-112">Пример 1. Перестройка экземпляров ролей облачной службы</span><span class="sxs-lookup"><span data-stu-id="729a6-112">Example 1: Rebuild role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="729a6-113">Эта команда перестраит 2 экземпляра ролей ContosoFrontEnd_IN_0 и ContosoBackEnd_IN_1 облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="729a6-113">This command rebuilds 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="729a6-114">Пример 2. Перестройка всех ролей облачной службы</span><span class="sxs-lookup"><span data-stu-id="729a6-114">Example 2: Rebuild all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="729a6-115">Эта команда перестраит все экземпляры роли облачной службы ContosoCS, которые принадлежат группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="729a6-115">This command rebuilds all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="729a6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="729a6-116">PARAMETERS</span></span>

### <span data-ttu-id="729a6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="729a6-117">-AsJob</span></span>
<span data-ttu-id="729a6-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="729a6-118">Run the command as a job</span></span>

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

### <span data-ttu-id="729a6-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="729a6-119">-CloudServiceName</span></span>
<span data-ttu-id="729a6-120">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="729a6-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="729a6-121">-DefaultProfile</span></span>
<span data-ttu-id="729a6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="729a6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="729a6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="729a6-123">-InputObject</span></span>
<span data-ttu-id="729a6-124">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="729a6-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="729a6-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="729a6-125">-NoWait</span></span>
<span data-ttu-id="729a6-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="729a6-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="729a6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="729a6-127">-PassThru</span></span>
<span data-ttu-id="729a6-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="729a6-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="729a6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="729a6-129">-ResourceGroupName</span></span>
<span data-ttu-id="729a6-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="729a6-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729a6-131">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="729a6-131">-RoleInstance</span></span>
<span data-ttu-id="729a6-132">Список имен экземпляров ролей облачной службы.</span><span class="sxs-lookup"><span data-stu-id="729a6-132">List of cloud service role instance names.</span></span>
<span data-ttu-id="729a6-133">Значение \*означает все экземпляры ролей облачной службы.</span><span class="sxs-lookup"><span data-stu-id="729a6-133">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="729a6-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="729a6-134">-SubscriptionId</span></span>
<span data-ttu-id="729a6-135">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="729a6-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="729a6-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="729a6-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729a6-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="729a6-137">-Confirm</span></span>
<span data-ttu-id="729a6-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="729a6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="729a6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="729a6-139">-WhatIf</span></span>
<span data-ttu-id="729a6-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="729a6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="729a6-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="729a6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="729a6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729a6-142">CommonParameters</span></span>
<span data-ttu-id="729a6-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="729a6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729a6-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="729a6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729a6-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="729a6-145">INPUTS</span></span>

### <span data-ttu-id="729a6-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="729a6-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="729a6-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="729a6-147">OUTPUTS</span></span>

### <span data-ttu-id="729a6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="729a6-148">System.Boolean</span></span>

## <span data-ttu-id="729a6-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="729a6-149">NOTES</span></span>

<span data-ttu-id="729a6-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="729a6-150">ALIASES</span></span>

<span data-ttu-id="729a6-151">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="729a6-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="729a6-152">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="729a6-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="729a6-153">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="729a6-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="729a6-154">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="729a6-154">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="729a6-155">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="729a6-155">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="729a6-156">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="729a6-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="729a6-157">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="729a6-157">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="729a6-158">`[RoleInstanceName <String>]`: Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="729a6-158">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="729a6-159">`[RoleName <String>]`: Название роли.</span><span class="sxs-lookup"><span data-stu-id="729a6-159">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="729a6-160">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="729a6-160">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="729a6-161">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="729a6-161">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="729a6-162">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="729a6-162">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="729a6-163">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="729a6-163">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="729a6-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="729a6-164">RELATED LINKS</span></span>

