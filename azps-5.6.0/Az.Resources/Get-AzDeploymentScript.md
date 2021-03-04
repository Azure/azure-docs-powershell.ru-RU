---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 7b61444bb4f3a23e1611e90b79545e1c174b0437
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956643"
---
# <span data-ttu-id="fdedd-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="fdedd-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="fdedd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdedd-102">SYNOPSIS</span></span>
<span data-ttu-id="fdedd-103">Получает или перечисляет сценарии развертывания.</span><span class="sxs-lookup"><span data-stu-id="fdedd-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="fdedd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fdedd-104">SYNTAX</span></span>

### <span data-ttu-id="fdedd-105">ListDeploymentScript (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fdedd-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdedd-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="fdedd-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdedd-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="fdedd-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdedd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdedd-108">DESCRIPTION</span></span>
<span data-ttu-id="fdedd-109">Для **работы с cmdlet Get-AzDeploymentScript** требуется один сценарий развертывания или список сценариев развертывания.</span><span class="sxs-lookup"><span data-stu-id="fdedd-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="fdedd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fdedd-110">EXAMPLES</span></span>

### <span data-ttu-id="fdedd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fdedd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="fdedd-112">Сценарии развертывания в подписке перечислены в контексте текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="fdedd-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="fdedd-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fdedd-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="fdedd-114">Сценарии развертывания в группе ресурсов DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="fdedd-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="fdedd-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="fdedd-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="fdedd-116">Получает сценарий развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="fdedd-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="fdedd-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="fdedd-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="fdedd-118">Сценарий развертывания с заданным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="fdedd-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="fdedd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdedd-119">PARAMETERS</span></span>

### <span data-ttu-id="fdedd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdedd-120">-DefaultProfile</span></span>
<span data-ttu-id="fdedd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fdedd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdedd-122">-Id</span><span class="sxs-lookup"><span data-stu-id="fdedd-122">-Id</span></span>
<span data-ttu-id="fdedd-123">Полное ид ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="fdedd-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="fdedd-124">Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="fdedd-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="fdedd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fdedd-125">-Name</span></span>
<span data-ttu-id="fdedd-126">Имя сценария развертывания</span><span class="sxs-lookup"><span data-stu-id="fdedd-126">The name of the deployment script</span></span>

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

### <span data-ttu-id="fdedd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdedd-127">-ResourceGroupName</span></span>
<span data-ttu-id="fdedd-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fdedd-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="fdedd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdedd-129">CommonParameters</span></span>
<span data-ttu-id="fdedd-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdedd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fdedd-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdedd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdedd-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdedd-132">INPUTS</span></span>

### <span data-ttu-id="fdedd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fdedd-133">System.String</span></span>

## <span data-ttu-id="fdedd-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fdedd-134">OUTPUTS</span></span>

### <span data-ttu-id="fdedd-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="fdedd-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="fdedd-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fdedd-136">NOTES</span></span>

## <span data-ttu-id="fdedd-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fdedd-137">RELATED LINKS</span></span>