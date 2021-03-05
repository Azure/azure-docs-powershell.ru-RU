---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 118fce3e75ee7ba66fa30e6e07cfce16e5dadcff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009304"
---
# <span data-ttu-id="62fa5-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="62fa5-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="62fa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="62fa5-103">Возвращает ботслужба, заданную параметрами.</span><span class="sxs-lookup"><span data-stu-id="62fa5-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="62fa5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62fa5-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="62fa5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62fa5-105">DESCRIPTION</span></span>
<span data-ttu-id="62fa5-106">Возвращает ботслужба, заданную параметрами.</span><span class="sxs-lookup"><span data-stu-id="62fa5-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="62fa5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62fa5-107">EXAMPLES</span></span>

### <span data-ttu-id="62fa5-108">Пример 1. Инициализация папки project</span><span class="sxs-lookup"><span data-stu-id="62fa5-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="62fa5-109">Инициализация подготовки ресурса к использованию и его состояние по умолчанию</span><span class="sxs-lookup"><span data-stu-id="62fa5-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="62fa5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62fa5-110">PARAMETERS</span></span>

### <span data-ttu-id="62fa5-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="62fa5-111">-CodeDir</span></span>
<span data-ttu-id="62fa5-112">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="62fa5-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="62fa5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fa5-113">-DefaultProfile</span></span>
<span data-ttu-id="62fa5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62fa5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62fa5-115">-Language</span><span class="sxs-lookup"><span data-stu-id="62fa5-115">-Language</span></span>


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

### <span data-ttu-id="62fa5-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="62fa5-116">-ProjFileName</span></span>


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

### <span data-ttu-id="62fa5-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62fa5-117">-SubscriptionId</span></span>
<span data-ttu-id="62fa5-118">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="62fa5-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="62fa5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fa5-119">CommonParameters</span></span>
<span data-ttu-id="62fa5-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62fa5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fa5-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62fa5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fa5-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62fa5-122">INPUTS</span></span>

## <span data-ttu-id="62fa5-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62fa5-123">OUTPUTS</span></span>

### <span data-ttu-id="62fa5-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="62fa5-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="62fa5-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62fa5-125">NOTES</span></span>

<span data-ttu-id="62fa5-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="62fa5-126">ALIASES</span></span>

## <span data-ttu-id="62fa5-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62fa5-127">RELATED LINKS</span></span>

