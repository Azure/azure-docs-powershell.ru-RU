---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: e1fff88e6d591f7ffd3d7b602e8d60febf5b1c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978099"
---
# <span data-ttu-id="247dc-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="247dc-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="247dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="247dc-102">SYNOPSIS</span></span>
<span data-ttu-id="247dc-103">Операция удаления развертывания.</span><span class="sxs-lookup"><span data-stu-id="247dc-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="247dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="247dc-104">SYNTAX</span></span>

### <span data-ttu-id="247dc-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="247dc-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="247dc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="247dc-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="247dc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="247dc-107">DESCRIPTION</span></span>
<span data-ttu-id="247dc-108">Операция удаления развертывания.</span><span class="sxs-lookup"><span data-stu-id="247dc-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="247dc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="247dc-109">EXAMPLES</span></span>

### <span data-ttu-id="247dc-110">Пример 1. Удаление источника "Весенний облачный развертывание" по имени.</span><span class="sxs-lookup"><span data-stu-id="247dc-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="247dc-111">Удалить по имени развертывание в облаке "Весенний".</span><span class="sxs-lookup"><span data-stu-id="247dc-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="247dc-112">Пример 2. Удаление источника "Весенние облачные развертывания" из трубы.</span><span class="sxs-lookup"><span data-stu-id="247dc-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="247dc-113">Удалите весенние облачные развертывания из трубы.</span><span class="sxs-lookup"><span data-stu-id="247dc-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="247dc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="247dc-114">PARAMETERS</span></span>

### <span data-ttu-id="247dc-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="247dc-115">-AppName</span></span>
<span data-ttu-id="247dc-116">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="247dc-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247dc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="247dc-117">-AsJob</span></span>
<span data-ttu-id="247dc-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="247dc-118">Run the command as a job</span></span>

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

### <span data-ttu-id="247dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="247dc-119">-DefaultProfile</span></span>
<span data-ttu-id="247dc-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="247dc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="247dc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="247dc-121">-InputObject</span></span>
<span data-ttu-id="247dc-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="247dc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="247dc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="247dc-123">-Name</span></span>
<span data-ttu-id="247dc-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="247dc-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247dc-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="247dc-125">-NoWait</span></span>
<span data-ttu-id="247dc-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="247dc-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="247dc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="247dc-127">-PassThru</span></span>
<span data-ttu-id="247dc-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="247dc-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="247dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="247dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="247dc-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="247dc-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="247dc-131">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="247dc-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247dc-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="247dc-132">-ServiceName</span></span>
<span data-ttu-id="247dc-133">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="247dc-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247dc-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="247dc-134">-SubscriptionId</span></span>
<span data-ttu-id="247dc-135">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="247dc-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="247dc-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="247dc-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247dc-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="247dc-137">-Confirm</span></span>
<span data-ttu-id="247dc-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="247dc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="247dc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="247dc-139">-WhatIf</span></span>
<span data-ttu-id="247dc-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="247dc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="247dc-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="247dc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="247dc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247dc-142">CommonParameters</span></span>
<span data-ttu-id="247dc-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="247dc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247dc-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="247dc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247dc-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="247dc-145">INPUTS</span></span>

### <span data-ttu-id="247dc-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="247dc-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="247dc-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="247dc-147">OUTPUTS</span></span>

### <span data-ttu-id="247dc-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="247dc-148">System.Boolean</span></span>

## <span data-ttu-id="247dc-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="247dc-149">NOTES</span></span>

<span data-ttu-id="247dc-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="247dc-150">ALIASES</span></span>

<span data-ttu-id="247dc-151">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="247dc-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="247dc-152">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="247dc-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="247dc-153">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="247dc-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="247dc-154">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="247dc-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="247dc-155">`[AppName <String>]`: Название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="247dc-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="247dc-156">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="247dc-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="247dc-157">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="247dc-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="247dc-158">`[DeploymentName <String>]`: название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="247dc-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="247dc-159">`[DomainName <String>]`: имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="247dc-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="247dc-160">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="247dc-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="247dc-161">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="247dc-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="247dc-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="247dc-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="247dc-163">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="247dc-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="247dc-164">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="247dc-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="247dc-165">`[SubscriptionId <String>]`. Получает ИД подписки, однозначно определяя подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="247dc-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="247dc-166">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="247dc-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="247dc-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="247dc-167">RELATED LINKS</span></span>

