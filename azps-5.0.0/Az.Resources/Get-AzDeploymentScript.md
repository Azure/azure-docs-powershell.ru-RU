---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: b5c3ca86129e622a90a84d099961a8f8dd433eef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245906"
---
# <span data-ttu-id="a1d64-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a1d64-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="a1d64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1d64-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d64-103">Возвращает или перечисляет сценарии развертывания.</span><span class="sxs-lookup"><span data-stu-id="a1d64-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="a1d64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1d64-104">SYNTAX</span></span>

### <span data-ttu-id="a1d64-105">ListDeploymentScript (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1d64-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1d64-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="a1d64-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1d64-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d64-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1d64-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1d64-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d64-109">Командлет **Get-AzDeploymentScript** получает один сценарий развертывания или список сценариев развертывания.</span><span class="sxs-lookup"><span data-stu-id="a1d64-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="a1d64-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1d64-110">EXAMPLES</span></span>

### <span data-ttu-id="a1d64-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1d64-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="a1d64-112">Список сценариев развертывания в подписке в контексте текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a1d64-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="a1d64-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a1d64-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="a1d64-114">Список сценариев развертывания в группе ресурсов DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="a1d64-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="a1d64-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a1d64-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="a1d64-116">Возвращает сценарий развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="a1d64-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="a1d64-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a1d64-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="a1d64-118">Получает скрипт развертывания с заданным идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1d64-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="a1d64-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1d64-119">PARAMETERS</span></span>

### <span data-ttu-id="a1d64-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d64-120">-DefaultProfile</span></span>
<span data-ttu-id="a1d64-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d64-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d64-122">-ID</span><span class="sxs-lookup"><span data-stu-id="a1d64-122">-Id</span></span>
<span data-ttu-id="a1d64-123">Полный идентификатор ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="a1d64-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="a1d64-124">Пример:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="a1d64-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="a1d64-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1d64-125">-Name</span></span>
<span data-ttu-id="a1d64-126">Имя скрипта развертывания.</span><span class="sxs-lookup"><span data-stu-id="a1d64-126">The name of the deployment script</span></span>

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

### <span data-ttu-id="a1d64-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d64-127">-ResourceGroupName</span></span>
<span data-ttu-id="a1d64-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1d64-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1d64-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d64-129">CommonParameters</span></span>
<span data-ttu-id="a1d64-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1d64-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a1d64-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1d64-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d64-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1d64-132">INPUTS</span></span>

### <span data-ttu-id="a1d64-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d64-133">System.String</span></span>

## <span data-ttu-id="a1d64-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1d64-134">OUTPUTS</span></span>

### <span data-ttu-id="a1d64-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a1d64-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="a1d64-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1d64-136">NOTES</span></span>

## <span data-ttu-id="a1d64-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1d64-137">RELATED LINKS</span></span>