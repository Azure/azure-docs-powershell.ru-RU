---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: 6c79d4b8d853d629a3b8e0422efb6a86eee18e34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235393"
---
# <span data-ttu-id="0f269-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0f269-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="0f269-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f269-102">SYNOPSIS</span></span>
<span data-ttu-id="0f269-103">Отмена выполняющегося развертывания в области клиента</span><span class="sxs-lookup"><span data-stu-id="0f269-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="0f269-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f269-104">SYNTAX</span></span>

### <span data-ttu-id="0f269-105">StopByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f269-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f269-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0f269-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f269-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f269-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f269-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f269-108">DESCRIPTION</span></span>
<span data-ttu-id="0f269-109">Командлет **Stop-AzTenantDeployment** отменяет развертывание, которое началось, но не завершено в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="0f269-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="0f269-110">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="0f269-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="0f269-111">Чтобы создать развертывание в области клиента, используйте командлет New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="0f269-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="0f269-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f269-112">EXAMPLES</span></span>

### <span data-ttu-id="0f269-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f269-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="0f269-114">Эта команда отменяет запущенное развертывание "deployment01" в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="0f269-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="0f269-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0f269-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="0f269-116">Эта команда получает развертывание "deployment01" в текущей области клиента и отменяет его.</span><span class="sxs-lookup"><span data-stu-id="0f269-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="0f269-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f269-117">PARAMETERS</span></span>

### <span data-ttu-id="0f269-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0f269-118">-ApiVersion</span></span>
<span data-ttu-id="0f269-119">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f269-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0f269-120">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="0f269-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0f269-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f269-121">-DefaultProfile</span></span>
<span data-ttu-id="0f269-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f269-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f269-123">-ID</span><span class="sxs-lookup"><span data-stu-id="0f269-123">-Id</span></span>
<span data-ttu-id="0f269-124">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="0f269-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0f269-125">Пример:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0f269-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f269-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f269-126">-InputObject</span></span>
<span data-ttu-id="0f269-127">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="0f269-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f269-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f269-128">-Name</span></span>
<span data-ttu-id="0f269-129">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="0f269-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f269-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f269-130">-PassThru</span></span>
<span data-ttu-id="0f269-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="0f269-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0f269-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="0f269-132">-Pre</span></span>
<span data-ttu-id="0f269-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="0f269-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0f269-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f269-134">-Confirm</span></span>
<span data-ttu-id="0f269-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f269-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f269-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f269-136">-WhatIf</span></span>
<span data-ttu-id="0f269-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f269-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f269-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f269-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f269-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f269-139">CommonParameters</span></span>
<span data-ttu-id="0f269-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f269-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f269-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f269-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f269-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f269-142">INPUTS</span></span>

### <span data-ttu-id="0f269-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0f269-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0f269-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f269-144">OUTPUTS</span></span>

### <span data-ttu-id="0f269-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f269-145">System.Boolean</span></span>

## <span data-ttu-id="0f269-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f269-146">NOTES</span></span>

## <span data-ttu-id="0f269-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f269-147">RELATED LINKS</span></span>
