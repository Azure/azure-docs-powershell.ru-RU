---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 4cdc70928f2b27ae1e1604c52e5703798a302a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567930"
---
# <span data-ttu-id="3ce81-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3ce81-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="3ce81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ce81-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce81-103">Отменяет развертывание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ce81-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ce81-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ce81-104">SYNTAX</span></span>

### <span data-ttu-id="3ce81-105">StopByResourceGroupDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ce81-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce81-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="3ce81-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ce81-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ce81-107">DESCRIPTION</span></span>
<span data-ttu-id="3ce81-108">Командлет **Stop-AzureRmResourceGroupDeployment** отменяет развертывание группы ресурсов Azure, которое было запущено, но не завершено.</span><span class="sxs-lookup"><span data-stu-id="3ce81-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="3ce81-109">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="3ce81-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="3ce81-110">Ресурс Azure — это управляемая пользователем сущность, например веб-сайт, база данных или сервер базы данных.</span><span class="sxs-lookup"><span data-stu-id="3ce81-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="3ce81-111">Группа ресурсов — это коллекция ресурсов, развернутых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="3ce81-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="3ce81-112">Чтобы развернуть группу ресурсов, используйте командлет New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="3ce81-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="3ce81-113">Командлет New-AzureRmResource создает новый ресурс, но он не инициирует операцию развертывания группы ресурсов, которую этот командлет может остановить.</span><span class="sxs-lookup"><span data-stu-id="3ce81-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="3ce81-114">Этот командлет останавливает только одно запущенное развертывание.</span><span class="sxs-lookup"><span data-stu-id="3ce81-114">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="3ce81-115">Используйте параметр *Name* для остановки определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="3ce81-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="3ce81-116">Если вы пропустите параметр *Name* , **AzureRmResourceGroupDeployment** ищет запущенное развертывание и останавливает его.</span><span class="sxs-lookup"><span data-stu-id="3ce81-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="3ce81-117">Если командлет обнаружит несколько запущенных развертываний, команда завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="3ce81-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="3ce81-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ce81-118">EXAMPLES</span></span>

## <span data-ttu-id="3ce81-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ce81-119">PARAMETERS</span></span>

### <span data-ttu-id="3ce81-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3ce81-120">-ApiVersion</span></span>
<span data-ttu-id="3ce81-121">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ce81-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3ce81-122">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ce81-122">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce81-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce81-123">-DefaultProfile</span></span>
<span data-ttu-id="3ce81-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3ce81-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce81-125">-ID</span><span class="sxs-lookup"><span data-stu-id="3ce81-125">-Id</span></span>
<span data-ttu-id="3ce81-126">Указывает идентификатор развертывания группы ресурсов, которую нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="3ce81-126">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce81-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ce81-127">-Name</span></span>
<span data-ttu-id="3ce81-128">Указывает имя развертывания группы ресурсов, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="3ce81-128">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="3ce81-129">Если этот параметр не указан, этот командлет выполняет поиск выполняющегося развертывания в группе ресурсов и останавливает его.</span><span class="sxs-lookup"><span data-stu-id="3ce81-129">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="3ce81-130">При обнаружении нескольких запущенных развертываний происходит сбой команды.</span><span class="sxs-lookup"><span data-stu-id="3ce81-130">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="3ce81-131">Чтобы получить имя развертывания, используйте командлет Get-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="3ce81-131">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce81-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="3ce81-132">-Pre</span></span>
<span data-ttu-id="3ce81-133">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="3ce81-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce81-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce81-134">-ResourceGroupName</span></span>
<span data-ttu-id="3ce81-135">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ce81-135">Specifies the name of the resource group.</span></span>
<span data-ttu-id="3ce81-136">Этот командлет останавливает развертывание группы ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3ce81-136">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce81-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ce81-137">-Confirm</span></span>
<span data-ttu-id="3ce81-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ce81-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce81-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce81-139">-WhatIf</span></span>
<span data-ttu-id="3ce81-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ce81-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ce81-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ce81-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce81-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce81-142">CommonParameters</span></span>
<span data-ttu-id="3ce81-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ce81-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce81-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce81-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce81-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ce81-145">INPUTS</span></span>

### <span data-ttu-id="3ce81-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="3ce81-146">None</span></span>

## <span data-ttu-id="3ce81-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ce81-147">OUTPUTS</span></span>

### <span data-ttu-id="3ce81-148">Значением</span><span class="sxs-lookup"><span data-stu-id="3ce81-148">Boolean</span></span>

## <span data-ttu-id="3ce81-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ce81-149">NOTES</span></span>

## <span data-ttu-id="3ce81-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ce81-150">RELATED LINKS</span></span>

[<span data-ttu-id="3ce81-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3ce81-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="3ce81-152">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3ce81-152">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="3ce81-153">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3ce81-153">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="3ce81-154">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3ce81-154">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="3ce81-155">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3ce81-155">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="3ce81-156">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3ce81-156">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


