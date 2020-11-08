---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/restart-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Restart-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 859ea1febad82dbb09e88debe3f825feab18b1c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235326"
---
# <span data-ttu-id="d67d0-101">Restart-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="d67d0-101">Restart-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="d67d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d67d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d67d0-103">Перезапустите развертывание.</span><span class="sxs-lookup"><span data-stu-id="d67d0-103">Restart the deployment.</span></span>

## <span data-ttu-id="d67d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d67d0-104">SYNTAX</span></span>

### <span data-ttu-id="d67d0-105">Перезагрузка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d67d0-105">Restart (Default)</span></span>
```
Restart-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d67d0-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d67d0-106">RestartViaIdentity</span></span>
```
Restart-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d67d0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d67d0-107">DESCRIPTION</span></span>
<span data-ttu-id="d67d0-108">Перезапустите развертывание.</span><span class="sxs-lookup"><span data-stu-id="d67d0-108">Restart the deployment.</span></span>

## <span data-ttu-id="d67d0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d67d0-109">EXAMPLES</span></span>

### <span data-ttu-id="d67d0-110">Пример 1: Перезагрузите пружинную облачную службу по имени.</span><span class="sxs-lookup"><span data-stu-id="d67d0-110">Example 1: Restart Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Restart-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="d67d0-111">Перезапустите пружинную облачную службу по имени.</span><span class="sxs-lookup"><span data-stu-id="d67d0-111">Restart Spring Cloud Service by name.</span></span>

### <span data-ttu-id="d67d0-112">Пример 2: Перезагрузите пружинную облачную службу из канала.</span><span class="sxs-lookup"><span data-stu-id="d67d0-112">Example 2: Restart Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Restart-AzSpringCloud
```

<span data-ttu-id="d67d0-113">Перезапустите пружинную облачную службу из канала.</span><span class="sxs-lookup"><span data-stu-id="d67d0-113">Restart Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="d67d0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d67d0-114">PARAMETERS</span></span>

### <span data-ttu-id="d67d0-115">-Имя_приложения</span><span class="sxs-lookup"><span data-stu-id="d67d0-115">-AppName</span></span>
<span data-ttu-id="d67d0-116">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="d67d0-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="d67d0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d67d0-117">-AsJob</span></span>
<span data-ttu-id="d67d0-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d67d0-118">Run the command as a job</span></span>

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

### <span data-ttu-id="d67d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67d0-119">-DefaultProfile</span></span>
<span data-ttu-id="d67d0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d67d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d67d0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d67d0-121">-InputObject</span></span>
<span data-ttu-id="d67d0-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d67d0-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d67d0-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d67d0-123">-Name</span></span>
<span data-ttu-id="d67d0-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="d67d0-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67d0-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="d67d0-125">-NoWait</span></span>
<span data-ttu-id="d67d0-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="d67d0-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d67d0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d67d0-127">-PassThru</span></span>
<span data-ttu-id="d67d0-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d67d0-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d67d0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67d0-129">-ResourceGroupName</span></span>
<span data-ttu-id="d67d0-130">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="d67d0-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d67d0-131">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d67d0-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d67d0-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d67d0-132">-ServiceName</span></span>
<span data-ttu-id="d67d0-133">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="d67d0-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d67d0-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d67d0-134">-SubscriptionId</span></span>
<span data-ttu-id="d67d0-135">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d67d0-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d67d0-136">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d67d0-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d67d0-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d67d0-137">-Confirm</span></span>
<span data-ttu-id="d67d0-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d67d0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d67d0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d67d0-139">-WhatIf</span></span>
<span data-ttu-id="d67d0-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d67d0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d67d0-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d67d0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d67d0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67d0-142">CommonParameters</span></span>
<span data-ttu-id="d67d0-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d67d0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67d0-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d67d0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67d0-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d67d0-145">INPUTS</span></span>

### <span data-ttu-id="d67d0-146">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d67d0-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d67d0-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d67d0-147">OUTPUTS</span></span>

### <span data-ttu-id="d67d0-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d67d0-148">System.Boolean</span></span>

## <span data-ttu-id="d67d0-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="d67d0-149">NOTES</span></span>

<span data-ttu-id="d67d0-150">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d67d0-150">ALIASES</span></span>

<span data-ttu-id="d67d0-151">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d67d0-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d67d0-152">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d67d0-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d67d0-153">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d67d0-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d67d0-154">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d67d0-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d67d0-155">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="d67d0-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d67d0-156">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="d67d0-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d67d0-157">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="d67d0-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d67d0-158">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="d67d0-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d67d0-159">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="d67d0-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d67d0-160">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d67d0-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d67d0-161">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="d67d0-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d67d0-162">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="d67d0-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d67d0-163">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d67d0-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d67d0-164">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="d67d0-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d67d0-165">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d67d0-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d67d0-166">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d67d0-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d67d0-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d67d0-167">RELATED LINKS</span></span>

