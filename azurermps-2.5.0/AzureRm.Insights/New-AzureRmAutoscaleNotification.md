---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
ms.openlocfilehash: 51a5c01c28471cf85617b8ab629c2f79b366d555
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915289"
---
# <span data-ttu-id="fe98c-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="fe98c-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="fe98c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe98c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe98c-103">Создает уведомление об автомасштабировании электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fe98c-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe98c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe98c-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe98c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe98c-105">DESCRIPTION</span></span>
<span data-ttu-id="fe98c-106">Командлет **New-AzureRmAutoscaleNotification** создает уведомление по электронной почте для автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="fe98c-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="fe98c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe98c-107">EXAMPLES</span></span>

### <span data-ttu-id="fe98c-108">Пример 1: Создание уведомления об автомасштабировании электронной почты</span><span class="sxs-lookup"><span data-stu-id="fe98c-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="fe98c-109">Эта команда создает уведомление по электронной почте Autosacale для двух указанных адресов.</span><span class="sxs-lookup"><span data-stu-id="fe98c-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="fe98c-110">Пример 2: Создание уведомления об автомасштабировании электронной почты для администратора подписки</span><span class="sxs-lookup"><span data-stu-id="fe98c-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="fe98c-111">Эта команда создает уведомление по электронной почте Autosacale для администратора подписки.</span><span class="sxs-lookup"><span data-stu-id="fe98c-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="fe98c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe98c-112">PARAMETERS</span></span>

### <span data-ttu-id="fe98c-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="fe98c-113">-CustomEmail</span></span>
<span data-ttu-id="fe98c-114">Указывает список адресов электронной почты, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="fe98c-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="fe98c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe98c-115">-DefaultProfile</span></span>
<span data-ttu-id="fe98c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fe98c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe98c-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="fe98c-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="fe98c-118">Это означает, что эта операция отправляет администратору подписки уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="fe98c-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="fe98c-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="fe98c-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="fe98c-120">Указывает на то, что эта операция отправляет уведомление по электронной почте для соадминистраторов подписки.</span><span class="sxs-lookup"><span data-stu-id="fe98c-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="fe98c-121">-Перехватчик</span><span class="sxs-lookup"><span data-stu-id="fe98c-121">-Webhook</span></span>
<span data-ttu-id="fe98c-122">Задает разделенный запятыми список веб-перехватчиков автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="fe98c-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="fe98c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe98c-123">CommonParameters</span></span>
<span data-ttu-id="fe98c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe98c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe98c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe98c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe98c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe98c-126">INPUTS</span></span>

### <span data-ttu-id="fe98c-127">Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="fe98c-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="fe98c-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="fe98c-128">System.String[]</span></span>

### <span data-ttu-id="fe98c-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fe98c-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fe98c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe98c-130">OUTPUTS</span></span>

### <span data-ttu-id="fe98c-131">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="fe98c-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="fe98c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe98c-132">NOTES</span></span>

## <span data-ttu-id="fe98c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe98c-133">RELATED LINKS</span></span>

[<span data-ttu-id="fe98c-134">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="fe98c-134">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


