---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: b232a3a487994fdc74fb3df4b0cf384e5e73fe32
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066256"
---
# <span data-ttu-id="baa93-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="baa93-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="baa93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="baa93-102">SYNOPSIS</span></span>
<span data-ttu-id="baa93-103">Удаляет развертывание в области клиента и любые связанные операции.</span><span class="sxs-lookup"><span data-stu-id="baa93-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="baa93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="baa93-104">SYNTAX</span></span>

### <span data-ttu-id="baa93-105">RemoveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="baa93-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa93-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="baa93-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa93-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="baa93-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baa93-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baa93-108">DESCRIPTION</span></span>
<span data-ttu-id="baa93-109">Командлет **Remove-AzTenantDeployment** удаляет развертывание Azure из текущей области клиента и любых связанных операций.</span><span class="sxs-lookup"><span data-stu-id="baa93-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="baa93-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="baa93-110">EXAMPLES</span></span>

### <span data-ttu-id="baa93-111">Пример 1: Удаление развертывания с указанным именем</span><span class="sxs-lookup"><span data-stu-id="baa93-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="baa93-112">Эта команда удаляет развертывание "RolesDeployment" в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="baa93-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="baa93-113">Пример 2: получение развертывания и его удаление</span><span class="sxs-lookup"><span data-stu-id="baa93-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="baa93-114">Эта команда получает развертывание "RolesDeployment" в текущей области клиента и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="baa93-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="baa93-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="baa93-115">PARAMETERS</span></span>

### <span data-ttu-id="baa93-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="baa93-116">-ApiVersion</span></span>
<span data-ttu-id="baa93-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="baa93-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="baa93-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="baa93-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="baa93-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baa93-119">-AsJob</span></span>
<span data-ttu-id="baa93-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="baa93-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="baa93-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa93-121">-DefaultProfile</span></span>
<span data-ttu-id="baa93-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="baa93-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baa93-123">-ID</span><span class="sxs-lookup"><span data-stu-id="baa93-123">-Id</span></span>
<span data-ttu-id="baa93-124">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="baa93-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="baa93-125">Пример:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="baa93-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa93-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baa93-126">-InputObject</span></span>
<span data-ttu-id="baa93-127">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="baa93-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baa93-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="baa93-128">-Name</span></span>
<span data-ttu-id="baa93-129">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="baa93-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa93-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="baa93-130">-PassThru</span></span>
<span data-ttu-id="baa93-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="baa93-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="baa93-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="baa93-132">-Pre</span></span>
<span data-ttu-id="baa93-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="baa93-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="baa93-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baa93-134">-Confirm</span></span>
<span data-ttu-id="baa93-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="baa93-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baa93-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baa93-136">-WhatIf</span></span>
<span data-ttu-id="baa93-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="baa93-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baa93-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="baa93-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baa93-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa93-139">CommonParameters</span></span>
<span data-ttu-id="baa93-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="baa93-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa93-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baa93-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa93-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="baa93-142">INPUTS</span></span>

### <span data-ttu-id="baa93-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="baa93-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="baa93-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="baa93-144">OUTPUTS</span></span>

### <span data-ttu-id="baa93-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="baa93-145">System.Boolean</span></span>

## <span data-ttu-id="baa93-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="baa93-146">NOTES</span></span>

## <span data-ttu-id="baa93-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baa93-147">RELATED LINKS</span></span>
