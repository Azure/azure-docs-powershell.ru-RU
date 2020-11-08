---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248871"
---
# <span data-ttu-id="8a079-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="8a079-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="8a079-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a079-102">SYNOPSIS</span></span>
<span data-ttu-id="8a079-103">Возвращает решение в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="8a079-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="8a079-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a079-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8a079-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a079-105">DESCRIPTION</span></span>
<span data-ttu-id="8a079-106">Возвращает решение в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="8a079-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="8a079-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a079-107">EXAMPLES</span></span>

### <span data-ttu-id="8a079-108">Пример 1: Get</span><span class="sxs-lookup"><span data-stu-id="8a079-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="8a079-109">Подготовьте миграцию решения проекта по имени.</span><span class="sxs-lookup"><span data-stu-id="8a079-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="8a079-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a079-110">PARAMETERS</span></span>

### <span data-ttu-id="8a079-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a079-111">-DefaultProfile</span></span>
<span data-ttu-id="8a079-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a079-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a079-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="8a079-113">-MigrateProjectName</span></span>
<span data-ttu-id="8a079-114">Имя проекта для миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="8a079-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="8a079-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a079-115">-Name</span></span>
<span data-ttu-id="8a079-116">Уникальное имя решения для миграции в рамках миграции проекта.</span><span class="sxs-lookup"><span data-stu-id="8a079-116">Unique name of a migration solution within a migrate project.</span></span>

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

### <span data-ttu-id="8a079-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a079-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a079-118">Имя группы ресурсов Azure, в состав которой входит переносимый проект.</span><span class="sxs-lookup"><span data-stu-id="8a079-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="8a079-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a079-119">-SubscriptionId</span></span>
<span data-ttu-id="8a079-120">Идентификатор подписки Azure, в которой был создан проект миграции.</span><span class="sxs-lookup"><span data-stu-id="8a079-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="8a079-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a079-121">CommonParameters</span></span>
<span data-ttu-id="8a079-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a079-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a079-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a079-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a079-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a079-124">INPUTS</span></span>

## <span data-ttu-id="8a079-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a079-125">OUTPUTS</span></span>

### <span data-ttu-id="8a079-126">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180901Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="8a079-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="8a079-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a079-127">NOTES</span></span>

<span data-ttu-id="8a079-128">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="8a079-128">ALIASES</span></span>

## <span data-ttu-id="8a079-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a079-129">RELATED LINKS</span></span>

