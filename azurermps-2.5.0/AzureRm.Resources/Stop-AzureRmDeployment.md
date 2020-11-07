---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 49ea711740eff624a9560b6d70239edb476dc989
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913739"
---
# <span data-ttu-id="31ecf-101">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="31ecf-101">Stop-AzureRmDeployment</span></span>

## <span data-ttu-id="31ecf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="31ecf-103">Cancal запущенное развертывание</span><span class="sxs-lookup"><span data-stu-id="31ecf-103">Cancal a running deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ecf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31ecf-104">SYNTAX</span></span>

### <span data-ttu-id="31ecf-105">StopByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31ecf-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzureRmDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ecf-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="31ecf-106">StopByDeploymentId</span></span>
```
Stop-AzureRmDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ecf-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="31ecf-107">StopByInputObject</span></span>
```
Stop-AzureRmDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ecf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31ecf-108">DESCRIPTION</span></span>
<span data-ttu-id="31ecf-109">Командлет **Stop-AzureRmDeployment** отменяет развертывание в области подписки, которая была запущена, но не завершена.</span><span class="sxs-lookup"><span data-stu-id="31ecf-109">The **Stop-AzureRmDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="31ecf-110">Чтобы остановить развертывание, необходимо, чтобы развертывание имело неполное состояние подготовки, такое как подготовка, а не завершенное состояние, например подготовка или сбой.</span><span class="sxs-lookup"><span data-stu-id="31ecf-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="31ecf-111">Чтобы создать развертывание в области подписки, используйте командлет New-AzureRmDeployment.</span><span class="sxs-lookup"><span data-stu-id="31ecf-111">To create a deployment at subscription scope, use the New-AzureRmDeployment cmdlet.</span></span>

<span data-ttu-id="31ecf-112">Этот командлет останавливает только одно запущенное развертывание.</span><span class="sxs-lookup"><span data-stu-id="31ecf-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="31ecf-113">Используйте параметр *Name* для остановки определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="31ecf-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="31ecf-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31ecf-114">EXAMPLES</span></span>

### <span data-ttu-id="31ecf-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31ecf-115">Example 1</span></span>
```
PS C:\>Stop-AzureRmDeployment -Name "deployment01"
```

<span data-ttu-id="31ecf-116">Эта команда отменяет запущенное развертывание "deployment01" в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="31ecf-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="31ecf-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="31ecf-117">Example 2</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "deployment01" | Stop-AzureRmDeployment
```

<span data-ttu-id="31ecf-118">Эта команда получает развертывание "deployment01" в текущей области подписки и отменяет ее.</span><span class="sxs-lookup"><span data-stu-id="31ecf-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="31ecf-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31ecf-119">PARAMETERS</span></span>

### <span data-ttu-id="31ecf-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="31ecf-120">-ApiVersion</span></span>
<span data-ttu-id="31ecf-121">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31ecf-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="31ecf-122">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="31ecf-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="31ecf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ecf-123">-DefaultProfile</span></span>
<span data-ttu-id="31ecf-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31ecf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31ecf-125">-ID</span><span class="sxs-lookup"><span data-stu-id="31ecf-125">-Id</span></span>
<span data-ttu-id="31ecf-126">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="31ecf-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="31ecf-127">Пример:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="31ecf-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="31ecf-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31ecf-128">-InputObject</span></span>
<span data-ttu-id="31ecf-129">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="31ecf-129">The deployment object.</span></span>

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

### <span data-ttu-id="31ecf-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31ecf-130">-Name</span></span>
<span data-ttu-id="31ecf-131">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="31ecf-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="31ecf-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31ecf-132">-PassThru</span></span>
<span data-ttu-id="31ecf-133">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="31ecf-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="31ecf-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="31ecf-134">-Pre</span></span>
<span data-ttu-id="31ecf-135">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="31ecf-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="31ecf-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31ecf-136">-Confirm</span></span>
<span data-ttu-id="31ecf-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="31ecf-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ecf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ecf-138">-WhatIf</span></span>
<span data-ttu-id="31ecf-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31ecf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31ecf-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="31ecf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ecf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ecf-141">CommonParameters</span></span>
<span data-ttu-id="31ecf-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31ecf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ecf-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ecf-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ecf-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31ecf-144">INPUTS</span></span>

### <span data-ttu-id="31ecf-145">System. String</span><span class="sxs-lookup"><span data-stu-id="31ecf-145">System.String</span></span>

## <span data-ttu-id="31ecf-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31ecf-146">OUTPUTS</span></span>

### <span data-ttu-id="31ecf-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31ecf-147">System.Boolean</span></span>

## <span data-ttu-id="31ecf-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="31ecf-148">NOTES</span></span>

## <span data-ttu-id="31ecf-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31ecf-149">RELATED LINKS</span></span>
