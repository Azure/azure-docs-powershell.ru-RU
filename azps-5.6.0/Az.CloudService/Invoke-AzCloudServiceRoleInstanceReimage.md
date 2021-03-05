---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
ms.openlocfilehash: 644912b841475c660852adcda2cba320d9026618
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965059"
---
# <span data-ttu-id="aa4a9-101">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="aa4a9-101">Invoke-AzCloudServiceRoleInstanceReimage</span></span>

## <span data-ttu-id="aa4a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa4a9-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4a9-103">Асинхронная операция "Экземпляр роли Reimage" переустановит операционную систему для экземпляров ролей веб-ролей или сотрудников.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-103">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="aa4a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa4a9-104">SYNTAX</span></span>

### <span data-ttu-id="aa4a9-105">Reimage (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa4a9-105">Reimage (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aa4a9-106">ReimageViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aa4a9-106">ReimageViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aa4a9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa4a9-107">DESCRIPTION</span></span>
<span data-ttu-id="aa4a9-108">Асинхронная операция "Экземпляр роли Reimage" переустановит операционную систему для экземпляров ролей веб-ролей или сотрудников.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-108">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="aa4a9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa4a9-109">EXAMPLES</span></span>

### <span data-ttu-id="aa4a9-110">Пример 1. Повторное экземпляр роли облачной службы</span><span class="sxs-lookup"><span data-stu-id="aa4a9-110">Example 1: Reimage role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="aa4a9-111">Эта команда переимежает экземпляр роли ContosoFrontEnd_IN_0 облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-111">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="aa4a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa4a9-112">PARAMETERS</span></span>

### <span data-ttu-id="aa4a9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa4a9-113">-AsJob</span></span>
<span data-ttu-id="aa4a9-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="aa4a9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="aa4a9-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="aa4a9-115">-CloudServiceName</span></span>
<span data-ttu-id="aa4a9-116">.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4a9-117">-DefaultProfile</span></span>
<span data-ttu-id="aa4a9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa4a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa4a9-119">-InputObject</span></span>
<span data-ttu-id="aa4a9-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4a9-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aa4a9-121">-NoWait</span></span>
<span data-ttu-id="aa4a9-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="aa4a9-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aa4a9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa4a9-123">-PassThru</span></span>
<span data-ttu-id="aa4a9-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aa4a9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa4a9-125">-ResourceGroupName</span></span>
<span data-ttu-id="aa4a9-126">.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4a9-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="aa4a9-127">-RoleInstanceName</span></span>
<span data-ttu-id="aa4a9-128">Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4a9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa4a9-129">-SubscriptionId</span></span>
<span data-ttu-id="aa4a9-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aa4a9-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4a9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa4a9-132">-Confirm</span></span>
<span data-ttu-id="aa4a9-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa4a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa4a9-134">-WhatIf</span></span>
<span data-ttu-id="aa4a9-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa4a9-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa4a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4a9-137">CommonParameters</span></span>
<span data-ttu-id="aa4a9-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4a9-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa4a9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4a9-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa4a9-140">INPUTS</span></span>

### <span data-ttu-id="aa4a9-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="aa4a9-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="aa4a9-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa4a9-142">OUTPUTS</span></span>

### <span data-ttu-id="aa4a9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa4a9-143">System.Boolean</span></span>

## <span data-ttu-id="aa4a9-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa4a9-144">NOTES</span></span>

<span data-ttu-id="aa4a9-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="aa4a9-145">ALIASES</span></span>

<span data-ttu-id="aa4a9-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="aa4a9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa4a9-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa4a9-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa4a9-149">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="aa4a9-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa4a9-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="aa4a9-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="aa4a9-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="aa4a9-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa4a9-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="aa4a9-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="aa4a9-153">`[RoleInstanceName <String>]`: имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="aa4a9-154">`[RoleName <String>]`: название роли.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="aa4a9-155">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="aa4a9-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="aa4a9-157">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="aa4a9-158">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="aa4a9-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa4a9-159">RELATED LINKS</span></span>

