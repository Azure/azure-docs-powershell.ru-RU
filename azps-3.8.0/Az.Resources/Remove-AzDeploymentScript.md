---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: a15804d0af664c46d443128e940e3b9f2c8a1acc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065270"
---
# <span data-ttu-id="a20a6-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a20a6-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="a20a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a20a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a20a6-103">Удаление сценария развертывания и связанных с ним ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a20a6-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="a20a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a20a6-104">SYNTAX</span></span>

### <span data-ttu-id="a20a6-105">RemoveDeploymentScriptLogByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a20a6-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a6-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="a20a6-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a6-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="a20a6-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a20a6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a20a6-108">DESCRIPTION</span></span>
<span data-ttu-id="a20a6-109">Командлет **Remove-AzDeploymentScript** удаляет скрипт развертывания и связанные с ним ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a20a6-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="a20a6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a20a6-110">EXAMPLES</span></span>

### <span data-ttu-id="a20a6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a20a6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="a20a6-112">Удаление сценария развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="a20a6-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="a20a6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a20a6-113">PARAMETERS</span></span>

### <span data-ttu-id="a20a6-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a20a6-114">-Confirm</span></span>
<span data-ttu-id="a20a6-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a20a6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a20a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20a6-116">-DefaultProfile</span></span>
<span data-ttu-id="a20a6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a20a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a20a6-118">-ID</span><span class="sxs-lookup"><span data-stu-id="a20a6-118">-Id</span></span>
<span data-ttu-id="a20a6-119">Полный идентификатор ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="a20a6-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="a20a6-120">Пример:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="a20a6-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a20a6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a20a6-121">-InputObject</span></span>
<span data-ttu-id="a20a6-122">Объект PowerShell для сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="a20a6-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a20a6-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a20a6-123">-Name</span></span>
<span data-ttu-id="a20a6-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a20a6-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a20a6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a20a6-125">-PassThru</span></span>
<span data-ttu-id="a20a6-126">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="a20a6-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a20a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a20a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="a20a6-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a20a6-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a20a6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20a6-129">-WhatIf</span></span>
<span data-ttu-id="a20a6-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a20a6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a20a6-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a20a6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a20a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20a6-132">CommonParameters</span></span>
<span data-ttu-id="a20a6-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a20a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a20a6-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a20a6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20a6-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a20a6-135">INPUTS</span></span>

### <span data-ttu-id="a20a6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a20a6-136">System.String</span></span>

### <span data-ttu-id="a20a6-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a20a6-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="a20a6-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a20a6-138">OUTPUTS</span></span>

### <span data-ttu-id="a20a6-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a20a6-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="a20a6-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="a20a6-140">NOTES</span></span>

## <span data-ttu-id="a20a6-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a20a6-141">RELATED LINKS</span></span>
