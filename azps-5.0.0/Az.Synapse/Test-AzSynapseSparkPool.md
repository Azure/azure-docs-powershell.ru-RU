---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245148"
---
# <span data-ttu-id="d3af6-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="d3af6-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="d3af6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3af6-102">SYNOPSIS</span></span>
<span data-ttu-id="d3af6-103">Проверка существования пула Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="d3af6-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="d3af6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3af6-104">SYNTAX</span></span>

### <span data-ttu-id="d3af6-105">TestByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3af6-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3af6-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3af6-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3af6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3af6-107">DESCRIPTION</span></span>
<span data-ttu-id="d3af6-108">Командлет **Test-AzSynapseSparkPool** проверяет наличие пула Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="d3af6-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="d3af6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3af6-109">EXAMPLES</span></span>

### <span data-ttu-id="d3af6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3af6-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="d3af6-111">Эта команда проверяет существование указанного пула Spark.</span><span class="sxs-lookup"><span data-stu-id="d3af6-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="d3af6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3af6-112">PARAMETERS</span></span>

### <span data-ttu-id="d3af6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3af6-113">-DefaultProfile</span></span>
<span data-ttu-id="d3af6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3af6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3af6-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3af6-115">-Name</span></span>
<span data-ttu-id="d3af6-116">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="d3af6-116">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3af6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3af6-117">-ResourceGroupName</span></span>
<span data-ttu-id="d3af6-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d3af6-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3af6-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d3af6-119">-WorkspaceName</span></span>
<span data-ttu-id="d3af6-120">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d3af6-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3af6-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d3af6-121">-WorkspaceObject</span></span>
<span data-ttu-id="d3af6-122">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="d3af6-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3af6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3af6-123">CommonParameters</span></span>
<span data-ttu-id="d3af6-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3af6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3af6-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3af6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3af6-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3af6-126">INPUTS</span></span>

### <span data-ttu-id="d3af6-127">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d3af6-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d3af6-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3af6-128">OUTPUTS</span></span>

### <span data-ttu-id="d3af6-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="d3af6-129">System.Object</span></span>
## <span data-ttu-id="d3af6-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3af6-130">NOTES</span></span>

## <span data-ttu-id="d3af6-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3af6-131">RELATED LINKS</span></span>
