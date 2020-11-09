---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247291"
---
# <span data-ttu-id="56d10-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="56d10-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="56d10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56d10-102">SYNOPSIS</span></span>
<span data-ttu-id="56d10-103">Создание объекта типа "Группа действий" Azns</span><span class="sxs-lookup"><span data-stu-id="56d10-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="56d10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56d10-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56d10-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56d10-105">DESCRIPTION</span></span>
<span data-ttu-id="56d10-106">Создает объект типа "Группа действий" Azns.</span><span class="sxs-lookup"><span data-stu-id="56d10-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="56d10-107">Этот объект передается команде, которая создает правило оповещения в журнале.</span><span class="sxs-lookup"><span data-stu-id="56d10-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="56d10-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56d10-108">EXAMPLES</span></span>

### <span data-ttu-id="56d10-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56d10-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="56d10-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56d10-110">PARAMETERS</span></span>

### <span data-ttu-id="56d10-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="56d10-111">-ActionGroup</span></span>
<span data-ttu-id="56d10-112">Список групп действий для отправки уведомления</span><span class="sxs-lookup"><span data-stu-id="56d10-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="56d10-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="56d10-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="56d10-114">Настраиваемые полезные данные веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="56d10-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="56d10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d10-115">-DefaultProfile</span></span>
<span data-ttu-id="56d10-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56d10-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56d10-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="56d10-117">-EmailSubject</span></span>
<span data-ttu-id="56d10-118">Тема сообщения электронной почты с уведомлением о предупреждении</span><span class="sxs-lookup"><span data-stu-id="56d10-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="56d10-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d10-119">CommonParameters</span></span>
<span data-ttu-id="56d10-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56d10-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d10-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56d10-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d10-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56d10-122">INPUTS</span></span>

### <span data-ttu-id="56d10-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="56d10-123">None</span></span>

## <span data-ttu-id="56d10-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56d10-124">OUTPUTS</span></span>

### <span data-ttu-id="56d10-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="56d10-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="56d10-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="56d10-126">NOTES</span></span>

## <span data-ttu-id="56d10-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56d10-127">RELATED LINKS</span></span>