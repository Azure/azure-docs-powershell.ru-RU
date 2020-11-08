---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250070"
---
# <span data-ttu-id="7ba1e-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7ba1e-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="7ba1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ba1e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba1e-103">Метод для получения проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="7ba1e-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="7ba1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ba1e-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7ba1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ba1e-105">DESCRIPTION</span></span>
<span data-ttu-id="7ba1e-106">Метод для получения проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="7ba1e-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="7ba1e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ba1e-107">EXAMPLES</span></span>

### <span data-ttu-id="7ba1e-108">Пример 1: Get</span><span class="sxs-lookup"><span data-stu-id="7ba1e-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="7ba1e-109">Метод для получения проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="7ba1e-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="7ba1e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ba1e-110">PARAMETERS</span></span>

### <span data-ttu-id="7ba1e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba1e-111">-DefaultProfile</span></span>
<span data-ttu-id="7ba1e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba1e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba1e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7ba1e-113">-Name</span></span>
<span data-ttu-id="7ba1e-114">Имя проекта для миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba1e-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="7ba1e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba1e-115">-ResourceGroupName</span></span>
<span data-ttu-id="7ba1e-116">Имя группы ресурсов Azure, в состав которой входит переносимый проект.</span><span class="sxs-lookup"><span data-stu-id="7ba1e-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="7ba1e-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ba1e-117">-SubscriptionId</span></span>
<span data-ttu-id="7ba1e-118">Идентификатор подписки Azure, в которой был создан проект миграции.</span><span class="sxs-lookup"><span data-stu-id="7ba1e-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="7ba1e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba1e-119">CommonParameters</span></span>
<span data-ttu-id="7ba1e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ba1e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba1e-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ba1e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba1e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ba1e-122">INPUTS</span></span>

## <span data-ttu-id="7ba1e-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ba1e-123">OUTPUTS</span></span>

### <span data-ttu-id="7ba1e-124">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180901Preview. IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7ba1e-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="7ba1e-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ba1e-125">NOTES</span></span>

<span data-ttu-id="7ba1e-126">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="7ba1e-126">ALIASES</span></span>

## <span data-ttu-id="7ba1e-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ba1e-127">RELATED LINKS</span></span>

