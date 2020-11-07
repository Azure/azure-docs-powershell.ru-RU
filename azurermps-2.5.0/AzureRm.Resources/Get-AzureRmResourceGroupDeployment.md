---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 9da5ee691b440ee24933d658dec3c85b1a7c8ced
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913423"
---
# <span data-ttu-id="ad74c-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ad74c-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="ad74c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad74c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad74c-103">Возвращает развертывания в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad74c-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad74c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad74c-104">SYNTAX</span></span>

### <span data-ttu-id="ad74c-105">GetByResourceGroupDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad74c-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad74c-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ad74c-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad74c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad74c-107">DESCRIPTION</span></span>
<span data-ttu-id="ad74c-108">Командлет **Get-AzureRmResourceGroupDeployment** получает развертывание в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ad74c-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="ad74c-109">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="ad74c-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="ad74c-110">По умолчанию **Get-AzureRmResourceGroupDeployment** получает все развертывания для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad74c-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="ad74c-111">Ресурс Azure — это управляемая пользователем сущность Azure, например сервер базы данных, база данных или веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="ad74c-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="ad74c-112">Группа ресурсов Azure — это коллекция ресурсов Azure, развернутых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="ad74c-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="ad74c-113">Развертывание — это операция, которая делает ресурсы в группе ресурсов доступной для использования.</span><span class="sxs-lookup"><span data-stu-id="ad74c-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="ad74c-114">Дополнительные сведения о ресурсах Azure и группах ресурсов Azure можно найти в командлете New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ad74c-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="ad74c-115">Вы можете использовать этот командлет для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="ad74c-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="ad74c-116">Для отладки используйте этот командлет с командлетом Get-AzureRmLog.</span><span class="sxs-lookup"><span data-stu-id="ad74c-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="ad74c-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad74c-117">EXAMPLES</span></span>

### <span data-ttu-id="ad74c-118">Пример 1: получение всех развертываний для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ad74c-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="ad74c-119">Эта команда получает все развертывания для группы ресурсов ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="ad74c-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="ad74c-120">На выходе показано развертывание для блога WordPress, в котором был использован шаблон коллекции.</span><span class="sxs-lookup"><span data-stu-id="ad74c-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="ad74c-121">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="ad74c-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="ad74c-122">Эта команда получает развертывание DeployWebsite01 группы ресурсов ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="ad74c-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="ad74c-123">Вы можете присвоить имя развертыванию при создании с помощью командлетов **New-AzureRmResourceGroup** или **New-AzureRmResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="ad74c-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="ad74c-124">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="ad74c-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="ad74c-125">Пример 3: получение развертываний всех групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="ad74c-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="ad74c-126">Эта команда получает все группы ресурсов в подписке с помощью командлета Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ad74c-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="ad74c-127">Команда передает группы ресурсов в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ad74c-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ad74c-128">Текущий командлет получает все развертывания всех групп ресурсов в подписке и передает результаты в командлет Format-Table, чтобы отобразить значения свойств **ResourceGroupName** , **DeploymentName** и **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="ad74c-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="ad74c-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad74c-129">PARAMETERS</span></span>

### <span data-ttu-id="ad74c-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ad74c-130">-ApiVersion</span></span>
<span data-ttu-id="ad74c-131">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad74c-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ad74c-132">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad74c-132">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad74c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad74c-133">-DefaultProfile</span></span>
<span data-ttu-id="ad74c-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ad74c-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad74c-135">-ID</span><span class="sxs-lookup"><span data-stu-id="ad74c-135">-Id</span></span>
<span data-ttu-id="ad74c-136">Указывает идентификатор развертывания группы ресурсов, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ad74c-136">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad74c-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad74c-137">-Name</span></span>
<span data-ttu-id="ad74c-138">Указывает имя развертывания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ad74c-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="ad74c-139">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="ad74c-139">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad74c-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="ad74c-140">-Pre</span></span>
<span data-ttu-id="ad74c-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="ad74c-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ad74c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad74c-142">-ResourceGroupName</span></span>
<span data-ttu-id="ad74c-143">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad74c-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ad74c-144">Командлет получает развертывание для группы ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ad74c-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="ad74c-145">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="ad74c-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="ad74c-146">Этот параметр является обязательным, и вы можете указать только одну группу ресурсов в каждой команде.</span><span class="sxs-lookup"><span data-stu-id="ad74c-146">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad74c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad74c-147">CommonParameters</span></span>
<span data-ttu-id="ad74c-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad74c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad74c-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad74c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad74c-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad74c-150">INPUTS</span></span>

### <span data-ttu-id="ad74c-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="ad74c-151">None</span></span>

## <span data-ttu-id="ad74c-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad74c-152">OUTPUTS</span></span>

### <span data-ttu-id="ad74c-153">Microsoft. Azure. Commands. ResourceManagement. Models.</span><span class="sxs-lookup"><span data-stu-id="ad74c-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="ad74c-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ad74c-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="ad74c-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad74c-155">NOTES</span></span>

## <span data-ttu-id="ad74c-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad74c-156">RELATED LINKS</span></span>

[<span data-ttu-id="ad74c-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ad74c-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="ad74c-158">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ad74c-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="ad74c-159">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ad74c-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ad74c-160">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ad74c-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ad74c-161">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ad74c-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ad74c-162">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ad74c-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


