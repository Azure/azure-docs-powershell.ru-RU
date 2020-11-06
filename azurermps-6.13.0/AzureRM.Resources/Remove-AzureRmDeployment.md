---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmDeployment.md
ms.openlocfilehash: a008ecf8b8c6681941e19b4db63f79c85fab8ba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562688"
---
# <span data-ttu-id="aa64a-101">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="aa64a-101">Remove-AzureRmDeployment</span></span>

## <span data-ttu-id="aa64a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa64a-102">SYNOPSIS</span></span>
<span data-ttu-id="aa64a-103">Удаление развертывания и связанных с ней операций</span><span class="sxs-lookup"><span data-stu-id="aa64a-103">Removes a deployment and any associated operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa64a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa64a-104">SYNTAX</span></span>

### <span data-ttu-id="aa64a-105">RemoveByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa64a-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzureRmDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa64a-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="aa64a-106">RemoveByDeploymentId</span></span>
```
Remove-AzureRmDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa64a-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="aa64a-107">RemoveByInputObject</span></span>
```
Remove-AzureRmDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa64a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa64a-108">DESCRIPTION</span></span>
<span data-ttu-id="aa64a-109">Командлет **Remove-AzureRmDeployment** удаляет развертывание Azure в области подписок и все связанные операции.</span><span class="sxs-lookup"><span data-stu-id="aa64a-109">The **Remove-AzureRmDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="aa64a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa64a-110">EXAMPLES</span></span>

### <span data-ttu-id="aa64a-111">Пример 1: Удаление развертывания с указанным именем</span><span class="sxs-lookup"><span data-stu-id="aa64a-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzureRmDeployment -Name "RolesDeployment"
```

<span data-ttu-id="aa64a-112">Эта команда удаляет развертывание "RolesDeployment" в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="aa64a-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="aa64a-113">Пример 2: получение развертывания и его удаление</span><span class="sxs-lookup"><span data-stu-id="aa64a-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Remove-AzureRmDeployment
```

<span data-ttu-id="aa64a-114">Эта команда получает развертывание "RolesDeployment" в текущей области подписки и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="aa64a-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="aa64a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa64a-115">PARAMETERS</span></span>

### <span data-ttu-id="aa64a-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aa64a-116">-ApiVersion</span></span>
<span data-ttu-id="aa64a-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa64a-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="aa64a-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="aa64a-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="aa64a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa64a-119">-AsJob</span></span>
<span data-ttu-id="aa64a-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aa64a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa64a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa64a-121">-DefaultProfile</span></span>
<span data-ttu-id="aa64a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa64a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa64a-123">-ID</span><span class="sxs-lookup"><span data-stu-id="aa64a-123">-Id</span></span>
<span data-ttu-id="aa64a-124">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="aa64a-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="aa64a-125">Пример:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="aa64a-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="aa64a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa64a-126">-InputObject</span></span>
<span data-ttu-id="aa64a-127">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="aa64a-127">The deployment object.</span></span>

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

### <span data-ttu-id="aa64a-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa64a-128">-Name</span></span>
<span data-ttu-id="aa64a-129">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="aa64a-129">The name of the deployment.</span></span>

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

### <span data-ttu-id="aa64a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa64a-130">-PassThru</span></span>
<span data-ttu-id="aa64a-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="aa64a-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="aa64a-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="aa64a-132">-Pre</span></span>
<span data-ttu-id="aa64a-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="aa64a-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="aa64a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa64a-134">-Confirm</span></span>
<span data-ttu-id="aa64a-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa64a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa64a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa64a-136">-WhatIf</span></span>
<span data-ttu-id="aa64a-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa64a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa64a-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa64a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa64a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa64a-139">CommonParameters</span></span>
<span data-ttu-id="aa64a-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa64a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa64a-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa64a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa64a-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa64a-142">INPUTS</span></span>

### <span data-ttu-id="aa64a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="aa64a-143">System.String</span></span>

## <span data-ttu-id="aa64a-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa64a-144">OUTPUTS</span></span>

### <span data-ttu-id="aa64a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa64a-145">System.Boolean</span></span>

## <span data-ttu-id="aa64a-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa64a-146">NOTES</span></span>

## <span data-ttu-id="aa64a-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa64a-147">RELATED LINKS</span></span>
