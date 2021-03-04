---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/initialize-azmigratereplicationinfrastructure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
ms.openlocfilehash: 27206ac1c4e256efcd4093c8cdc9647b6059b3ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982787"
---
# <span data-ttu-id="6700b-101">Initialize-AzMigrateReplicationInfrastructure</span><span class="sxs-lookup"><span data-stu-id="6700b-101">Initialize-AzMigrateReplicationInfrastructure</span></span>

## <span data-ttu-id="6700b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6700b-102">SYNOPSIS</span></span>
<span data-ttu-id="6700b-103">Инициализирует инфраструктуру проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="6700b-103">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="6700b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6700b-104">SYNTAX</span></span>

```
Initialize-AzMigrateReplicationInfrastructure -ProjectName <String> -ResourceGroupName <String>
 -Scenario <String> -TargetRegion <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6700b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6700b-105">DESCRIPTION</span></span>
<span data-ttu-id="6700b-106">Этот Initialize-AzMigrateReplicationInfrastructure инициализирует инфраструктуру проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="6700b-106">The Initialize-AzMigrateReplicationInfrastructure cmdlet initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="6700b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6700b-107">EXAMPLES</span></span>

### <span data-ttu-id="6700b-108">Пример 1. Инициализирует инфраструктуру проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="6700b-108">Example 1: Initialises the infrastructure for the migrate project.</span></span>
```powershell
PS C:\> Initialize-AzMigrateReplicationInfrastructure.ps1 -ResourceGroupName TestRG  -ProjectName TestProject -Vmwareagentless -TargetRegion centralus

True
```

<span data-ttu-id="6700b-109">Инициализирует инфраструктуру проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="6700b-109">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="6700b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6700b-110">PARAMETERS</span></span>

### <span data-ttu-id="6700b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6700b-111">-DefaultProfile</span></span>
<span data-ttu-id="6700b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6700b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6700b-113">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="6700b-113">-ProjectName</span></span>
<span data-ttu-id="6700b-114">Имя проекта миграции Azure Migrate, который будет использоваться для миграции на сервер.</span><span class="sxs-lookup"><span data-stu-id="6700b-114">Specifies the name of the Azure Migrate project to be used for server migration.</span></span>

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

### <span data-ttu-id="6700b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6700b-115">-ResourceGroupName</span></span>
<span data-ttu-id="6700b-116">Группа ресурсов в azure Migrate Project в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="6700b-116">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="6700b-117">-Scenario</span><span class="sxs-lookup"><span data-stu-id="6700b-117">-Scenario</span></span>
<span data-ttu-id="6700b-118">Определяет сценарий миграции сервера, для которого необходимо инициализировать инфраструктуру репликации.</span><span class="sxs-lookup"><span data-stu-id="6700b-118">Specifies the server migration scenario for which the replication infrastructure needs to be initialized.</span></span>

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

### <span data-ttu-id="6700b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6700b-119">-SubscriptionId</span></span>
<span data-ttu-id="6700b-120">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="6700b-120">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6700b-121">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="6700b-121">-TargetRegion</span></span>
<span data-ttu-id="6700b-122">Определяет целевой регион Azure для миграции на сервер.</span><span class="sxs-lookup"><span data-stu-id="6700b-122">Specifies the target Azure region for server migrations.</span></span>

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

### <span data-ttu-id="6700b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6700b-123">-Confirm</span></span>
<span data-ttu-id="6700b-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6700b-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6700b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6700b-125">-WhatIf</span></span>
<span data-ttu-id="6700b-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6700b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6700b-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6700b-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6700b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6700b-128">CommonParameters</span></span>
<span data-ttu-id="6700b-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6700b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6700b-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6700b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6700b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6700b-131">INPUTS</span></span>

## <span data-ttu-id="6700b-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6700b-132">OUTPUTS</span></span>

### <span data-ttu-id="6700b-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6700b-133">System.Boolean</span></span>

## <span data-ttu-id="6700b-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6700b-134">NOTES</span></span>

<span data-ttu-id="6700b-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6700b-135">ALIASES</span></span>

## <span data-ttu-id="6700b-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6700b-136">RELATED LINKS</span></span>

