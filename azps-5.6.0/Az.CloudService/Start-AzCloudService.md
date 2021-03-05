---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/start-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Start-AzCloudService.md
ms.openlocfilehash: 7bbd639c670112a227e90ee1f9a4b07171673fbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986166"
---
# <span data-ttu-id="60e29-101">Start-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="60e29-101">Start-AzCloudService</span></span>

## <span data-ttu-id="60e29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60e29-102">SYNOPSIS</span></span>
<span data-ttu-id="60e29-103">Запускает облачную службу.</span><span class="sxs-lookup"><span data-stu-id="60e29-103">Starts the cloud service.</span></span>

## <span data-ttu-id="60e29-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60e29-104">SYNTAX</span></span>

### <span data-ttu-id="60e29-105">Начало (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60e29-105">Start (Default)</span></span>
```
Start-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="60e29-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="60e29-106">StartViaIdentity</span></span>
```
Start-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60e29-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60e29-107">DESCRIPTION</span></span>
<span data-ttu-id="60e29-108">Запускает облачную службу.</span><span class="sxs-lookup"><span data-stu-id="60e29-108">Starts the cloud service.</span></span>

## <span data-ttu-id="60e29-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60e29-109">EXAMPLES</span></span>

### <span data-ttu-id="60e29-110">Пример 1. Запуск облачной службы</span><span class="sxs-lookup"><span data-stu-id="60e29-110">Example 1: Start cloud service</span></span>
```powershell
PS C:\> Start-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="60e29-111">Эта команда запускает все экземпляры ролей, которые относятся к облачной службе ContosoCS.</span><span class="sxs-lookup"><span data-stu-id="60e29-111">This command starts all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="60e29-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60e29-112">PARAMETERS</span></span>

### <span data-ttu-id="60e29-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60e29-113">-AsJob</span></span>
<span data-ttu-id="60e29-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="60e29-114">Run the command as a job</span></span>

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

### <span data-ttu-id="60e29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e29-115">-DefaultProfile</span></span>
<span data-ttu-id="60e29-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60e29-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e29-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60e29-117">-InputObject</span></span>
<span data-ttu-id="60e29-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="60e29-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60e29-119">-Name</span><span class="sxs-lookup"><span data-stu-id="60e29-119">-Name</span></span>
<span data-ttu-id="60e29-120">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="60e29-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e29-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="60e29-121">-NoWait</span></span>
<span data-ttu-id="60e29-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="60e29-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="60e29-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60e29-123">-PassThru</span></span>
<span data-ttu-id="60e29-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="60e29-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="60e29-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60e29-125">-ResourceGroupName</span></span>
<span data-ttu-id="60e29-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60e29-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e29-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60e29-127">-SubscriptionId</span></span>
<span data-ttu-id="60e29-128">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="60e29-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="60e29-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="60e29-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e29-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60e29-130">-Confirm</span></span>
<span data-ttu-id="60e29-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="60e29-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e29-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e29-132">-WhatIf</span></span>
<span data-ttu-id="60e29-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60e29-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60e29-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="60e29-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60e29-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e29-135">CommonParameters</span></span>
<span data-ttu-id="60e29-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60e29-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e29-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60e29-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e29-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60e29-138">INPUTS</span></span>

### <span data-ttu-id="60e29-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="60e29-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="60e29-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60e29-140">OUTPUTS</span></span>

### <span data-ttu-id="60e29-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60e29-141">System.Boolean</span></span>

## <span data-ttu-id="60e29-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60e29-142">NOTES</span></span>

<span data-ttu-id="60e29-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="60e29-143">ALIASES</span></span>

<span data-ttu-id="60e29-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="60e29-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60e29-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="60e29-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60e29-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60e29-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60e29-147">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="60e29-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60e29-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="60e29-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="60e29-149">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="60e29-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60e29-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="60e29-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="60e29-151">`[RoleInstanceName <String>]`: имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="60e29-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="60e29-152">`[RoleName <String>]`: название роли.</span><span class="sxs-lookup"><span data-stu-id="60e29-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="60e29-153">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="60e29-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="60e29-154">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="60e29-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="60e29-155">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="60e29-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="60e29-156">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="60e29-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="60e29-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60e29-157">RELATED LINKS</span></span>

