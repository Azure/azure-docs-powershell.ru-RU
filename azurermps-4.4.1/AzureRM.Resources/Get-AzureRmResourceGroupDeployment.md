---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567082"
---
# <span data-ttu-id="13c4c-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="13c4c-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="13c4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="13c4c-103">Возвращает развертывания в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13c4c-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13c4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13c4c-104">SYNTAX</span></span>

### <span data-ttu-id="13c4c-105">Заданный параметр имени развертывания.</span><span class="sxs-lookup"><span data-stu-id="13c4c-105">The deployment name parameter set.</span></span> <span data-ttu-id="13c4c-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="13c4c-106">(Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13c4c-107">Заданный параметр идентификатора развертывания.</span><span class="sxs-lookup"><span data-stu-id="13c4c-107">The deployment Id parameter set.</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13c4c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13c4c-108">DESCRIPTION</span></span>
<span data-ttu-id="13c4c-109">Командлет **Get-AzureRmResourceGroupDeployment** получает развертывание в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="13c4c-109">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="13c4c-110">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="13c4c-110">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="13c4c-111">По умолчанию **Get-AzureRmResourceGroupDeployment** получает все развертывания для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13c4c-111">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="13c4c-112">Ресурс Azure — это управляемая пользователем сущность Azure, например сервер базы данных, база данных или веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="13c4c-112">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="13c4c-113">Группа ресурсов Azure — это коллекция ресурсов Azure, развернутых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="13c4c-113">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="13c4c-114">Развертывание — это операция, которая делает ресурсы в группе ресурсов доступной для использования.</span><span class="sxs-lookup"><span data-stu-id="13c4c-114">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="13c4c-115">Дополнительные сведения о ресурсах Azure и группах ресурсов Azure можно найти в командлете New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="13c4c-115">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="13c4c-116">Вы можете использовать этот командлет для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="13c4c-116">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="13c4c-117">Для отладки используйте этот командлет с командлетом Get-AzureRmLog.</span><span class="sxs-lookup"><span data-stu-id="13c4c-117">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="13c4c-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13c4c-118">EXAMPLES</span></span>

### <span data-ttu-id="13c4c-119">Пример 1: получение всех развертываний для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="13c4c-119">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="13c4c-120">Эта команда получает все развертывания для группы ресурсов ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="13c4c-120">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="13c4c-121">На выходе показано развертывание для блога WordPress, в котором был использован шаблон коллекции.</span><span class="sxs-lookup"><span data-stu-id="13c4c-121">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="13c4c-122">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="13c4c-122">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="13c4c-123">Эта команда получает развертывание DeployWebsite01 группы ресурсов ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="13c4c-123">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="13c4c-124">Вы можете присвоить имя развертыванию при создании с помощью командлетов **New-AzureRmResourceGroup** или **New-AzureRmResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="13c4c-124">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="13c4c-125">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="13c4c-125">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="13c4c-126">Пример 3: получение развертываний всех групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="13c4c-126">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="13c4c-127">Эта команда получает все группы ресурсов в подписке с помощью командлета Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="13c4c-127">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="13c4c-128">Команда передает группы ресурсов в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="13c4c-128">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="13c4c-129">Текущий командлет получает все развертывания всех групп ресурсов в подписке и передает результаты в командлет Format-Table, чтобы отобразить значения свойств **ResourceGroupName** , **DeploymentName** и **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="13c4c-129">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="13c4c-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13c4c-130">PARAMETERS</span></span>

### <span data-ttu-id="13c4c-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="13c4c-131">-ApiVersion</span></span>
<span data-ttu-id="13c4c-132">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13c4c-132">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="13c4c-133">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="13c4c-133">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="13c4c-134">-ID</span><span class="sxs-lookup"><span data-stu-id="13c4c-134">-Id</span></span>
<span data-ttu-id="13c4c-135">Указывает идентификатор развертывания группы ресурсов, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="13c4c-135">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c4c-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13c4c-136">-Name</span></span>
<span data-ttu-id="13c4c-137">Указывает имя развертывания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="13c4c-137">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="13c4c-138">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="13c4c-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c4c-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="13c4c-139">-Pre</span></span>
<span data-ttu-id="13c4c-140">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="13c4c-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="13c4c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13c4c-141">-ResourceGroupName</span></span>
<span data-ttu-id="13c4c-142">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13c4c-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="13c4c-143">Командлет получает развертывание для группы ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="13c4c-143">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="13c4c-144">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="13c4c-144">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="13c4c-145">Этот параметр является обязательным, и вы можете указать только одну группу ресурсов в каждой команде.</span><span class="sxs-lookup"><span data-stu-id="13c4c-145">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c4c-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c4c-146">-DefaultProfile</span></span>
<span data-ttu-id="13c4c-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13c4c-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13c4c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c4c-148">CommonParameters</span></span>
<span data-ttu-id="13c4c-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13c4c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c4c-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13c4c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c4c-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13c4c-151">INPUTS</span></span>

### <span data-ttu-id="13c4c-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="13c4c-152">None</span></span>

## <span data-ttu-id="13c4c-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13c4c-153">OUTPUTS</span></span>

### <span data-ttu-id="13c4c-154">Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="13c4c-154">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="13c4c-155">Командлет возвращает развертывание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13c4c-155">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="13c4c-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="13c4c-156">NOTES</span></span>

## <span data-ttu-id="13c4c-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13c4c-157">RELATED LINKS</span></span>

[<span data-ttu-id="13c4c-158">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="13c4c-158">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="13c4c-159">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="13c4c-159">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="13c4c-160">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="13c4c-160">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="13c4c-161">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="13c4c-161">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="13c4c-162">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="13c4c-162">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="13c4c-163">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="13c4c-163">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


