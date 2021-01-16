---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: b5c3ca86129e622a90a84d099961a8f8dd433eef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325349"
---
# <span data-ttu-id="94892-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="94892-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="94892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94892-102">SYNOPSIS</span></span>
<span data-ttu-id="94892-103">Получает или перечисляет сценарии развертывания.</span><span class="sxs-lookup"><span data-stu-id="94892-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="94892-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94892-104">SYNTAX</span></span>

### <span data-ttu-id="94892-105">ListDeploymentScript (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94892-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94892-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="94892-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94892-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="94892-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94892-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94892-108">DESCRIPTION</span></span>
<span data-ttu-id="94892-109">Для **этого можно** получить один сценарий развертывания или список сценариев.</span><span class="sxs-lookup"><span data-stu-id="94892-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="94892-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94892-110">EXAMPLES</span></span>

### <span data-ttu-id="94892-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94892-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="94892-112">Сценарии развертывания в подписке перечислены в контексте текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="94892-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="94892-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94892-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="94892-114">Сценарии развертывания в группе ресурсов DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="94892-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="94892-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="94892-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="94892-116">Возвращает сценарий развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="94892-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="94892-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="94892-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="94892-118">Сценарий развертывания с заданным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="94892-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="94892-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94892-119">PARAMETERS</span></span>

### <span data-ttu-id="94892-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94892-120">-DefaultProfile</span></span>
<span data-ttu-id="94892-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94892-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94892-122">-Id</span><span class="sxs-lookup"><span data-stu-id="94892-122">-Id</span></span>
<span data-ttu-id="94892-123">Полное ид ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="94892-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="94892-124">Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="94892-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94892-125">-Name</span><span class="sxs-lookup"><span data-stu-id="94892-125">-Name</span></span>
<span data-ttu-id="94892-126">Имя сценария развертывания</span><span class="sxs-lookup"><span data-stu-id="94892-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94892-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94892-127">-ResourceGroupName</span></span>
<span data-ttu-id="94892-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94892-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94892-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94892-129">CommonParameters</span></span>
<span data-ttu-id="94892-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94892-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="94892-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94892-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94892-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94892-132">INPUTS</span></span>

### <span data-ttu-id="94892-133">System.String</span><span class="sxs-lookup"><span data-stu-id="94892-133">System.String</span></span>

## <span data-ttu-id="94892-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94892-134">OUTPUTS</span></span>

### <span data-ttu-id="94892-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="94892-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="94892-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94892-136">NOTES</span></span>

## <span data-ttu-id="94892-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94892-137">RELATED LINKS</span></span>