---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219169"
---
# <span data-ttu-id="57ec6-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="57ec6-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="57ec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="57ec6-103">Способ запуска в качестве учетной записи.</span><span class="sxs-lookup"><span data-stu-id="57ec6-103">Method to get run as account.</span></span>

## <span data-ttu-id="57ec6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57ec6-104">SYNTAX</span></span>

### <span data-ttu-id="57ec6-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57ec6-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57ec6-106">Получить</span><span class="sxs-lookup"><span data-stu-id="57ec6-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="57ec6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57ec6-107">DESCRIPTION</span></span>
<span data-ttu-id="57ec6-108">Способ запуска в качестве учетной записи.</span><span class="sxs-lookup"><span data-stu-id="57ec6-108">Method to get run as account.</span></span>

## <span data-ttu-id="57ec6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57ec6-109">EXAMPLES</span></span>

### <span data-ttu-id="57ec6-110">Пример 1. Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57ec6-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="57ec6-111">List all run as accounts in a site.</span><span class="sxs-lookup"><span data-stu-id="57ec6-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="57ec6-112">Пример 2. Получить</span><span class="sxs-lookup"><span data-stu-id="57ec6-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="57ec6-113">Получить "Выполнить как учетную запись" по имени.</span><span class="sxs-lookup"><span data-stu-id="57ec6-113">Get Run as account by name.</span></span>

## <span data-ttu-id="57ec6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57ec6-114">PARAMETERS</span></span>

### <span data-ttu-id="57ec6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57ec6-115">-AccountName</span></span>
<span data-ttu-id="57ec6-116">Запустите как имя ARM учетной записи.</span><span class="sxs-lookup"><span data-stu-id="57ec6-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57ec6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ec6-117">-DefaultProfile</span></span>
<span data-ttu-id="57ec6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57ec6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57ec6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ec6-119">-ResourceGroupName</span></span>
<span data-ttu-id="57ec6-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57ec6-120">The name of the resource group.</span></span>
<span data-ttu-id="57ec6-121">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="57ec6-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="57ec6-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="57ec6-122">-SiteName</span></span>
<span data-ttu-id="57ec6-123">Имя сайта.</span><span class="sxs-lookup"><span data-stu-id="57ec6-123">Site name.</span></span>

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

### <span data-ttu-id="57ec6-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57ec6-124">-SubscriptionId</span></span>
<span data-ttu-id="57ec6-125">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="57ec6-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="57ec6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ec6-126">CommonParameters</span></span>
<span data-ttu-id="57ec6-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ec6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ec6-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57ec6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ec6-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57ec6-129">INPUTS</span></span>

## <span data-ttu-id="57ec6-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57ec6-130">OUTPUTS</span></span>

### <span data-ttu-id="57ec6-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="57ec6-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="57ec6-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57ec6-132">NOTES</span></span>

<span data-ttu-id="57ec6-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="57ec6-133">ALIASES</span></span>

## <span data-ttu-id="57ec6-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57ec6-134">RELATED LINKS</span></span>

