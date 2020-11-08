---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245144"
---
# <span data-ttu-id="5679e-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5679e-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="5679e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5679e-102">SYNOPSIS</span></span>
<span data-ttu-id="5679e-103">Проверка существования пула SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="5679e-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5679e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5679e-104">SYNTAX</span></span>

### <span data-ttu-id="5679e-105">TestByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5679e-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5679e-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5679e-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5679e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5679e-107">DESCRIPTION</span></span>
<span data-ttu-id="5679e-108">Командлет **Test-AzSynapseSqlPool** проверяет наличие пула SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="5679e-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5679e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5679e-109">EXAMPLES</span></span>

### <span data-ttu-id="5679e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5679e-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="5679e-111">Эта команда проверяет существование указанного пула SQL.</span><span class="sxs-lookup"><span data-stu-id="5679e-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="5679e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5679e-112">PARAMETERS</span></span>

### <span data-ttu-id="5679e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5679e-113">-DefaultProfile</span></span>
<span data-ttu-id="5679e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5679e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5679e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5679e-115">-Name</span></span>
<span data-ttu-id="5679e-116">Имя пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5679e-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="5679e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5679e-117">-ResourceGroupName</span></span>
<span data-ttu-id="5679e-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5679e-118">Resource group name.</span></span>

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

### <span data-ttu-id="5679e-119">-Version</span><span class="sxs-lookup"><span data-stu-id="5679e-119">-Version</span></span>
<span data-ttu-id="5679e-120">Версия пула Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="5679e-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="5679e-121">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="5679e-121">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5679e-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5679e-122">-WorkspaceName</span></span>
<span data-ttu-id="5679e-123">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5679e-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5679e-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5679e-124">-WorkspaceObject</span></span>
<span data-ttu-id="5679e-125">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="5679e-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5679e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5679e-126">CommonParameters</span></span>
<span data-ttu-id="5679e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5679e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5679e-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5679e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5679e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5679e-129">INPUTS</span></span>

### <span data-ttu-id="5679e-130">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5679e-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5679e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5679e-131">OUTPUTS</span></span>

### <span data-ttu-id="5679e-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="5679e-132">System.Object</span></span>
## <span data-ttu-id="5679e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5679e-133">NOTES</span></span>

## <span data-ttu-id="5679e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5679e-134">RELATED LINKS</span></span>
