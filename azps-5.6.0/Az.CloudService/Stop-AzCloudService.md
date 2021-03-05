---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/stop-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
ms.openlocfilehash: 539106e979babd1df41ca2505a2978132e825b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007219"
---
# <span data-ttu-id="3a435-101">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="3a435-101">Stop-AzCloudService</span></span>

## <span data-ttu-id="3a435-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a435-102">SYNOPSIS</span></span>
<span data-ttu-id="3a435-103">Отключите облачную службу.</span><span class="sxs-lookup"><span data-stu-id="3a435-103">Power off the cloud service.</span></span>
<span data-ttu-id="3a435-104">Обратите внимание на то, что ресурсы все еще закреплены, и за них взимается плата.</span><span class="sxs-lookup"><span data-stu-id="3a435-104">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="3a435-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3a435-105">SYNTAX</span></span>

### <span data-ttu-id="3a435-106">PowerOff (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a435-106">PowerOff (Default)</span></span>
```
Stop-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3a435-107">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a435-107">PowerOffViaIdentity</span></span>
```
Stop-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3a435-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a435-108">DESCRIPTION</span></span>
<span data-ttu-id="3a435-109">Отключите облачную службу.</span><span class="sxs-lookup"><span data-stu-id="3a435-109">Power off the cloud service.</span></span>
<span data-ttu-id="3a435-110">Обратите внимание на то, что ресурсы все еще закреплены, и за них взимается плата.</span><span class="sxs-lookup"><span data-stu-id="3a435-110">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="3a435-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3a435-111">EXAMPLES</span></span>

### <span data-ttu-id="3a435-112">Пример 1. Остановка облачной службы</span><span class="sxs-lookup"><span data-stu-id="3a435-112">Example 1: Stop cloud service</span></span>
```powershell
PS C:\> Stop-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="3a435-113">Эта команда останавливает все экземпляры ролей, которые относятся к облачной службе ContosoCS.</span><span class="sxs-lookup"><span data-stu-id="3a435-113">This command stops all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="3a435-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a435-114">PARAMETERS</span></span>

### <span data-ttu-id="3a435-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a435-115">-AsJob</span></span>
<span data-ttu-id="3a435-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3a435-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3a435-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a435-117">-DefaultProfile</span></span>
<span data-ttu-id="3a435-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a435-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a435-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a435-119">-InputObject</span></span>
<span data-ttu-id="3a435-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3a435-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a435-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3a435-121">-Name</span></span>
<span data-ttu-id="3a435-122">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="3a435-122">Name of the cloud service.</span></span>

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

### <span data-ttu-id="3a435-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3a435-123">-NoWait</span></span>
<span data-ttu-id="3a435-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="3a435-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a435-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a435-125">-PassThru</span></span>
<span data-ttu-id="3a435-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="3a435-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3a435-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a435-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a435-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a435-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="3a435-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a435-129">-SubscriptionId</span></span>
<span data-ttu-id="3a435-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a435-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3a435-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="3a435-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3a435-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a435-132">-Confirm</span></span>
<span data-ttu-id="3a435-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a435-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a435-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a435-134">-WhatIf</span></span>
<span data-ttu-id="3a435-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a435-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a435-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3a435-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a435-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a435-137">CommonParameters</span></span>
<span data-ttu-id="3a435-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a435-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a435-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a435-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a435-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a435-140">INPUTS</span></span>

### <span data-ttu-id="3a435-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="3a435-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="3a435-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a435-142">OUTPUTS</span></span>

### <span data-ttu-id="3a435-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a435-143">System.Boolean</span></span>

## <span data-ttu-id="3a435-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3a435-144">NOTES</span></span>

<span data-ttu-id="3a435-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3a435-145">ALIASES</span></span>

<span data-ttu-id="3a435-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3a435-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a435-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3a435-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a435-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a435-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a435-149">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="3a435-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a435-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="3a435-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="3a435-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="3a435-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a435-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="3a435-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="3a435-153">`[RoleInstanceName <String>]`: Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="3a435-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="3a435-154">`[RoleName <String>]`: Название роли.</span><span class="sxs-lookup"><span data-stu-id="3a435-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="3a435-155">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a435-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3a435-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="3a435-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3a435-157">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="3a435-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="3a435-158">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="3a435-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="3a435-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a435-159">RELATED LINKS</span></span>

