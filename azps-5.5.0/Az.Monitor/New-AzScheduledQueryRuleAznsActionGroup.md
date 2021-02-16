---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218993"
---
# <span data-ttu-id="668cf-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="668cf-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="668cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="668cf-102">SYNOPSIS</span></span>
<span data-ttu-id="668cf-103">Создание объекта типа "Группа действий Azns"</span><span class="sxs-lookup"><span data-stu-id="668cf-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="668cf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="668cf-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="668cf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="668cf-105">DESCRIPTION</span></span>
<span data-ttu-id="668cf-106">Создает объект типа Azns Action Group.</span><span class="sxs-lookup"><span data-stu-id="668cf-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="668cf-107">Этот объект передается команде, которая создает правило оповещения журнала.</span><span class="sxs-lookup"><span data-stu-id="668cf-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="668cf-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="668cf-108">EXAMPLES</span></span>

### <span data-ttu-id="668cf-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="668cf-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="668cf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="668cf-110">PARAMETERS</span></span>

### <span data-ttu-id="668cf-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="668cf-111">-ActionGroup</span></span>
<span data-ttu-id="668cf-112">Список групп действий, на которые нужно отправить уведомление</span><span class="sxs-lookup"><span data-stu-id="668cf-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="668cf-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="668cf-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="668cf-114">Настраиваемый веб-сайт</span><span class="sxs-lookup"><span data-stu-id="668cf-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="668cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668cf-115">-DefaultProfile</span></span>
<span data-ttu-id="668cf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="668cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="668cf-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="668cf-117">-EmailSubject</span></span>
<span data-ttu-id="668cf-118">Тема оповещения по электронной почте</span><span class="sxs-lookup"><span data-stu-id="668cf-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="668cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668cf-119">CommonParameters</span></span>
<span data-ttu-id="668cf-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="668cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668cf-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="668cf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668cf-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="668cf-122">INPUTS</span></span>

### <span data-ttu-id="668cf-123">Нет</span><span class="sxs-lookup"><span data-stu-id="668cf-123">None</span></span>

## <span data-ttu-id="668cf-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="668cf-124">OUTPUTS</span></span>

### <span data-ttu-id="668cf-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="668cf-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="668cf-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="668cf-126">NOTES</span></span>

## <span data-ttu-id="668cf-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="668cf-127">RELATED LINKS</span></span>
