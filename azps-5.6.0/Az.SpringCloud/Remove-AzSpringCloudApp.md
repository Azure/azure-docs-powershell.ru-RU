---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: c6dccbaa5e398d5d00b02a28cc8942b9e5264859
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977763"
---
# <span data-ttu-id="3f6b9-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="3f6b9-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="3f6b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6b9-103">Операция удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-103">Operation to delete an App.</span></span>

## <span data-ttu-id="3f6b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f6b9-104">SYNTAX</span></span>

### <span data-ttu-id="3f6b9-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f6b9-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3f6b9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f6b9-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f6b9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f6b9-107">DESCRIPTION</span></span>
<span data-ttu-id="3f6b9-108">Операция удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-108">Operation to delete an App.</span></span>

## <span data-ttu-id="3f6b9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f6b9-109">EXAMPLES</span></span>

### <span data-ttu-id="3f6b9-110">Пример 1. Удаление приложения Spring Cloud По имени.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="3f6b9-111">Удаление приложения Spring Cloud App по имени.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="3f6b9-112">Пример 2. Удаление приложения "Весенние облака" из трубы.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="3f6b9-113">Удалите приложение "Весенний облако" из трубы.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="3f6b9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f6b9-114">PARAMETERS</span></span>

### <span data-ttu-id="3f6b9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f6b9-115">-AsJob</span></span>
<span data-ttu-id="3f6b9-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3f6b9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3f6b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6b9-117">-DefaultProfile</span></span>
<span data-ttu-id="3f6b9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f6b9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f6b9-119">-InputObject</span></span>
<span data-ttu-id="3f6b9-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3f6b9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3f6b9-121">-Name</span></span>
<span data-ttu-id="3f6b9-122">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6b9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3f6b9-123">-NoWait</span></span>
<span data-ttu-id="3f6b9-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="3f6b9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3f6b9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f6b9-125">-PassThru</span></span>
<span data-ttu-id="3f6b9-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3f6b9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f6b9-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f6b9-128">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3f6b9-129">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3f6b9-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3f6b9-130">-ServiceName</span></span>
<span data-ttu-id="3f6b9-131">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="3f6b9-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f6b9-132">-SubscriptionId</span></span>
<span data-ttu-id="3f6b9-133">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3f6b9-134">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3f6b9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f6b9-135">-Confirm</span></span>
<span data-ttu-id="3f6b9-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f6b9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f6b9-137">-WhatIf</span></span>
<span data-ttu-id="3f6b9-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f6b9-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f6b9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6b9-140">CommonParameters</span></span>
<span data-ttu-id="3f6b9-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6b9-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f6b9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6b9-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f6b9-143">INPUTS</span></span>

### <span data-ttu-id="3f6b9-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="3f6b9-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="3f6b9-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f6b9-145">OUTPUTS</span></span>

### <span data-ttu-id="3f6b9-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f6b9-146">System.Boolean</span></span>

## <span data-ttu-id="3f6b9-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f6b9-147">NOTES</span></span>

<span data-ttu-id="3f6b9-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3f6b9-148">ALIASES</span></span>

<span data-ttu-id="3f6b9-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3f6b9-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f6b9-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f6b9-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f6b9-152">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="3f6b9-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f6b9-153">`[AppName <String>]`: Название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="3f6b9-154">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="3f6b9-155">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="3f6b9-156">`[DeploymentName <String>]`: Название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="3f6b9-157">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="3f6b9-158">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="3f6b9-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f6b9-159">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="3f6b9-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="3f6b9-160">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3f6b9-161">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3f6b9-162">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="3f6b9-163">`[SubscriptionId <String>]`. Получает ИД подписки, однозначно определяя подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="3f6b9-164">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="3f6b9-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3f6b9-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f6b9-165">RELATED LINKS</span></span>

