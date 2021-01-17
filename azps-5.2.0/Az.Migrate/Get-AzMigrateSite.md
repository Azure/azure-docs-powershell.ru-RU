---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408956"
---
# <span data-ttu-id="c36f4-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="c36f4-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="c36f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c36f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c36f4-103">Способ получения сайта.</span><span class="sxs-lookup"><span data-stu-id="c36f4-103">Method to get a site.</span></span>

## <span data-ttu-id="c36f4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c36f4-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c36f4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c36f4-105">DESCRIPTION</span></span>
<span data-ttu-id="c36f4-106">Способ получения сайта.</span><span class="sxs-lookup"><span data-stu-id="c36f4-106">Method to get a site.</span></span>

## <span data-ttu-id="c36f4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c36f4-107">EXAMPLES</span></span>

### <span data-ttu-id="c36f4-108">Пример 1. Получить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c36f4-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="c36f4-109">Получить сайт по имени</span><span class="sxs-lookup"><span data-stu-id="c36f4-109">Get site by name</span></span>

## <span data-ttu-id="c36f4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c36f4-110">PARAMETERS</span></span>

### <span data-ttu-id="c36f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36f4-111">-DefaultProfile</span></span>
<span data-ttu-id="c36f4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c36f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c36f4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c36f4-113">-Name</span></span>
<span data-ttu-id="c36f4-114">Имя сайта.</span><span class="sxs-lookup"><span data-stu-id="c36f4-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36f4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c36f4-115">-ResourceGroupName</span></span>
<span data-ttu-id="c36f4-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c36f4-116">The name of the resource group.</span></span>
<span data-ttu-id="c36f4-117">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="c36f4-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c36f4-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c36f4-118">-SubscriptionId</span></span>
<span data-ttu-id="c36f4-119">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c36f4-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c36f4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36f4-120">CommonParameters</span></span>
<span data-ttu-id="c36f4-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36f4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36f4-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c36f4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36f4-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c36f4-123">INPUTS</span></span>

## <span data-ttu-id="c36f4-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c36f4-124">OUTPUTS</span></span>

### <span data-ttu-id="c36f4-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="c36f4-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="c36f4-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c36f4-126">NOTES</span></span>

<span data-ttu-id="c36f4-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c36f4-127">ALIASES</span></span>

## <span data-ttu-id="c36f4-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c36f4-128">RELATED LINKS</span></span>

