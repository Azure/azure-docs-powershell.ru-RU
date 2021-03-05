---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 0de600b2b21d634e85b4ed0266a3b72c95266f44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963608"
---
# <span data-ttu-id="4e6d5-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="4e6d5-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="4e6d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6d5-103">Остановите развертывание.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-103">Stop the deployment.</span></span>

## <span data-ttu-id="4e6d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e6d5-104">SYNTAX</span></span>

### <span data-ttu-id="4e6d5-105">Остановка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e6d5-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e6d5-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e6d5-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e6d5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e6d5-107">DESCRIPTION</span></span>
<span data-ttu-id="4e6d5-108">Остановите развертывание.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-108">Stop the deployment.</span></span>

## <span data-ttu-id="4e6d5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e6d5-109">EXAMPLES</span></span>

### <span data-ttu-id="4e6d5-110">Пример 1. Остановка службы "Весенние облачные службы" по имени.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="4e6d5-111">Остановка службы "Весенние облачные службы" по имени.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="4e6d5-112">Пример 2. Остановка службы "Весенние облачные службы" из канала.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="4e6d5-113">Остановка службы "Весенние облачные службы" из трубы.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="4e6d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e6d5-114">PARAMETERS</span></span>

### <span data-ttu-id="4e6d5-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="4e6d5-115">-AppName</span></span>
<span data-ttu-id="4e6d5-116">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e6d5-117">-AsJob</span></span>
<span data-ttu-id="4e6d5-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4e6d5-118">Run the command as a job</span></span>

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

### <span data-ttu-id="4e6d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6d5-119">-DefaultProfile</span></span>
<span data-ttu-id="4e6d5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e6d5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e6d5-121">-InputObject</span></span>
<span data-ttu-id="4e6d5-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4e6d5-123">-Name</span></span>
<span data-ttu-id="4e6d5-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d5-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4e6d5-125">-NoWait</span></span>
<span data-ttu-id="4e6d5-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="4e6d5-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4e6d5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e6d5-127">-PassThru</span></span>
<span data-ttu-id="4e6d5-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4e6d5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e6d5-129">-ResourceGroupName</span></span>
<span data-ttu-id="4e6d5-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4e6d5-131">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d5-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4e6d5-132">-ServiceName</span></span>
<span data-ttu-id="4e6d5-133">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d5-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e6d5-134">-SubscriptionId</span></span>
<span data-ttu-id="4e6d5-135">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e6d5-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6d5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e6d5-137">-Confirm</span></span>
<span data-ttu-id="4e6d5-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e6d5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e6d5-139">-WhatIf</span></span>
<span data-ttu-id="4e6d5-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e6d5-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e6d5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6d5-142">CommonParameters</span></span>
<span data-ttu-id="4e6d5-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6d5-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e6d5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6d5-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e6d5-145">INPUTS</span></span>

### <span data-ttu-id="4e6d5-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="4e6d5-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="4e6d5-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e6d5-147">OUTPUTS</span></span>

### <span data-ttu-id="4e6d5-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4e6d5-148">System.Boolean</span></span>

## <span data-ttu-id="4e6d5-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e6d5-149">NOTES</span></span>

<span data-ttu-id="4e6d5-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4e6d5-150">ALIASES</span></span>

<span data-ttu-id="4e6d5-151">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4e6d5-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e6d5-152">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e6d5-153">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e6d5-154">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="4e6d5-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e6d5-155">`[AppName <String>]`: название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="4e6d5-156">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="4e6d5-157">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="4e6d5-158">`[DeploymentName <String>]`: название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="4e6d5-159">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="4e6d5-160">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="4e6d5-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e6d5-161">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="4e6d5-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="4e6d5-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4e6d5-163">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4e6d5-164">`[ServiceName <String>]`: Название ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="4e6d5-165">`[SubscriptionId <String>]`: получает ИД подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="4e6d5-166">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4e6d5-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e6d5-167">RELATED LINKS</span></span>

