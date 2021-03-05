---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
ms.openlocfilehash: f184696dbcfce35bf6e52f889d2c787214330e70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985309"
---
# <span data-ttu-id="ad871-101">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="ad871-101">Restart-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="ad871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad871-102">SYNOPSIS</span></span>
<span data-ttu-id="ad871-103">Асинхронная операция "Экземпляр перезагрузки" запрашивает перезагрузку экземпляра роли в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="ad871-103">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="ad871-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad871-104">SYNTAX</span></span>

### <span data-ttu-id="ad871-105">Перезапуск (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad871-105">Restart (Default)</span></span>
```
Restart-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ad871-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ad871-106">RestartViaIdentity</span></span>
```
Restart-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ad871-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad871-107">DESCRIPTION</span></span>
<span data-ttu-id="ad871-108">Асинхронная операция "Экземпляр перезагрузки" запрашивает перезагрузку экземпляра роли в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="ad871-108">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="ad871-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad871-109">EXAMPLES</span></span>

### <span data-ttu-id="ad871-110">Пример 1. Перезапуск экземпляра роли облачной службы</span><span class="sxs-lookup"><span data-stu-id="ad871-110">Example 1: Restart role instance of a cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="ad871-111">Эта команда перезапустит экземпляр роли ContosoFrontEnd_IN_0 облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="ad871-111">This command restarts role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="ad871-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad871-112">PARAMETERS</span></span>

### <span data-ttu-id="ad871-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad871-113">-AsJob</span></span>
<span data-ttu-id="ad871-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ad871-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ad871-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="ad871-115">-CloudServiceName</span></span>
<span data-ttu-id="ad871-116">.</span><span class="sxs-lookup"><span data-stu-id="ad871-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad871-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad871-117">-DefaultProfile</span></span>
<span data-ttu-id="ad871-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad871-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad871-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad871-119">-InputObject</span></span>
<span data-ttu-id="ad871-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ad871-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad871-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ad871-121">-NoWait</span></span>
<span data-ttu-id="ad871-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ad871-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ad871-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad871-123">-PassThru</span></span>
<span data-ttu-id="ad871-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="ad871-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ad871-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad871-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad871-126">.</span><span class="sxs-lookup"><span data-stu-id="ad871-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad871-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="ad871-127">-RoleInstanceName</span></span>
<span data-ttu-id="ad871-128">Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="ad871-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad871-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad871-129">-SubscriptionId</span></span>
<span data-ttu-id="ad871-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad871-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ad871-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ad871-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad871-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad871-132">-Confirm</span></span>
<span data-ttu-id="ad871-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad871-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad871-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad871-134">-WhatIf</span></span>
<span data-ttu-id="ad871-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad871-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad871-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad871-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad871-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad871-137">CommonParameters</span></span>
<span data-ttu-id="ad871-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad871-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad871-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad871-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad871-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad871-140">INPUTS</span></span>

### <span data-ttu-id="ad871-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="ad871-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="ad871-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad871-142">OUTPUTS</span></span>

### <span data-ttu-id="ad871-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ad871-143">System.Boolean</span></span>

## <span data-ttu-id="ad871-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad871-144">NOTES</span></span>

<span data-ttu-id="ad871-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ad871-145">ALIASES</span></span>

<span data-ttu-id="ad871-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ad871-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad871-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ad871-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad871-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad871-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad871-149">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ad871-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad871-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ad871-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="ad871-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ad871-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad871-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ad871-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="ad871-153">`[RoleInstanceName <String>]`: имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="ad871-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="ad871-154">`[RoleName <String>]`: название роли.</span><span class="sxs-lookup"><span data-stu-id="ad871-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="ad871-155">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad871-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ad871-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ad871-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ad871-157">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="ad871-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="ad871-158">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="ad871-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="ad871-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad871-159">RELATED LINKS</span></span>

