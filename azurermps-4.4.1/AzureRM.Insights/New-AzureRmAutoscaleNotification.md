---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: f6791d2cc962f0bb0db038ad8c5391425c09bfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568781"
---
# <span data-ttu-id="49660-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="49660-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="49660-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49660-102">SYNOPSIS</span></span>
<span data-ttu-id="49660-103">Создает уведомление об автомасштабировании электронной почты.</span><span class="sxs-lookup"><span data-stu-id="49660-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49660-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49660-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhooks] <WebhookNotification[]>] [[-CustomEmails] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49660-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49660-105">DESCRIPTION</span></span>
<span data-ttu-id="49660-106">Командлет **New-AzureRmAutoscaleNotification** создает уведомление по электронной почте для автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="49660-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="49660-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49660-107">EXAMPLES</span></span>

### <span data-ttu-id="49660-108">Пример 1: Создание уведомления об автомасштабировании электронной почты</span><span class="sxs-lookup"><span data-stu-id="49660-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="49660-109">Эта команда создает уведомление по электронной почте Autosacale для двух указанных адресов.</span><span class="sxs-lookup"><span data-stu-id="49660-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="49660-110">Пример 2: Создание уведомления об автомасштабировании электронной почты для администратора подписки</span><span class="sxs-lookup"><span data-stu-id="49660-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="49660-111">Эта команда создает уведомление по электронной почте Autosacale для администратора подписки.</span><span class="sxs-lookup"><span data-stu-id="49660-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="49660-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49660-112">PARAMETERS</span></span>

### <span data-ttu-id="49660-113">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="49660-113">-CustomEmails</span></span>
<span data-ttu-id="49660-114">Указывает список адресов электронной почты, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="49660-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="49660-115">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="49660-115">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="49660-116">Это означает, что эта операция отправляет администратору подписки уведомление по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="49660-116">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="49660-117">-SendEmailToSubscriptionCoAdministrators</span><span class="sxs-lookup"><span data-stu-id="49660-117">-SendEmailToSubscriptionCoAdministrators</span></span>
<span data-ttu-id="49660-118">Указывает на то, что эта операция отправляет уведомление по электронной почте для соадминистраторов подписки.</span><span class="sxs-lookup"><span data-stu-id="49660-118">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="49660-119">-Перехватчики</span><span class="sxs-lookup"><span data-stu-id="49660-119">-Webhooks</span></span>
<span data-ttu-id="49660-120">Задает разделенный запятыми список веб-перехватчиков автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="49660-120">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="49660-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49660-121">-DefaultProfile</span></span>
<span data-ttu-id="49660-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49660-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49660-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49660-123">CommonParameters</span></span>
<span data-ttu-id="49660-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49660-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49660-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49660-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49660-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49660-126">INPUTS</span></span>

## <span data-ttu-id="49660-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49660-127">OUTPUTS</span></span>

### <span data-ttu-id="49660-128">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="49660-128">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="49660-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="49660-129">NOTES</span></span>

## <span data-ttu-id="49660-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49660-130">RELATED LINKS</span></span>

[<span data-ttu-id="49660-131">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="49660-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


