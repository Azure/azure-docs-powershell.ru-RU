---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/stop-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
ms.openlocfilehash: 1417cc797935a532decf886f0c814ef32deee3aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233468"
---
# <span data-ttu-id="c15e5-101">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="c15e5-101">Stop-AzCloudService</span></span>

## <span data-ttu-id="c15e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c15e5-102">SYNOPSIS</span></span>
<span data-ttu-id="c15e5-103">Отключите облачную службу.</span><span class="sxs-lookup"><span data-stu-id="c15e5-103">Power off the cloud service.</span></span>
<span data-ttu-id="c15e5-104">Обратите внимание на то, что ресурсы все еще закреплены, и с вас взимается плата за ресурсы.</span><span class="sxs-lookup"><span data-stu-id="c15e5-104">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="c15e5-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c15e5-105">SYNTAX</span></span>

### <span data-ttu-id="c15e5-106">PowerOff (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c15e5-106">PowerOff (Default)</span></span>
```
Stop-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c15e5-107">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c15e5-107">PowerOffViaIdentity</span></span>
```
Stop-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c15e5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c15e5-108">DESCRIPTION</span></span>
<span data-ttu-id="c15e5-109">Отключите облачную службу.</span><span class="sxs-lookup"><span data-stu-id="c15e5-109">Power off the cloud service.</span></span>
<span data-ttu-id="c15e5-110">Обратите внимание на то, что ресурсы все еще закреплены, и за них взимается плата.</span><span class="sxs-lookup"><span data-stu-id="c15e5-110">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="c15e5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c15e5-111">EXAMPLES</span></span>

### <span data-ttu-id="c15e5-112">Пример 1. Остановка облачной службы</span><span class="sxs-lookup"><span data-stu-id="c15e5-112">Example 1: Stop cloud service</span></span>
```powershell
PS C:\> Stop-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="c15e5-113">Эта команда останавливает все экземпляры ролей, которые относятся к облачной службе ContosoCS.</span><span class="sxs-lookup"><span data-stu-id="c15e5-113">This command stops all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="c15e5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c15e5-114">PARAMETERS</span></span>

### <span data-ttu-id="c15e5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c15e5-115">-AsJob</span></span>
<span data-ttu-id="c15e5-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c15e5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c15e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c15e5-117">-DefaultProfile</span></span>
<span data-ttu-id="c15e5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c15e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c15e5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c15e5-119">-InputObject</span></span>
<span data-ttu-id="c15e5-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c15e5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c15e5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c15e5-121">-Name</span></span>
<span data-ttu-id="c15e5-122">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="c15e5-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c15e5-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c15e5-123">-NoWait</span></span>
<span data-ttu-id="c15e5-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="c15e5-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c15e5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c15e5-125">-PassThru</span></span>
<span data-ttu-id="c15e5-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="c15e5-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c15e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c15e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="c15e5-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c15e5-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c15e5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c15e5-129">-SubscriptionId</span></span>
<span data-ttu-id="c15e5-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c15e5-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c15e5-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="c15e5-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c15e5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c15e5-132">-Confirm</span></span>
<span data-ttu-id="c15e5-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c15e5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c15e5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c15e5-134">-WhatIf</span></span>
<span data-ttu-id="c15e5-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c15e5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c15e5-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c15e5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c15e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15e5-137">CommonParameters</span></span>
<span data-ttu-id="c15e5-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c15e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15e5-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c15e5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15e5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c15e5-140">INPUTS</span></span>

### <span data-ttu-id="c15e5-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="c15e5-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="c15e5-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c15e5-142">OUTPUTS</span></span>

### <span data-ttu-id="c15e5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c15e5-143">System.Boolean</span></span>

## <span data-ttu-id="c15e5-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c15e5-144">NOTES</span></span>

<span data-ttu-id="c15e5-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c15e5-145">ALIASES</span></span>

<span data-ttu-id="c15e5-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c15e5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c15e5-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c15e5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c15e5-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c15e5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c15e5-149">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="c15e5-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c15e5-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c15e5-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="c15e5-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="c15e5-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c15e5-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c15e5-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="c15e5-153">`[RoleInstanceName <String>]`: имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="c15e5-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="c15e5-154">`[RoleName <String>]`: название роли.</span><span class="sxs-lookup"><span data-stu-id="c15e5-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="c15e5-155">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c15e5-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c15e5-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="c15e5-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c15e5-157">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="c15e5-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="c15e5-158">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="c15e5-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="c15e5-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c15e5-159">RELATED LINKS</span></span>

