---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398023"
---
# <span data-ttu-id="4035a-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="4035a-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="4035a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4035a-102">SYNOPSIS</span></span>
<span data-ttu-id="4035a-103">Способ получения проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="4035a-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="4035a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4035a-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4035a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4035a-105">DESCRIPTION</span></span>
<span data-ttu-id="4035a-106">Способ получения проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="4035a-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="4035a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4035a-107">EXAMPLES</span></span>

### <span data-ttu-id="4035a-108">Пример 1. Получить</span><span class="sxs-lookup"><span data-stu-id="4035a-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="4035a-109">Способ получения проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="4035a-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="4035a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4035a-110">PARAMETERS</span></span>

### <span data-ttu-id="4035a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4035a-111">-DefaultProfile</span></span>
<span data-ttu-id="4035a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4035a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4035a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4035a-113">-Name</span></span>
<span data-ttu-id="4035a-114">Имя проекта миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="4035a-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="4035a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4035a-115">-ResourceGroupName</span></span>
<span data-ttu-id="4035a-116">Имя группы ресурсов Azure, в которую входит переносимый проект.</span><span class="sxs-lookup"><span data-stu-id="4035a-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="4035a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4035a-117">-SubscriptionId</span></span>
<span data-ttu-id="4035a-118">Azure Subscription Id, в котором был создан проект переноса.</span><span class="sxs-lookup"><span data-stu-id="4035a-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="4035a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4035a-119">CommonParameters</span></span>
<span data-ttu-id="4035a-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4035a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4035a-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4035a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4035a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4035a-122">INPUTS</span></span>

## <span data-ttu-id="4035a-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4035a-123">OUTPUTS</span></span>

### <span data-ttu-id="4035a-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="4035a-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="4035a-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4035a-125">NOTES</span></span>

<span data-ttu-id="4035a-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4035a-126">ALIASES</span></span>

## <span data-ttu-id="4035a-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4035a-127">RELATED LINKS</span></span>

