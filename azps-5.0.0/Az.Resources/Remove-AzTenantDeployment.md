---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249821"
---
# <span data-ttu-id="7ebd0-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7ebd0-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="7ebd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ebd0-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebd0-103">Удаляет развертывание в области клиента и любые связанные операции.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="7ebd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ebd0-104">SYNTAX</span></span>

### <span data-ttu-id="7ebd0-105">RemoveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7ebd0-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ebd0-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="7ebd0-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ebd0-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7ebd0-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ebd0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ebd0-108">DESCRIPTION</span></span>
<span data-ttu-id="7ebd0-109">Командлет **Remove-AzTenantDeployment** удаляет развертывание Azure из текущей области клиента и любых связанных операций.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="7ebd0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ebd0-110">EXAMPLES</span></span>

### <span data-ttu-id="7ebd0-111">Пример 1: Удаление развертывания с указанным именем</span><span class="sxs-lookup"><span data-stu-id="7ebd0-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="7ebd0-112">Эта команда удаляет развертывание "RolesDeployment" в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="7ebd0-113">Пример 2: получение развертывания и его удаление</span><span class="sxs-lookup"><span data-stu-id="7ebd0-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="7ebd0-114">Эта команда получает развертывание "RolesDeployment" в текущей области клиента и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="7ebd0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ebd0-115">PARAMETERS</span></span>

### <span data-ttu-id="7ebd0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ebd0-116">-AsJob</span></span>
<span data-ttu-id="7ebd0-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7ebd0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ebd0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ebd0-118">-DefaultProfile</span></span>
<span data-ttu-id="7ebd0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ebd0-120">-ID</span><span class="sxs-lookup"><span data-stu-id="7ebd0-120">-Id</span></span>
<span data-ttu-id="7ebd0-121">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="7ebd0-122">Пример:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="7ebd0-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebd0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ebd0-123">-InputObject</span></span>
<span data-ttu-id="7ebd0-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebd0-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7ebd0-125">-Name</span></span>
<span data-ttu-id="7ebd0-126">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebd0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ebd0-127">-PassThru</span></span>
<span data-ttu-id="7ebd0-128">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="7ebd0-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7ebd0-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="7ebd0-129">-Pre</span></span>
<span data-ttu-id="7ebd0-130">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7ebd0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ebd0-131">-Confirm</span></span>
<span data-ttu-id="7ebd0-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebd0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebd0-133">-WhatIf</span></span>
<span data-ttu-id="7ebd0-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ebd0-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebd0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebd0-136">CommonParameters</span></span>
<span data-ttu-id="7ebd0-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ebd0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebd0-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ebd0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebd0-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ebd0-139">INPUTS</span></span>

### <span data-ttu-id="7ebd0-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7ebd0-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7ebd0-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ebd0-141">OUTPUTS</span></span>

### <span data-ttu-id="7ebd0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ebd0-142">System.Boolean</span></span>

## <span data-ttu-id="7ebd0-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ebd0-143">NOTES</span></span>

## <span data-ttu-id="7ebd0-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ebd0-144">RELATED LINKS</span></span>
