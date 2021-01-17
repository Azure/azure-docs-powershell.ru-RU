---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398156"
---
# <span data-ttu-id="1a6e8-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1a6e8-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="1a6e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6e8-103">Возвращает развертывание в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="1a6e8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a6e8-104">SYNTAX</span></span>

### <span data-ttu-id="1a6e8-105">GetByResourceGroupDeploymentName (Default)</span><span class="sxs-lookup"><span data-stu-id="1a6e8-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a6e8-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="1a6e8-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a6e8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a6e8-107">DESCRIPTION</span></span>
<span data-ttu-id="1a6e8-108">Для развертывания в группе ресурсов Azure развертывается **cmdlet Get-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="1a6e8-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="1a6e8-109">Укажите *параметр "Имя"* *или "ИД",* чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="1a6e8-110">По умолчанию **Get-AzResourceGroupDeployment** получает все развертывания для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="1a6e8-111">Ресурс Azure — это объект Azure, управляемый пользователем, например сервер базы данных, база данных или веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="1a6e8-112">Группа ресурсов Azure — это набор ресурсов Azure, развертываемых в качестве единицы.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="1a6e8-113">Развертывание — это операция, которая делает ресурсы из группы ресурсов доступными для использования.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="1a6e8-114">Дополнительные сведения о ресурсах Azure и группах ресурсов Azure см. в New-AzResourceGroup>.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1a6e8-115">Этот cmdlet можно использовать для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="1a6e8-116">Для отладки используйте этот Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="1a6e8-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a6e8-117">EXAMPLES</span></span>

### <span data-ttu-id="1a6e8-118">Пример 1. Получить все развертывания для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1a6e8-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="1a6e8-119">Эта команда получает все развертывания для группы ресурсов ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="1a6e8-120">В результате будет показана развертывание блога WordPress, в который использовался шаблон коллекции.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="1a6e8-121">Пример 2. Получить развертывание по имени</span><span class="sxs-lookup"><span data-stu-id="1a6e8-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="1a6e8-122">Эта команда получает развертывание DeployWebsite01 группы ресурсов ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="1a6e8-123">Вы можете назначить имя развертыванию при его создании с помощью проектлетов **New-AzResourceGroup** или **New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="1a6e8-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="1a6e8-124">Если не назначить имя, в качестве имени по умолчанию будет использоваться шаблон, используемый для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="1a6e8-125">Пример 3. Развертывание всех групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="1a6e8-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="1a6e8-126">Эта команда получает все группы ресурсов в вашей подписке с помощью Get-AzResourceGroup командлета.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1a6e8-127">Команда передает группы ресурсов текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1a6e8-128">Текущий cmdlet получает все развертывания всех групп ресурсов в подписке и передает результаты в Format-Table, чтобы отобразить значения их свойств **ResourceGroupName,** **DeploymentName** и **ProvisioningState.**</span><span class="sxs-lookup"><span data-stu-id="1a6e8-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="1a6e8-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a6e8-129">PARAMETERS</span></span>

### <span data-ttu-id="1a6e8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6e8-130">-DefaultProfile</span></span>
<span data-ttu-id="1a6e8-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1a6e8-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a6e8-132">-Id</span><span class="sxs-lookup"><span data-stu-id="1a6e8-132">-Id</span></span>
<span data-ttu-id="1a6e8-133">Определяет ИД развертывания группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-133">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="1a6e8-134">-Name</span><span class="sxs-lookup"><span data-stu-id="1a6e8-134">-Name</span></span>
<span data-ttu-id="1a6e8-135">Указывает имя нужного развертывания.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="1a6e8-136">Поддиавные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-136">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="1a6e8-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="1a6e8-137">-Pre</span></span>
<span data-ttu-id="1a6e8-138">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1a6e8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a6e8-139">-ResourceGroupName</span></span>
<span data-ttu-id="1a6e8-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1a6e8-141">Он получает развертывания для группы ресурсов, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="1a6e8-142">Поддиавные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="1a6e8-143">Этот параметр является required, и в каждой команде можно указать только одну группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-143">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="1a6e8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6e8-144">CommonParameters</span></span>
<span data-ttu-id="1a6e8-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a6e8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6e8-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a6e8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6e8-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a6e8-147">INPUTS</span></span>

### <span data-ttu-id="1a6e8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1a6e8-148">System.String</span></span>

## <span data-ttu-id="1a6e8-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a6e8-149">OUTPUTS</span></span>

### <span data-ttu-id="1a6e8-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1a6e8-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="1a6e8-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a6e8-151">NOTES</span></span>

## <span data-ttu-id="1a6e8-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a6e8-152">RELATED LINKS</span></span>

[<span data-ttu-id="1a6e8-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1a6e8-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="1a6e8-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1a6e8-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="1a6e8-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1a6e8-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="1a6e8-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1a6e8-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="1a6e8-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1a6e8-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="1a6e8-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1a6e8-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


