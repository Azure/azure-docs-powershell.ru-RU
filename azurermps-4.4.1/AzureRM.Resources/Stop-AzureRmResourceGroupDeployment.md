---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f07b2f59f1a38aca780e1e869bb3904725df6dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734777"
---
# <span data-ttu-id="62365-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62365-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="62365-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62365-102">SYNOPSIS</span></span>
<span data-ttu-id="62365-103">Отменяет развертывание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62365-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62365-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62365-104">SYNTAX</span></span>

### <span data-ttu-id="62365-105">Заданный параметр имени развертывания.</span><span class="sxs-lookup"><span data-stu-id="62365-105">The deployment name parameter set.</span></span> <span data-ttu-id="62365-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="62365-106">(Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62365-107">Заданный параметр идентификатора развертывания.</span><span class="sxs-lookup"><span data-stu-id="62365-107">The deployment Id parameter set.</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62365-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62365-108">DESCRIPTION</span></span>
<span data-ttu-id="62365-109">Командлет **Stop-AzureRmResourceGroupDeployment** отменяет развертывание группы ресурсов Azure, которое было запущено, но не завершено.</span><span class="sxs-lookup"><span data-stu-id="62365-109">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="62365-110">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="62365-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="62365-111">Ресурс Azure — это управляемая пользователем сущность, например веб-сайт, база данных или сервер базы данных.</span><span class="sxs-lookup"><span data-stu-id="62365-111">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="62365-112">Группа ресурсов — это коллекция ресурсов, развернутых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="62365-112">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="62365-113">Чтобы развернуть группу ресурсов, используйте командлет New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="62365-113">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="62365-114">Командлет New-AzureRmResource создает новый ресурс, но он не инициирует операцию развертывания группы ресурсов, которую этот командлет может остановить.</span><span class="sxs-lookup"><span data-stu-id="62365-114">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="62365-115">Этот командлет останавливает только одно запущенное развертывание.</span><span class="sxs-lookup"><span data-stu-id="62365-115">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="62365-116">Используйте параметр *Name* для остановки определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="62365-116">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="62365-117">Если вы пропустите параметр *Name* , **AzureRmResourceGroupDeployment** ищет запущенное развертывание и останавливает его.</span><span class="sxs-lookup"><span data-stu-id="62365-117">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="62365-118">Если командлет обнаружит несколько запущенных развертываний, команда завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="62365-118">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="62365-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62365-119">EXAMPLES</span></span>

## <span data-ttu-id="62365-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62365-120">PARAMETERS</span></span>

### <span data-ttu-id="62365-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="62365-121">-ApiVersion</span></span>
<span data-ttu-id="62365-122">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62365-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="62365-123">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="62365-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="62365-124">-ID</span><span class="sxs-lookup"><span data-stu-id="62365-124">-Id</span></span>
<span data-ttu-id="62365-125">Указывает идентификатор развертывания группы ресурсов, которую нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="62365-125">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="62365-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62365-126">-Name</span></span>
<span data-ttu-id="62365-127">Указывает имя развертывания группы ресурсов, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="62365-127">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="62365-128">Если этот параметр не указан, этот командлет выполняет поиск выполняющегося развертывания в группе ресурсов и останавливает его.</span><span class="sxs-lookup"><span data-stu-id="62365-128">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="62365-129">При обнаружении нескольких запущенных развертываний происходит сбой команды.</span><span class="sxs-lookup"><span data-stu-id="62365-129">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="62365-130">Чтобы получить имя развертывания, используйте командлет Get-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="62365-130">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62365-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="62365-131">-Pre</span></span>
<span data-ttu-id="62365-132">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="62365-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="62365-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62365-133">-ResourceGroupName</span></span>
<span data-ttu-id="62365-134">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62365-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="62365-135">Этот командлет останавливает развертывание группы ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="62365-135">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="62365-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62365-136">-Confirm</span></span>
<span data-ttu-id="62365-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62365-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62365-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62365-138">-WhatIf</span></span>
<span data-ttu-id="62365-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62365-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62365-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62365-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62365-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62365-141">-DefaultProfile</span></span>
<span data-ttu-id="62365-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62365-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62365-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62365-143">CommonParameters</span></span>
<span data-ttu-id="62365-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62365-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62365-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62365-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62365-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62365-146">INPUTS</span></span>

### <span data-ttu-id="62365-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="62365-147">None</span></span>

## <span data-ttu-id="62365-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62365-148">OUTPUTS</span></span>

### <span data-ttu-id="62365-149">Значением</span><span class="sxs-lookup"><span data-stu-id="62365-149">Boolean</span></span>

## <span data-ttu-id="62365-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="62365-150">NOTES</span></span>

## <span data-ttu-id="62365-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62365-151">RELATED LINKS</span></span>

[<span data-ttu-id="62365-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62365-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="62365-153">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="62365-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="62365-154">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="62365-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="62365-155">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62365-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="62365-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62365-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="62365-157">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62365-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


