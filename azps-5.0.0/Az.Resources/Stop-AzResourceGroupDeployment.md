---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: fa189637c9c2c1b63ab0e8dd0b00fab3f4505da0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245691"
---
# <span data-ttu-id="2aed3-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2aed3-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="2aed3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2aed3-102">SYNOPSIS</span></span>
<span data-ttu-id="2aed3-103">Отменяет развертывание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2aed3-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="2aed3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2aed3-104">SYNTAX</span></span>

### <span data-ttu-id="2aed3-105">StopByResourceGroupDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2aed3-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aed3-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2aed3-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aed3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2aed3-107">DESCRIPTION</span></span>
<span data-ttu-id="2aed3-108">Командлет **Stop-AzResourceGroupDeployment** отменяет развертывание группы ресурсов Azure, которое было запущено, но не завершено.</span><span class="sxs-lookup"><span data-stu-id="2aed3-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="2aed3-109">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="2aed3-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="2aed3-110">Ресурс Azure — это управляемая пользователем сущность, например веб-сайт, база данных или сервер базы данных.</span><span class="sxs-lookup"><span data-stu-id="2aed3-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="2aed3-111">Группа ресурсов — это коллекция ресурсов, развернутых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="2aed3-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="2aed3-112">Чтобы развернуть группу ресурсов, используйте командлет New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2aed3-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="2aed3-113">Командлет New-AzResource создает новый ресурс, но он не инициирует операцию развертывания группы ресурсов, которую этот командлет может остановить.</span><span class="sxs-lookup"><span data-stu-id="2aed3-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="2aed3-114">Этот командлет останавливает только одно запущенное развертывание.</span><span class="sxs-lookup"><span data-stu-id="2aed3-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="2aed3-115">Используйте параметр *Name* для остановки определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="2aed3-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="2aed3-116">Если вы пропустите параметр *Name* , **AzResourceGroupDeployment** ищет запущенное развертывание и останавливает его.</span><span class="sxs-lookup"><span data-stu-id="2aed3-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="2aed3-117">Если командлет обнаружит несколько запущенных развертываний, команда завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="2aed3-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="2aed3-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2aed3-118">EXAMPLES</span></span>

### <span data-ttu-id="2aed3-119">Пример 1: запуск и остановка развертывания группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2aed3-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="2aed3-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2aed3-120">PARAMETERS</span></span>

### <span data-ttu-id="2aed3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aed3-121">-DefaultProfile</span></span>
<span data-ttu-id="2aed3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2aed3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2aed3-123">-ID</span><span class="sxs-lookup"><span data-stu-id="2aed3-123">-Id</span></span>
<span data-ttu-id="2aed3-124">Указывает идентификатор развертывания группы ресурсов, которую нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="2aed3-124">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="2aed3-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2aed3-125">-Name</span></span>
<span data-ttu-id="2aed3-126">Указывает имя развертывания группы ресурсов, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="2aed3-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="2aed3-127">Если этот параметр не указан, этот командлет выполняет поиск выполняющегося развертывания в группе ресурсов и останавливает его.</span><span class="sxs-lookup"><span data-stu-id="2aed3-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="2aed3-128">При обнаружении нескольких запущенных развертываний происходит сбой команды.</span><span class="sxs-lookup"><span data-stu-id="2aed3-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="2aed3-129">Чтобы получить имя развертывания, используйте командлет Get-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="2aed3-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="2aed3-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="2aed3-130">-Pre</span></span>
<span data-ttu-id="2aed3-131">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="2aed3-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2aed3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aed3-132">-ResourceGroupName</span></span>
<span data-ttu-id="2aed3-133">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2aed3-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="2aed3-134">Этот командлет останавливает развертывание группы ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2aed3-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2aed3-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2aed3-135">-Confirm</span></span>
<span data-ttu-id="2aed3-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2aed3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aed3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aed3-137">-WhatIf</span></span>
<span data-ttu-id="2aed3-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2aed3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aed3-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2aed3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aed3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aed3-140">CommonParameters</span></span>
<span data-ttu-id="2aed3-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2aed3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aed3-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aed3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aed3-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2aed3-143">INPUTS</span></span>

### <span data-ttu-id="2aed3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2aed3-144">System.String</span></span>

## <span data-ttu-id="2aed3-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2aed3-145">OUTPUTS</span></span>

### <span data-ttu-id="2aed3-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2aed3-146">System.Boolean</span></span>

## <span data-ttu-id="2aed3-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="2aed3-147">NOTES</span></span>

## <span data-ttu-id="2aed3-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2aed3-148">RELATED LINKS</span></span>

[<span data-ttu-id="2aed3-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2aed3-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="2aed3-150">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="2aed3-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="2aed3-151">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2aed3-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="2aed3-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2aed3-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="2aed3-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2aed3-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="2aed3-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2aed3-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


