---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519727"
---
# <span data-ttu-id="90247-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="90247-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="90247-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90247-102">SYNOPSIS</span></span>
<span data-ttu-id="90247-103">Возвращает ботслужба, заданную параметрами.</span><span class="sxs-lookup"><span data-stu-id="90247-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="90247-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="90247-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="90247-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90247-105">DESCRIPTION</span></span>
<span data-ttu-id="90247-106">Возвращает ботслужба, заданную параметрами.</span><span class="sxs-lookup"><span data-stu-id="90247-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="90247-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="90247-107">EXAMPLES</span></span>

### <span data-ttu-id="90247-108">Пример 1. Публикация botService в Azure</span><span class="sxs-lookup"><span data-stu-id="90247-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="90247-109">Публикация botService в Azure по коду</span><span class="sxs-lookup"><span data-stu-id="90247-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="90247-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90247-110">PARAMETERS</span></span>

### <span data-ttu-id="90247-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="90247-111">-CodeDir</span></span>
<span data-ttu-id="90247-112">Этот параметр определяет путь к ZIP-индексу.</span><span class="sxs-lookup"><span data-stu-id="90247-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="90247-113">-Name</span><span class="sxs-lookup"><span data-stu-id="90247-113">-Name</span></span>
<span data-ttu-id="90247-114">Этот параметр определяет имя бота.</span><span class="sxs-lookup"><span data-stu-id="90247-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="90247-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90247-115">-ResourceGroupName</span></span>
<span data-ttu-id="90247-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90247-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90247-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90247-117">-Confirm</span></span>
<span data-ttu-id="90247-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="90247-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90247-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90247-119">-WhatIf</span></span>
<span data-ttu-id="90247-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90247-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90247-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="90247-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90247-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90247-122">CommonParameters</span></span>
<span data-ttu-id="90247-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90247-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90247-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90247-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90247-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90247-125">INPUTS</span></span>

## <span data-ttu-id="90247-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="90247-126">OUTPUTS</span></span>

## <span data-ttu-id="90247-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="90247-127">NOTES</span></span>

<span data-ttu-id="90247-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="90247-128">ALIASES</span></span>

## <span data-ttu-id="90247-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90247-129">RELATED LINKS</span></span>

