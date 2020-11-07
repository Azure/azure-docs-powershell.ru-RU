---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 139b38fed6e768e761631687f06cd833afaa4068
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913259"
---
# <span data-ttu-id="ffb21-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ffb21-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="ffb21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ffb21-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb21-103">Отменяет развертывание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffb21-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffb21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ffb21-104">SYNTAX</span></span>

### <span data-ttu-id="ffb21-105">StopByResourceGroupDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ffb21-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffb21-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ffb21-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffb21-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffb21-107">DESCRIPTION</span></span>
<span data-ttu-id="ffb21-108">Командлет **Stop-AzureRmResourceGroupDeployment** отменяет развертывание группы ресурсов Azure, которое было запущено, но не завершено.</span><span class="sxs-lookup"><span data-stu-id="ffb21-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="ffb21-109">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="ffb21-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="ffb21-110">Ресурс Azure — это управляемая пользователем сущность, например веб-сайт, база данных или сервер базы данных.</span><span class="sxs-lookup"><span data-stu-id="ffb21-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="ffb21-111">Группа ресурсов — это коллекция ресурсов, развернутых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="ffb21-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="ffb21-112">Чтобы развернуть группу ресурсов, используйте командлет New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ffb21-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="ffb21-113">Командлет New-AzureRmResource создает новый ресурс, но он не инициирует операцию развертывания группы ресурсов, которую этот командлет может остановить.</span><span class="sxs-lookup"><span data-stu-id="ffb21-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="ffb21-114">Этот командлет останавливает только одно запущенное развертывание.</span><span class="sxs-lookup"><span data-stu-id="ffb21-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="ffb21-115">Используйте параметр *Name* для остановки определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="ffb21-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="ffb21-116">Если вы пропустите параметр *Name* , **AzureRmResourceGroupDeployment** ищет запущенное развертывание и останавливает его.</span><span class="sxs-lookup"><span data-stu-id="ffb21-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="ffb21-117">Если командлет обнаружит несколько запущенных развертываний, команда завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="ffb21-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="ffb21-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ffb21-118">EXAMPLES</span></span>

### <span data-ttu-id="ffb21-119">Пример 1: запуск и остановка развертывания группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ffb21-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzureRmResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azuredeploy.json -TemplateParameterFile .\storage-account-create-azuredeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmResourceGro...

PS C:\> Stop-AzureRmResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzureRmResourceGro...
```

## <span data-ttu-id="ffb21-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ffb21-120">PARAMETERS</span></span>

### <span data-ttu-id="ffb21-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ffb21-121">-ApiVersion</span></span>
<span data-ttu-id="ffb21-122">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffb21-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ffb21-123">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ffb21-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ffb21-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb21-124">-DefaultProfile</span></span>
<span data-ttu-id="ffb21-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ffb21-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffb21-126">-ID</span><span class="sxs-lookup"><span data-stu-id="ffb21-126">-Id</span></span>
<span data-ttu-id="ffb21-127">Указывает идентификатор развертывания группы ресурсов, которую нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="ffb21-127">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="ffb21-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ffb21-128">-Name</span></span>
<span data-ttu-id="ffb21-129">Указывает имя развертывания группы ресурсов, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="ffb21-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="ffb21-130">Если этот параметр не указан, этот командлет выполняет поиск выполняющегося развертывания в группе ресурсов и останавливает его.</span><span class="sxs-lookup"><span data-stu-id="ffb21-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="ffb21-131">При обнаружении нескольких запущенных развертываний происходит сбой команды.</span><span class="sxs-lookup"><span data-stu-id="ffb21-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="ffb21-132">Чтобы получить имя развертывания, используйте командлет Get-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ffb21-132">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="ffb21-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="ffb21-133">-Pre</span></span>
<span data-ttu-id="ffb21-134">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="ffb21-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ffb21-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffb21-135">-ResourceGroupName</span></span>
<span data-ttu-id="ffb21-136">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffb21-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="ffb21-137">Этот командлет останавливает развертывание группы ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ffb21-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ffb21-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffb21-138">-Confirm</span></span>
<span data-ttu-id="ffb21-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ffb21-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb21-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb21-140">-WhatIf</span></span>
<span data-ttu-id="ffb21-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ffb21-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffb21-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ffb21-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb21-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb21-143">CommonParameters</span></span>
<span data-ttu-id="ffb21-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ffb21-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb21-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffb21-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb21-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ffb21-146">INPUTS</span></span>

### <span data-ttu-id="ffb21-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="ffb21-147">None</span></span>

## <span data-ttu-id="ffb21-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffb21-148">OUTPUTS</span></span>

### <span data-ttu-id="ffb21-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ffb21-149">System.Boolean</span></span>

## <span data-ttu-id="ffb21-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffb21-150">NOTES</span></span>

## <span data-ttu-id="ffb21-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffb21-151">RELATED LINKS</span></span>

[<span data-ttu-id="ffb21-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ffb21-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ffb21-153">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ffb21-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ffb21-154">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ffb21-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="ffb21-155">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ffb21-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ffb21-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ffb21-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ffb21-157">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ffb21-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


