---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
ms.openlocfilehash: d998e29fc254b1bf507ab7d7732bc3bdcf68f54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211881"
---
# <span data-ttu-id="20741-101">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="20741-101">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>

## <span data-ttu-id="20741-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20741-102">SYNOPSIS</span></span>
<span data-ttu-id="20741-103">Асинхронная операция переустановки экземпляра роли переустановит операционную систему в экземплярах ролей веб-ролей или сотрудников и инициализирует используемые ими ресурсы хранилища.</span><span class="sxs-lookup"><span data-stu-id="20741-103">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="20741-104">Если вы не хотите инициализировать ресурсы хранилища, используйте экземпляр роли Reimage.</span><span class="sxs-lookup"><span data-stu-id="20741-104">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="20741-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="20741-105">SYNTAX</span></span>

### <span data-ttu-id="20741-106">Перестройка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20741-106">Rebuild (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20741-107">RebuildViaIdentity</span><span class="sxs-lookup"><span data-stu-id="20741-107">RebuildViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20741-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20741-108">DESCRIPTION</span></span>
<span data-ttu-id="20741-109">Асинхронная операция переустановки экземпляра роли переустановит операционную систему с экземплярами ролей веб-ролей или сотрудников и инициализирует используемые ими ресурсы хранилища.</span><span class="sxs-lookup"><span data-stu-id="20741-109">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="20741-110">Если вы не хотите инициализировать ресурсы хранилища, используйте экземпляр роли Reimage.</span><span class="sxs-lookup"><span data-stu-id="20741-110">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="20741-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="20741-111">EXAMPLES</span></span>

### <span data-ttu-id="20741-112">Пример 1. Перестройка экземпляра роли облачной службы</span><span class="sxs-lookup"><span data-stu-id="20741-112">Example 1: Rebuild role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="20741-113">Эта команда переимежает экземпляр роли ContosoFrontEnd_IN_0 облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="20741-113">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="20741-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20741-114">PARAMETERS</span></span>

### <span data-ttu-id="20741-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20741-115">-AsJob</span></span>
<span data-ttu-id="20741-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="20741-116">Run the command as a job</span></span>

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

### <span data-ttu-id="20741-117">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="20741-117">-CloudServiceName</span></span>
<span data-ttu-id="20741-118">.</span><span class="sxs-lookup"><span data-stu-id="20741-118">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20741-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20741-119">-DefaultProfile</span></span>
<span data-ttu-id="20741-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20741-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20741-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20741-121">-InputObject</span></span>
<span data-ttu-id="20741-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="20741-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20741-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="20741-123">-NoWait</span></span>
<span data-ttu-id="20741-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="20741-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="20741-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20741-125">-PassThru</span></span>
<span data-ttu-id="20741-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="20741-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="20741-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20741-127">-ResourceGroupName</span></span>
<span data-ttu-id="20741-128">.</span><span class="sxs-lookup"><span data-stu-id="20741-128">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20741-129">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="20741-129">-RoleInstanceName</span></span>
<span data-ttu-id="20741-130">Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="20741-130">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20741-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20741-131">-SubscriptionId</span></span>
<span data-ttu-id="20741-132">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="20741-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="20741-133">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="20741-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20741-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20741-134">-Confirm</span></span>
<span data-ttu-id="20741-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20741-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20741-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20741-136">-WhatIf</span></span>
<span data-ttu-id="20741-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20741-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20741-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="20741-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20741-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20741-139">CommonParameters</span></span>
<span data-ttu-id="20741-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20741-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20741-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20741-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20741-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20741-142">INPUTS</span></span>

### <span data-ttu-id="20741-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="20741-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="20741-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="20741-144">OUTPUTS</span></span>

### <span data-ttu-id="20741-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="20741-145">System.Boolean</span></span>

## <span data-ttu-id="20741-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="20741-146">NOTES</span></span>

<span data-ttu-id="20741-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="20741-147">ALIASES</span></span>

<span data-ttu-id="20741-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="20741-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20741-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="20741-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20741-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20741-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20741-151">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="20741-151">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20741-152">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="20741-152">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="20741-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="20741-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20741-154">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="20741-154">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="20741-155">`[RoleInstanceName <String>]`: Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="20741-155">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="20741-156">`[RoleName <String>]`: Название роли.</span><span class="sxs-lookup"><span data-stu-id="20741-156">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="20741-157">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="20741-157">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="20741-158">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="20741-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="20741-159">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="20741-159">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="20741-160">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="20741-160">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="20741-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20741-161">RELATED LINKS</span></span>

