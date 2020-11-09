---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244229"
---
# <span data-ttu-id="3726e-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="3726e-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="3726e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3726e-102">SYNOPSIS</span></span>
<span data-ttu-id="3726e-103">Получает журнал выполнения скрипта развертывания.</span><span class="sxs-lookup"><span data-stu-id="3726e-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="3726e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3726e-104">SYNTAX</span></span>

### <span data-ttu-id="3726e-105">GetDeploymentScriptLogByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3726e-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3726e-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="3726e-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3726e-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="3726e-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3726e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3726e-108">DESCRIPTION</span></span>
<span data-ttu-id="3726e-109">Командлет **Get-AzDeploymentScriptLog** получает журнал выполнения скрипта развертывания.</span><span class="sxs-lookup"><span data-stu-id="3726e-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="3726e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3726e-110">EXAMPLES</span></span>

### <span data-ttu-id="3726e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3726e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="3726e-112">Получает журнал сценария развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="3726e-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="3726e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3726e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="3726e-114">Получает последние 3 строки журнала сценария развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="3726e-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="3726e-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3726e-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="3726e-116">Первая команда получает сценарий развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="3726e-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="3726e-117">Вторая команда получает журнал заданного сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="3726e-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="3726e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3726e-118">PARAMETERS</span></span>

### <span data-ttu-id="3726e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3726e-119">-DefaultProfile</span></span>
<span data-ttu-id="3726e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3726e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3726e-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="3726e-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="3726e-122">Объект PowerShell для сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="3726e-122">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3726e-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="3726e-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="3726e-124">Полный идентификатор ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="3726e-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="3726e-125">Пример:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="3726e-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3726e-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3726e-126">-Name</span></span>
<span data-ttu-id="3726e-127">Имя скрипта развертывания.</span><span class="sxs-lookup"><span data-stu-id="3726e-127">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3726e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3726e-128">-ResourceGroupName</span></span>
<span data-ttu-id="3726e-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3726e-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3726e-130">-Tail</span><span class="sxs-lookup"><span data-stu-id="3726e-130">-Tail</span></span>
<span data-ttu-id="3726e-131">Ограничить вывод на последние n строк</span><span class="sxs-lookup"><span data-stu-id="3726e-131">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3726e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3726e-132">CommonParameters</span></span>
<span data-ttu-id="3726e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3726e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3726e-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3726e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3726e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3726e-135">INPUTS</span></span>

### <span data-ttu-id="3726e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3726e-136">System.String</span></span>

### <span data-ttu-id="3726e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="3726e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="3726e-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3726e-138">OUTPUTS</span></span>

### <span data-ttu-id="3726e-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="3726e-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="3726e-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="3726e-140">NOTES</span></span>

## <span data-ttu-id="3726e-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3726e-141">RELATED LINKS</span></span>