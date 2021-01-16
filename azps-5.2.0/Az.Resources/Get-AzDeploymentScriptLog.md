---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325348"
---
# <span data-ttu-id="62068-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="62068-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="62068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62068-102">SYNOPSIS</span></span>
<span data-ttu-id="62068-103">Журнал выполнения сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="62068-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="62068-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62068-104">SYNTAX</span></span>

### <span data-ttu-id="62068-105">GetDeploymentScriptLogByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62068-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62068-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="62068-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62068-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="62068-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62068-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62068-108">DESCRIPTION</span></span>
<span data-ttu-id="62068-109">С **его учетом** можно получить журнал выполнения сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="62068-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="62068-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62068-110">EXAMPLES</span></span>

### <span data-ttu-id="62068-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62068-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="62068-112">Получает журнал сценария развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="62068-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="62068-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="62068-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="62068-114">Возвращает последние 3 строки журнала сценария развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="62068-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="62068-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="62068-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="62068-116">Первая команда получает сценарий развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="62068-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="62068-117">Вторая команда получает журнал заданного сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="62068-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="62068-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62068-118">PARAMETERS</span></span>

### <span data-ttu-id="62068-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62068-119">-DefaultProfile</span></span>
<span data-ttu-id="62068-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62068-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62068-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="62068-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="62068-122">Объект PowerShell сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="62068-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="62068-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="62068-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="62068-124">Полное ид ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="62068-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="62068-125">Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="62068-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="62068-126">-Name</span><span class="sxs-lookup"><span data-stu-id="62068-126">-Name</span></span>
<span data-ttu-id="62068-127">Имя сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="62068-127">The name of the deployment script.</span></span>

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

### <span data-ttu-id="62068-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62068-128">-ResourceGroupName</span></span>
<span data-ttu-id="62068-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62068-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="62068-130">-Tail</span><span class="sxs-lookup"><span data-stu-id="62068-130">-Tail</span></span>
<span data-ttu-id="62068-131">Ограничение вывода последними n строками</span><span class="sxs-lookup"><span data-stu-id="62068-131">Limit output to last n lines</span></span>

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

### <span data-ttu-id="62068-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62068-132">CommonParameters</span></span>
<span data-ttu-id="62068-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62068-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62068-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62068-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62068-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62068-135">INPUTS</span></span>

### <span data-ttu-id="62068-136">System.String</span><span class="sxs-lookup"><span data-stu-id="62068-136">System.String</span></span>

### <span data-ttu-id="62068-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="62068-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="62068-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62068-138">OUTPUTS</span></span>

### <span data-ttu-id="62068-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="62068-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="62068-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62068-140">NOTES</span></span>

## <span data-ttu-id="62068-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62068-141">RELATED LINKS</span></span>
