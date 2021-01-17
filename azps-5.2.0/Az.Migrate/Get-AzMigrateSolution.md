---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417084"
---
# <span data-ttu-id="dde8c-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="dde8c-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="dde8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dde8c-102">SYNOPSIS</span></span>
<span data-ttu-id="dde8c-103">Получает решение в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="dde8c-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="dde8c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dde8c-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dde8c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dde8c-105">DESCRIPTION</span></span>
<span data-ttu-id="dde8c-106">Получает решение в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="dde8c-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="dde8c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dde8c-107">EXAMPLES</span></span>

### <span data-ttu-id="dde8c-108">Пример 1. Получить</span><span class="sxs-lookup"><span data-stu-id="dde8c-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="dde8c-109">Получить решение migrate project by name (Перенести решение проекта по имени).</span><span class="sxs-lookup"><span data-stu-id="dde8c-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="dde8c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dde8c-110">PARAMETERS</span></span>

### <span data-ttu-id="dde8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde8c-111">-DefaultProfile</span></span>
<span data-ttu-id="dde8c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dde8c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde8c-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="dde8c-113">-MigrateProjectName</span></span>
<span data-ttu-id="dde8c-114">Имя проекта миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="dde8c-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="dde8c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dde8c-115">-Name</span></span>
<span data-ttu-id="dde8c-116">Уникальное имя решения миграции в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="dde8c-116">Unique name of a migration solution within a migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde8c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde8c-117">-ResourceGroupName</span></span>
<span data-ttu-id="dde8c-118">Имя группы ресурсов Azure, в которую входит переносимый проект.</span><span class="sxs-lookup"><span data-stu-id="dde8c-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="dde8c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dde8c-119">-SubscriptionId</span></span>
<span data-ttu-id="dde8c-120">Azure Subscription Id, в котором был создан проект переноса.</span><span class="sxs-lookup"><span data-stu-id="dde8c-120">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde8c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde8c-121">CommonParameters</span></span>
<span data-ttu-id="dde8c-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde8c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde8c-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dde8c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde8c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dde8c-124">INPUTS</span></span>

## <span data-ttu-id="dde8c-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dde8c-125">OUTPUTS</span></span>

### <span data-ttu-id="dde8c-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="dde8c-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="dde8c-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dde8c-127">NOTES</span></span>

<span data-ttu-id="dde8c-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dde8c-128">ALIASES</span></span>

## <span data-ttu-id="dde8c-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dde8c-129">RELATED LINKS</span></span>

