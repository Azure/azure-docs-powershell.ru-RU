---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 4176b07f8a19538a05899b526d21f21cfcc20c9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982947"
---
# <span data-ttu-id="d71ab-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="d71ab-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="d71ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d71ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d71ab-103">Способ получения проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="d71ab-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="d71ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d71ab-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d71ab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d71ab-105">DESCRIPTION</span></span>
<span data-ttu-id="d71ab-106">Способ получения проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="d71ab-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="d71ab-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d71ab-107">EXAMPLES</span></span>

### <span data-ttu-id="d71ab-108">Пример 1. Получить</span><span class="sxs-lookup"><span data-stu-id="d71ab-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="d71ab-109">Способ получения проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="d71ab-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="d71ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d71ab-110">PARAMETERS</span></span>

### <span data-ttu-id="d71ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d71ab-111">-DefaultProfile</span></span>
<span data-ttu-id="d71ab-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d71ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d71ab-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d71ab-113">-Name</span></span>
<span data-ttu-id="d71ab-114">Имя проекта миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="d71ab-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d71ab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d71ab-115">-ResourceGroupName</span></span>
<span data-ttu-id="d71ab-116">Имя группы ресурсов Azure, в которую входит переносимый проект.</span><span class="sxs-lookup"><span data-stu-id="d71ab-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="d71ab-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d71ab-117">-SubscriptionId</span></span>
<span data-ttu-id="d71ab-118">Azure Subscription Id, в котором был создан проект переноса.</span><span class="sxs-lookup"><span data-stu-id="d71ab-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="d71ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d71ab-119">CommonParameters</span></span>
<span data-ttu-id="d71ab-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d71ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d71ab-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d71ab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d71ab-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d71ab-122">INPUTS</span></span>

## <span data-ttu-id="d71ab-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d71ab-123">OUTPUTS</span></span>

### <span data-ttu-id="d71ab-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="d71ab-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="d71ab-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d71ab-125">NOTES</span></span>

<span data-ttu-id="d71ab-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d71ab-126">ALIASES</span></span>

## <span data-ttu-id="d71ab-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d71ab-127">RELATED LINKS</span></span>

