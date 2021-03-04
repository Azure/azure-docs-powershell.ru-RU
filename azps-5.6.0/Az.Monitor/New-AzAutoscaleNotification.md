---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: c537908d2249ca5ec8a33adffa4e655b0a9ec6e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982664"
---
# <span data-ttu-id="6e9a0-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="6e9a0-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="6e9a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6e9a0-103">Создает уведомление по электронной почте об автомасштабе.</span><span class="sxs-lookup"><span data-stu-id="6e9a0-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="6e9a0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6e9a0-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e9a0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e9a0-105">DESCRIPTION</span></span>
<span data-ttu-id="6e9a0-106">Для **автоматической** шкалы создается уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="6e9a0-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="6e9a0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6e9a0-107">EXAMPLES</span></span>

### <span data-ttu-id="6e9a0-108">Пример 1. Создание уведомления по электронной почте с авто шкалой</span><span class="sxs-lookup"><span data-stu-id="6e9a0-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="6e9a0-109">Эта команда создает уведомление по электронной почте с автоматическим уст. для двух указанных адресов.</span><span class="sxs-lookup"><span data-stu-id="6e9a0-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="6e9a0-110">Пример 2. Создание уведомления по электронной почте с автомасштабом для администратора подписки</span><span class="sxs-lookup"><span data-stu-id="6e9a0-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="6e9a0-111">Эта команда создает уведомление по электронной почте для администратора подписки.</span><span class="sxs-lookup"><span data-stu-id="6e9a0-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="6e9a0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e9a0-112">PARAMETERS</span></span>

### <span data-ttu-id="6e9a0-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="6e9a0-113">-CustomEmail</span></span>
<span data-ttu-id="6e9a0-114">Определяет список адресов электронной почты, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="6e9a0-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e9a0-115">-DefaultProfile</span></span>
<span data-ttu-id="6e9a0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6e9a0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e9a0-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="6e9a0-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="6e9a0-118">Указывает на то, что в ходе этой операции администратору подписки будет отправлено уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="6e9a0-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a0-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="6e9a0-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="6e9a0-120">Указывает на то, что в ходе этой операции администраторам подписки будет отправлено уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="6e9a0-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a0-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="6e9a0-121">-Webhook</span></span>
<span data-ttu-id="6e9a0-122">Определяет список веб-сайтов автомасштаби, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="6e9a0-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e9a0-123">CommonParameters</span></span>
<span data-ttu-id="6e9a0-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e9a0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e9a0-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e9a0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e9a0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e9a0-126">INPUTS</span></span>

### <span data-ttu-id="6e9a0-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span><span class="sxs-lookup"><span data-stu-id="6e9a0-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="6e9a0-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6e9a0-128">System.String[]</span></span>

### <span data-ttu-id="6e9a0-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6e9a0-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6e9a0-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e9a0-130">OUTPUTS</span></span>

### <span data-ttu-id="6e9a0-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="6e9a0-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="6e9a0-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6e9a0-132">NOTES</span></span>

## <span data-ttu-id="6e9a0-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e9a0-133">RELATED LINKS</span></span>

[<span data-ttu-id="6e9a0-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="6e9a0-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


