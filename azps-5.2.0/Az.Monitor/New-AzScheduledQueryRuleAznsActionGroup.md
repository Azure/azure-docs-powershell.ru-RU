---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417559"
---
# <span data-ttu-id="4c876-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="4c876-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="4c876-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c876-102">SYNOPSIS</span></span>
<span data-ttu-id="4c876-103">Создание объекта типа "Группа действий Azns"</span><span class="sxs-lookup"><span data-stu-id="4c876-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="4c876-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4c876-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c876-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c876-105">DESCRIPTION</span></span>
<span data-ttu-id="4c876-106">Создает объект типа Azns Action Group.</span><span class="sxs-lookup"><span data-stu-id="4c876-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="4c876-107">Этот объект передается команде, которая создает правило оповещения журнала.</span><span class="sxs-lookup"><span data-stu-id="4c876-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="4c876-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4c876-108">EXAMPLES</span></span>

### <span data-ttu-id="4c876-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4c876-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="4c876-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c876-110">PARAMETERS</span></span>

### <span data-ttu-id="4c876-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="4c876-111">-ActionGroup</span></span>
<span data-ttu-id="4c876-112">Список групп действий, на которые нужно отправить уведомление</span><span class="sxs-lookup"><span data-stu-id="4c876-112">The list of action groups to send notification to</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c876-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="4c876-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="4c876-114">Настраиваемый веб-сайт</span><span class="sxs-lookup"><span data-stu-id="4c876-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="4c876-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c876-115">-DefaultProfile</span></span>
<span data-ttu-id="4c876-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c876-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c876-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="4c876-117">-EmailSubject</span></span>
<span data-ttu-id="4c876-118">Тема оповещения по электронной почте</span><span class="sxs-lookup"><span data-stu-id="4c876-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="4c876-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c876-119">CommonParameters</span></span>
<span data-ttu-id="4c876-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c876-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c876-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c876-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c876-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c876-122">INPUTS</span></span>

### <span data-ttu-id="4c876-123">Нет</span><span class="sxs-lookup"><span data-stu-id="4c876-123">None</span></span>

## <span data-ttu-id="4c876-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c876-124">OUTPUTS</span></span>

### <span data-ttu-id="4c876-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="4c876-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="4c876-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4c876-126">NOTES</span></span>

## <span data-ttu-id="4c876-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c876-127">RELATED LINKS</span></span>
