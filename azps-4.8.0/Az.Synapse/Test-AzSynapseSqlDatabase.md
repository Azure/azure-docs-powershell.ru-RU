---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077460"
---
# <span data-ttu-id="68412-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="68412-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="68412-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68412-102">SYNOPSIS</span></span>
<span data-ttu-id="68412-103">Проверка существования базы данных SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="68412-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="68412-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68412-104">SYNTAX</span></span>

### <span data-ttu-id="68412-105">TestByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="68412-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68412-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68412-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68412-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68412-107">DESCRIPTION</span></span>
<span data-ttu-id="68412-108">Командлет **Test-AzSynapseSqlDatabase** проверяет наличие базы данных SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="68412-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="68412-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68412-109">EXAMPLES</span></span>

### <span data-ttu-id="68412-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="68412-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="68412-111">Эта команда проверяет существование указанной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="68412-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="68412-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68412-112">PARAMETERS</span></span>

### <span data-ttu-id="68412-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68412-113">-DefaultProfile</span></span>
<span data-ttu-id="68412-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68412-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68412-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="68412-115">-Name</span></span>
<span data-ttu-id="68412-116">Имя базы данных SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="68412-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="68412-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68412-117">-ResourceGroupName</span></span>
<span data-ttu-id="68412-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68412-118">Resource group name.</span></span>

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

### <span data-ttu-id="68412-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="68412-119">-WorkspaceName</span></span>
<span data-ttu-id="68412-120">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="68412-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="68412-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="68412-121">-WorkspaceObject</span></span>
<span data-ttu-id="68412-122">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="68412-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="68412-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68412-123">CommonParameters</span></span>
<span data-ttu-id="68412-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68412-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68412-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68412-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68412-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68412-126">INPUTS</span></span>

### <span data-ttu-id="68412-127">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="68412-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="68412-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68412-128">OUTPUTS</span></span>

### <span data-ttu-id="68412-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68412-129">System.Boolean</span></span>

## <span data-ttu-id="68412-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="68412-130">NOTES</span></span>

## <span data-ttu-id="68412-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68412-131">RELATED LINKS</span></span>