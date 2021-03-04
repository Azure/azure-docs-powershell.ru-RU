---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedroppedsqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
ms.openlocfilehash: 26e4e5c77913f01b8a7097f6baebd68977ceed22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981832"
---
# <span data-ttu-id="39d37-101">Get-AzSynapseDroppedSqlPool</span><span class="sxs-lookup"><span data-stu-id="39d37-101">Get-AzSynapseDroppedSqlPool</span></span>

## <span data-ttu-id="39d37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39d37-102">SYNOPSIS</span></span>
<span data-ttu-id="39d37-103">Получает резервную копию SQL-пула Synapse Sql.</span><span class="sxs-lookup"><span data-stu-id="39d37-103">Gets a dropped Sql pool backup of a Synapse Sql Pool.</span></span>

## <span data-ttu-id="39d37-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39d37-104">SYNTAX</span></span>

### <span data-ttu-id="39d37-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39d37-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39d37-106">DroppedSqlPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="39d37-106">DroppedSqlPoolResourceId</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39d37-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39d37-107">DESCRIPTION</span></span>
<span data-ttu-id="39d37-108">Для **этого** вы получаете указанную удаленную резервную копию пула SQL, которую можно восстановить, или все удаленные резервные копии, которые можно восстановить в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="39d37-108">The **Get-AzSynapseDroppedSqlPool** cmdlet gets a specified deleted SQL pool backup that you can restore, or all deleted backups that you can restore in a workspace.</span></span> 


## <span data-ttu-id="39d37-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39d37-109">EXAMPLES</span></span>

### <span data-ttu-id="39d37-110">Пример 1. Получить указанные пропаданые sqlpools из SQL-пула</span><span class="sxs-lookup"><span data-stu-id="39d37-110">Example 1: Get a specified dropped sqlpools from a sql pool</span></span>
```powershell
PS C:\> Get-AzSynapseDroppedSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name "ContosoSqlPool"
```
<span data-ttu-id="39d37-111">Он извлекает сброшенные sqlpools для SQL-пула.</span><span class="sxs-lookup"><span data-stu-id="39d37-111">The cmdlet retrieves dropped sqlpools for a sql pool.</span></span>

### <span data-ttu-id="39d37-112">Пример 2. Все перепахленные sqlpool в рабочей области</span><span class="sxs-lookup"><span data-stu-id="39d37-112">Example 2: Get all dropped sqlpool on a workspace</span></span>
```
PS C:\>Get-AzSynapseDroppedSqlPool -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="39d37-113">Эта команда получает все доступные перепады sqlpool в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="39d37-113">This command gets all available dropped sqlpool on a specified workspace.</span></span>

## <span data-ttu-id="39d37-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39d37-114">PARAMETERS</span></span>

### <span data-ttu-id="39d37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d37-115">-DefaultProfile</span></span>
<span data-ttu-id="39d37-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39d37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d37-117">-Name</span><span class="sxs-lookup"><span data-stu-id="39d37-117">-Name</span></span>
<span data-ttu-id="39d37-118">Пул SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="39d37-118">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: AzSynapseDroppedSqlPool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d37-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39d37-119">-ResourceId</span></span>
<span data-ttu-id="39d37-120">Ввести упадет ИД пула SQL.</span><span class="sxs-lookup"><span data-stu-id="39d37-120">Input a Dropped Sql Pool Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DroppedSqlPoolResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39d37-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d37-121">-ResourceGroupName</span></span>
<span data-ttu-id="39d37-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39d37-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d37-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="39d37-123">-WorkspaceName</span></span>
<span data-ttu-id="39d37-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="39d37-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d37-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d37-125">CommonParameters</span></span>
<span data-ttu-id="39d37-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d37-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d37-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39d37-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d37-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39d37-128">INPUTS</span></span>

### <span data-ttu-id="39d37-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="39d37-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="39d37-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39d37-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="39d37-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39d37-131">OUTPUTS</span></span>

### <span data-ttu-id="39d37-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span><span class="sxs-lookup"><span data-stu-id="39d37-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span></span>

## <span data-ttu-id="39d37-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39d37-133">NOTES</span></span>

## <span data-ttu-id="39d37-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39d37-134">RELATED LINKS</span></span>
