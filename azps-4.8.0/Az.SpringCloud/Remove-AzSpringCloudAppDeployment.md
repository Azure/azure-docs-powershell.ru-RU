---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f91747d7c48521a9a14906cd873df564fadc4aa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080262"
---
# <span data-ttu-id="48ea7-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="48ea7-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="48ea7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="48ea7-103">Операция удаления развертывания.</span><span class="sxs-lookup"><span data-stu-id="48ea7-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="48ea7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48ea7-104">SYNTAX</span></span>

### <span data-ttu-id="48ea7-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48ea7-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="48ea7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="48ea7-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="48ea7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48ea7-107">DESCRIPTION</span></span>
<span data-ttu-id="48ea7-108">Операция удаления развертывания.</span><span class="sxs-lookup"><span data-stu-id="48ea7-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="48ea7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48ea7-109">EXAMPLES</span></span>

### <span data-ttu-id="48ea7-110">Пример 1: удаление пружины с облачным развертыванием по имени.</span><span class="sxs-lookup"><span data-stu-id="48ea7-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="48ea7-111">Удалите подвесной облачное развертывание по имени.</span><span class="sxs-lookup"><span data-stu-id="48ea7-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="48ea7-112">Пример 2: удаление весны развертывание в облаке из канала.</span><span class="sxs-lookup"><span data-stu-id="48ea7-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="48ea7-113">Удалите с канала пружинное развертывание.</span><span class="sxs-lookup"><span data-stu-id="48ea7-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="48ea7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48ea7-114">PARAMETERS</span></span>

### <span data-ttu-id="48ea7-115">-Имя_приложения</span><span class="sxs-lookup"><span data-stu-id="48ea7-115">-AppName</span></span>
<span data-ttu-id="48ea7-116">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="48ea7-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="48ea7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ea7-117">-DefaultProfile</span></span>
<span data-ttu-id="48ea7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48ea7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48ea7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48ea7-119">-InputObject</span></span>
<span data-ttu-id="48ea7-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="48ea7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="48ea7-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="48ea7-121">-Name</span></span>
<span data-ttu-id="48ea7-122">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="48ea7-122">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="48ea7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48ea7-123">-PassThru</span></span>
<span data-ttu-id="48ea7-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="48ea7-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="48ea7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ea7-125">-ResourceGroupName</span></span>
<span data-ttu-id="48ea7-126">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="48ea7-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="48ea7-127">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="48ea7-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="48ea7-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="48ea7-128">-ServiceName</span></span>
<span data-ttu-id="48ea7-129">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="48ea7-129">The name of the Service resource.</span></span>

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

### <span data-ttu-id="48ea7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48ea7-130">-SubscriptionId</span></span>
<span data-ttu-id="48ea7-131">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="48ea7-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="48ea7-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="48ea7-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="48ea7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48ea7-133">-Confirm</span></span>
<span data-ttu-id="48ea7-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48ea7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48ea7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48ea7-135">-WhatIf</span></span>
<span data-ttu-id="48ea7-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48ea7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48ea7-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48ea7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48ea7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ea7-138">CommonParameters</span></span>
<span data-ttu-id="48ea7-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48ea7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ea7-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48ea7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ea7-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48ea7-141">INPUTS</span></span>

### <span data-ttu-id="48ea7-142">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="48ea7-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="48ea7-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48ea7-143">OUTPUTS</span></span>

### <span data-ttu-id="48ea7-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48ea7-144">System.Boolean</span></span>

## <span data-ttu-id="48ea7-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="48ea7-145">NOTES</span></span>

<span data-ttu-id="48ea7-146">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="48ea7-146">ALIASES</span></span>

<span data-ttu-id="48ea7-147">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="48ea7-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48ea7-148">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="48ea7-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48ea7-149">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48ea7-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48ea7-150">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="48ea7-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48ea7-151">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="48ea7-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="48ea7-152">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="48ea7-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="48ea7-153">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="48ea7-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="48ea7-154">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="48ea7-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="48ea7-155">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="48ea7-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="48ea7-156">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="48ea7-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48ea7-157">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="48ea7-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="48ea7-158">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="48ea7-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="48ea7-159">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="48ea7-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="48ea7-160">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="48ea7-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="48ea7-161">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="48ea7-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="48ea7-162">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="48ea7-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="48ea7-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48ea7-163">RELATED LINKS</span></span>

