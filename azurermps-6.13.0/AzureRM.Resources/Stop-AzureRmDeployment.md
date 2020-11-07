---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmDeployment.md
ms.openlocfilehash: d8f54706ed37412f6b1081311d90d032b57d2a16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734294"
---
# <span data-ttu-id="bd85f-101">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="bd85f-101">Stop-AzureRmDeployment</span></span>

## <span data-ttu-id="bd85f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd85f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd85f-103">Cancal запущенное развертывание</span><span class="sxs-lookup"><span data-stu-id="bd85f-103">Cancal a running deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd85f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd85f-104">SYNTAX</span></span>

### <span data-ttu-id="bd85f-105">StopByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd85f-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzureRmDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd85f-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="bd85f-106">StopByDeploymentId</span></span>
```
Stop-AzureRmDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd85f-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="bd85f-107">StopByInputObject</span></span>
```
Stop-AzureRmDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd85f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd85f-108">DESCRIPTION</span></span>
<span data-ttu-id="bd85f-109">Командлет **Stop-AzureRmDeployment** отменяет развертывание в области подписки, которая была запущена, но не завершена.</span><span class="sxs-lookup"><span data-stu-id="bd85f-109">The **Stop-AzureRmDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="bd85f-110">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="bd85f-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="bd85f-111">Чтобы создать развертывание в области подписки, используйте командлет New-AzureRmDeployment.</span><span class="sxs-lookup"><span data-stu-id="bd85f-111">To create a deployment at subscription scope, use the New-AzureRmDeployment cmdlet.</span></span>

<span data-ttu-id="bd85f-112">Этот командлет останавливает только одно запущенное развертывание.</span><span class="sxs-lookup"><span data-stu-id="bd85f-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="bd85f-113">Используйте параметр *Name* для остановки определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="bd85f-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="bd85f-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd85f-114">EXAMPLES</span></span>

### <span data-ttu-id="bd85f-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd85f-115">Example 1</span></span>
```
PS C:\>Stop-AzureRmDeployment -Name "deployment01"
```

<span data-ttu-id="bd85f-116">Эта команда отменяет запущенное развертывание "deployment01" в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="bd85f-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="bd85f-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bd85f-117">Example 2</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "deployment01" | Stop-AzureRmDeployment
```

<span data-ttu-id="bd85f-118">Эта команда получает развертывание "deployment01" в текущей области подписки и отменяет ее.</span><span class="sxs-lookup"><span data-stu-id="bd85f-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="bd85f-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd85f-119">PARAMETERS</span></span>

### <span data-ttu-id="bd85f-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bd85f-120">-ApiVersion</span></span>
<span data-ttu-id="bd85f-121">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd85f-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bd85f-122">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="bd85f-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bd85f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd85f-123">-DefaultProfile</span></span>
<span data-ttu-id="bd85f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd85f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd85f-125">-ID</span><span class="sxs-lookup"><span data-stu-id="bd85f-125">-Id</span></span>
<span data-ttu-id="bd85f-126">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="bd85f-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="bd85f-127">Пример:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="bd85f-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="bd85f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd85f-128">-InputObject</span></span>
<span data-ttu-id="bd85f-129">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="bd85f-129">The deployment object.</span></span>

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

### <span data-ttu-id="bd85f-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd85f-130">-Name</span></span>
<span data-ttu-id="bd85f-131">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="bd85f-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="bd85f-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd85f-132">-PassThru</span></span>
<span data-ttu-id="bd85f-133">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="bd85f-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bd85f-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="bd85f-134">-Pre</span></span>
<span data-ttu-id="bd85f-135">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="bd85f-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bd85f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd85f-136">-Confirm</span></span>
<span data-ttu-id="bd85f-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd85f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd85f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd85f-138">-WhatIf</span></span>
<span data-ttu-id="bd85f-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd85f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd85f-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd85f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd85f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd85f-141">CommonParameters</span></span>
<span data-ttu-id="bd85f-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd85f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd85f-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd85f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd85f-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd85f-144">INPUTS</span></span>

### <span data-ttu-id="bd85f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bd85f-145">System.String</span></span>

## <span data-ttu-id="bd85f-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd85f-146">OUTPUTS</span></span>

### <span data-ttu-id="bd85f-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd85f-147">System.Boolean</span></span>

## <span data-ttu-id="bd85f-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd85f-148">NOTES</span></span>

## <span data-ttu-id="bd85f-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd85f-149">RELATED LINKS</span></span>
