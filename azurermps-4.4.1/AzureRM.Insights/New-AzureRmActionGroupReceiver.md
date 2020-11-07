---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
ms.openlocfilehash: cd08e0106fe78ddae04ac4543210b310fe3aa579
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733373"
---
# <span data-ttu-id="d3f04-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="d3f04-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="d3f04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3f04-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f04-103">Создает нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="d3f04-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3f04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3f04-104">SYNTAX</span></span>

### <span data-ttu-id="d3f04-105">NewEmailReceiver (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3f04-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f04-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="d3f04-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f04-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="d3f04-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f04-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3f04-108">DESCRIPTION</span></span>
<span data-ttu-id="d3f04-109">Командлет **New-AzureRmActionGroupReceiver** создает в памяти нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="d3f04-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="d3f04-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3f04-110">EXAMPLES</span></span>

### <span data-ttu-id="d3f04-111">Пример 1: создание нового получателя электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="d3f04-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="d3f04-112">Эта команда создает новый ресивер электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="d3f04-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="d3f04-113">Пример 2: создание нового приемника SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="d3f04-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="d3f04-114">Эта команда создает новый ресивер SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="d3f04-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="d3f04-115">Пример 3: создание в памяти нового приемника веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="d3f04-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="d3f04-116">Эта команда создает в памяти нового приемника веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="d3f04-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="d3f04-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3f04-117">PARAMETERS</span></span>

### <span data-ttu-id="d3f04-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3f04-118">-Name</span></span>
<span data-ttu-id="d3f04-119">Указывает имя получателя.</span><span class="sxs-lookup"><span data-stu-id="d3f04-119">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f04-120">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="d3f04-120">-EmailAddress</span></span>
<span data-ttu-id="d3f04-121">Указывает адрес получателя электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d3f04-121">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f04-122">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="d3f04-122">-CountryCode</span></span>
<span data-ttu-id="d3f04-123">Указывает код страны для получателя SMS.</span><span class="sxs-lookup"><span data-stu-id="d3f04-123">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f04-124">-Заданный</span><span class="sxs-lookup"><span data-stu-id="d3f04-124">-PhoneNumber</span></span>
<span data-ttu-id="d3f04-125">Задает номер телефона для ресивера SMS.</span><span class="sxs-lookup"><span data-stu-id="d3f04-125">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f04-126">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="d3f04-126">-ServiceUri</span></span>
<span data-ttu-id="d3f04-127">Задает универсальный код ресурса (URI) для приемника веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="d3f04-127">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f04-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f04-128">-DefaultProfile</span></span>
<span data-ttu-id="d3f04-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f04-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3f04-130">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="d3f04-130">-EmailReceiver</span></span>
<span data-ttu-id="d3f04-131">Указывает, что нужно создать получателя электронной почты</span><span class="sxs-lookup"><span data-stu-id="d3f04-131">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f04-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="d3f04-132">-SmsReceiver</span></span>
<span data-ttu-id="d3f04-133">Указывает, что нужно создать ресивер SMS</span><span class="sxs-lookup"><span data-stu-id="d3f04-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f04-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="d3f04-134">-WebhookReceiver</span></span>
<span data-ttu-id="d3f04-135">Указывает, что нужно создать приемник веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="d3f04-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f04-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f04-136">CommonParameters</span></span>
<span data-ttu-id="d3f04-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3f04-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f04-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f04-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f04-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3f04-139">INPUTS</span></span>

## <span data-ttu-id="d3f04-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3f04-140">OUTPUTS</span></span>

### <span data-ttu-id="d3f04-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="d3f04-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="d3f04-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3f04-142">NOTES</span></span>

## <span data-ttu-id="d3f04-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3f04-143">RELATED LINKS</span></span>

<span data-ttu-id="d3f04-144">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="d3f04-144">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
