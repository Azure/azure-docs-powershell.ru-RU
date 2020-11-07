---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: e6f6be148757bb2f30ac0f09575907669ddc195b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905622"
---
# <span data-ttu-id="f417d-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f417d-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="f417d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f417d-102">SYNOPSIS</span></span>
<span data-ttu-id="f417d-103">Возвращает развертывания в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f417d-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="f417d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f417d-104">SYNTAX</span></span>

### <span data-ttu-id="f417d-105">GetByResourceGroupDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f417d-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f417d-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f417d-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f417d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f417d-107">DESCRIPTION</span></span>
<span data-ttu-id="f417d-108">Командлет **Get-AzResourceGroupDeployment** получает развертывание в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f417d-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="f417d-109">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="f417d-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="f417d-110">По умолчанию **Get-AzResourceGroupDeployment** получает все развертывания для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f417d-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="f417d-111">Ресурс Azure — это управляемая пользователем сущность Azure, например сервер базы данных, база данных или веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="f417d-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="f417d-112">Группа ресурсов Azure — это коллекция ресурсов Azure, развернутых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="f417d-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="f417d-113">Развертывание — это операция, которая делает ресурсы в группе ресурсов доступной для использования.</span><span class="sxs-lookup"><span data-stu-id="f417d-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="f417d-114">Дополнительные сведения о ресурсах Azure и группах ресурсов Azure можно найти в командлете New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f417d-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f417d-115">Вы можете использовать этот командлет для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="f417d-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="f417d-116">Для отладки используйте этот командлет с командлетом Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="f417d-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="f417d-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f417d-117">EXAMPLES</span></span>

### <span data-ttu-id="f417d-118">Пример 1: получение всех развертываний для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f417d-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="f417d-119">Эта команда получает все развертывания для группы ресурсов ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="f417d-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="f417d-120">На выходе показано развертывание для блога WordPress, в котором был использован шаблон коллекции.</span><span class="sxs-lookup"><span data-stu-id="f417d-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="f417d-121">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="f417d-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="f417d-122">Эта команда получает развертывание DeployWebsite01 группы ресурсов ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="f417d-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="f417d-123">Вы можете присвоить имя развертыванию при создании с помощью командлетов **New-AzResourceGroup** или **New-AzResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="f417d-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="f417d-124">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="f417d-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="f417d-125">Пример 3: получение развертываний всех групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="f417d-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="f417d-126">Эта команда получает все группы ресурсов в подписке с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f417d-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f417d-127">Команда передает группы ресурсов в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f417d-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f417d-128">Текущий командлет получает все развертывания всех групп ресурсов в подписке и передает результаты в командлет Format-Table, чтобы отобразить значения свойств **ResourceGroupName** , **DeploymentName** и **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="f417d-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="f417d-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f417d-129">PARAMETERS</span></span>

### <span data-ttu-id="f417d-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f417d-130">-ApiVersion</span></span>
<span data-ttu-id="f417d-131">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f417d-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f417d-132">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f417d-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f417d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f417d-133">-DefaultProfile</span></span>
<span data-ttu-id="f417d-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f417d-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f417d-135">-ID</span><span class="sxs-lookup"><span data-stu-id="f417d-135">-Id</span></span>
<span data-ttu-id="f417d-136">Указывает идентификатор развертывания группы ресурсов, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f417d-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="f417d-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f417d-137">-Name</span></span>
<span data-ttu-id="f417d-138">Указывает имя развертывания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f417d-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="f417d-139">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="f417d-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="f417d-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="f417d-140">-Pre</span></span>
<span data-ttu-id="f417d-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f417d-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f417d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f417d-142">-ResourceGroupName</span></span>
<span data-ttu-id="f417d-143">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f417d-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f417d-144">Командлет получает развертывание для группы ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f417d-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="f417d-145">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="f417d-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="f417d-146">Этот параметр является обязательным, и вы можете указать только одну группу ресурсов в каждой команде.</span><span class="sxs-lookup"><span data-stu-id="f417d-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="f417d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f417d-147">CommonParameters</span></span>
<span data-ttu-id="f417d-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f417d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f417d-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f417d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f417d-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f417d-150">INPUTS</span></span>

### <span data-ttu-id="f417d-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f417d-151">System.String</span></span>

## <span data-ttu-id="f417d-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f417d-152">OUTPUTS</span></span>

### <span data-ttu-id="f417d-153">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f417d-153">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="f417d-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="f417d-154">NOTES</span></span>

## <span data-ttu-id="f417d-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f417d-155">RELATED LINKS</span></span>

[<span data-ttu-id="f417d-156">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f417d-156">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="f417d-157">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f417d-157">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="f417d-158">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f417d-158">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="f417d-159">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f417d-159">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="f417d-160">Остановить-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f417d-160">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="f417d-161">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f417d-161">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


