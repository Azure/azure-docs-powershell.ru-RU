---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: 79ef8a92997790f547847e05eae6ca101016bc42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960872"
---
# <span data-ttu-id="d5df3-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="d5df3-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="d5df3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5df3-102">SYNOPSIS</span></span>
<span data-ttu-id="d5df3-103">Возвращает ботслужба, заданную параметрами.</span><span class="sxs-lookup"><span data-stu-id="d5df3-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="d5df3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5df3-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d5df3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5df3-105">DESCRIPTION</span></span>
<span data-ttu-id="d5df3-106">Возвращает ботслужба, заданную параметрами.</span><span class="sxs-lookup"><span data-stu-id="d5df3-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="d5df3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5df3-107">EXAMPLES</span></span>

### <span data-ttu-id="d5df3-108">Пример 1. Загрузка папки приложения BotService</span><span class="sxs-lookup"><span data-stu-id="d5df3-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="d5df3-109">Загрузка папки приложения BotService</span><span class="sxs-lookup"><span data-stu-id="d5df3-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="d5df3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5df3-110">PARAMETERS</span></span>

### <span data-ttu-id="d5df3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5df3-111">-DefaultProfile</span></span>
<span data-ttu-id="d5df3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5df3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5df3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d5df3-113">-Name</span></span>
<span data-ttu-id="d5df3-114">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="d5df3-114">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5df3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5df3-115">-ResourceGroupName</span></span>
<span data-ttu-id="d5df3-116">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="d5df3-116">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5df3-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="d5df3-117">-SavePath</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5df3-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5df3-118">-SubscriptionId</span></span>
<span data-ttu-id="d5df3-119">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d5df3-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d5df3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5df3-120">CommonParameters</span></span>
<span data-ttu-id="d5df3-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5df3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5df3-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5df3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5df3-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5df3-123">INPUTS</span></span>

## <span data-ttu-id="d5df3-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5df3-124">OUTPUTS</span></span>

### <span data-ttu-id="d5df3-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="d5df3-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="d5df3-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5df3-126">NOTES</span></span>

<span data-ttu-id="d5df3-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d5df3-127">ALIASES</span></span>

## <span data-ttu-id="d5df3-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5df3-128">RELATED LINKS</span></span>

