---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 9258c15578aaeae5102a5d60b2f18a8a4f179d76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967624"
---
# <span data-ttu-id="c4a62-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c4a62-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="c4a62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a62-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a62-103">Отмена развертывания группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4a62-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="c4a62-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4a62-104">SYNTAX</span></span>

### <span data-ttu-id="c4a62-105">StopByResourceGroupDeploymentName (Default)</span><span class="sxs-lookup"><span data-stu-id="c4a62-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4a62-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c4a62-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4a62-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4a62-107">DESCRIPTION</span></span>
<span data-ttu-id="c4a62-108">Из-за настройки **Stop-AzResourceGroupDeployment** развертывание группы ресурсов Azure отменено, но не завершено.</span><span class="sxs-lookup"><span data-stu-id="c4a62-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="c4a62-109">Чтобы завершить развертывание, необходимо иметь неполное состояние подготовка, например подготовка, а не завершалось состояние, например "Подготовка" или "Сбой".</span><span class="sxs-lookup"><span data-stu-id="c4a62-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="c4a62-110">Ресурс Azure — это объект, управляемый пользователем, например веб-сайт, база данных или сервер базы данных.</span><span class="sxs-lookup"><span data-stu-id="c4a62-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="c4a62-111">Группа ресурсов — это набор ресурсов, развертываемых в качестве единицы.</span><span class="sxs-lookup"><span data-stu-id="c4a62-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="c4a62-112">Чтобы развернуть группу ресурсов, воспользуйтесь New-AzResourceGroupDeployment управления.</span><span class="sxs-lookup"><span data-stu-id="c4a62-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="c4a62-113">С New-AzResource создается новый ресурс, но при этом не запускается операция развертывания группы ресурсов, которая может быть остановиться.</span><span class="sxs-lookup"><span data-stu-id="c4a62-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="c4a62-114">Этот cmdlet останавливает только одно развертывание.</span><span class="sxs-lookup"><span data-stu-id="c4a62-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="c4a62-115">Используйте параметр *Name,* чтобы остановить определенное развертывание.</span><span class="sxs-lookup"><span data-stu-id="c4a62-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="c4a62-116">Если параметр *Name* не задан, **stop-AzResourceGroupDeployment** выполняет поиск запущенного развертывания и останавливает его.</span><span class="sxs-lookup"><span data-stu-id="c4a62-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="c4a62-117">Если командлет обнаружит несколько запущенных командлетов, команда не будет работать.</span><span class="sxs-lookup"><span data-stu-id="c4a62-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="c4a62-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4a62-118">EXAMPLES</span></span>

### <span data-ttu-id="c4a62-119">Пример 1. Запуск и остановка развертывания группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c4a62-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="c4a62-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4a62-120">PARAMETERS</span></span>

### <span data-ttu-id="c4a62-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a62-121">-DefaultProfile</span></span>
<span data-ttu-id="c4a62-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c4a62-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4a62-123">-Id</span><span class="sxs-lookup"><span data-stu-id="c4a62-123">-Id</span></span>
<span data-ttu-id="c4a62-124">Указывает, что развертывание группы ресурсов нужно прекратить.</span><span class="sxs-lookup"><span data-stu-id="c4a62-124">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a62-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c4a62-125">-Name</span></span>
<span data-ttu-id="c4a62-126">Указывает имя развертывания группы ресурсов, которое нужно прекратить.</span><span class="sxs-lookup"><span data-stu-id="c4a62-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="c4a62-127">Если этот параметр не задан, выполняется поиск запущенного развертывания в группе ресурсов и его остановка.</span><span class="sxs-lookup"><span data-stu-id="c4a62-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="c4a62-128">Если обнаружится несколько запущенных команд, команда не будет работать.</span><span class="sxs-lookup"><span data-stu-id="c4a62-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="c4a62-129">Чтобы получить имя развертывания, используйте Get-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="c4a62-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a62-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="c4a62-130">-Pre</span></span>
<span data-ttu-id="c4a62-131">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="c4a62-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c4a62-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a62-132">-ResourceGroupName</span></span>
<span data-ttu-id="c4a62-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4a62-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="c4a62-134">Этот cmdlet останавливает развертывание группы ресурсов, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c4a62-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a62-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4a62-135">-Confirm</span></span>
<span data-ttu-id="c4a62-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4a62-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a62-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a62-137">-WhatIf</span></span>
<span data-ttu-id="c4a62-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4a62-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a62-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c4a62-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a62-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a62-140">CommonParameters</span></span>
<span data-ttu-id="c4a62-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a62-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a62-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4a62-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a62-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4a62-143">INPUTS</span></span>

### <span data-ttu-id="c4a62-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c4a62-144">System.String</span></span>

## <span data-ttu-id="c4a62-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4a62-145">OUTPUTS</span></span>

### <span data-ttu-id="c4a62-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4a62-146">System.Boolean</span></span>

## <span data-ttu-id="c4a62-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4a62-147">NOTES</span></span>

## <span data-ttu-id="c4a62-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4a62-148">RELATED LINKS</span></span>

[<span data-ttu-id="c4a62-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c4a62-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="c4a62-150">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="c4a62-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="c4a62-151">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c4a62-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="c4a62-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c4a62-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="c4a62-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c4a62-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="c4a62-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c4a62-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


