---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074319"
---
# <span data-ttu-id="34ea1-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="34ea1-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="34ea1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="34ea1-103">Получает журнал выполнения скрипта развертывания.</span><span class="sxs-lookup"><span data-stu-id="34ea1-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="34ea1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34ea1-104">SYNTAX</span></span>

### <span data-ttu-id="34ea1-105">GetDeploymentScriptLogByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34ea1-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34ea1-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="34ea1-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34ea1-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="34ea1-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34ea1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34ea1-108">DESCRIPTION</span></span>
<span data-ttu-id="34ea1-109">Командлет **Get-AzDeploymentScriptLog** получает журнал выполнения скрипта развертывания.</span><span class="sxs-lookup"><span data-stu-id="34ea1-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="34ea1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34ea1-110">EXAMPLES</span></span>

### <span data-ttu-id="34ea1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34ea1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="34ea1-112">Получает журнал сценария развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="34ea1-112">Gets log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="34ea1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="34ea1-113">Example 2</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="34ea1-114">Первая команда получает сценарий развертывания с именем MyDeploymentScript в группе ресурсов DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="34ea1-114">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="34ea1-115">Вторая команда получает журнал заданного сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="34ea1-115">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="34ea1-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34ea1-116">PARAMETERS</span></span>

### <span data-ttu-id="34ea1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ea1-117">-DefaultProfile</span></span>
<span data-ttu-id="34ea1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34ea1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34ea1-119">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="34ea1-119">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="34ea1-120">Объект PowerShell для сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="34ea1-120">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea1-121">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="34ea1-121">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="34ea1-122">Полный идентификатор ресурса сценария развертывания.</span><span class="sxs-lookup"><span data-stu-id="34ea1-122">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="34ea1-123">Пример:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="34ea1-123">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ea1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34ea1-124">-Name</span></span>
<span data-ttu-id="34ea1-125">Имя скрипта развертывания.</span><span class="sxs-lookup"><span data-stu-id="34ea1-125">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34ea1-126">-ResourceGroupName</span></span>
<span data-ttu-id="34ea1-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34ea1-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ea1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ea1-128">CommonParameters</span></span>
<span data-ttu-id="34ea1-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34ea1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="34ea1-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ea1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ea1-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34ea1-131">INPUTS</span></span>

### <span data-ttu-id="34ea1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="34ea1-132">System.String</span></span>

### <span data-ttu-id="34ea1-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="34ea1-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="34ea1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34ea1-134">OUTPUTS</span></span>

### <span data-ttu-id="34ea1-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="34ea1-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="34ea1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="34ea1-136">NOTES</span></span>

## <span data-ttu-id="34ea1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34ea1-137">RELATED LINKS</span></span>
