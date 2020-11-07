---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 35f540d26464b7cdc4b08916f1397b71ee7cca18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899529"
---
# <span data-ttu-id="1180a-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="1180a-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="1180a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1180a-102">SYNOPSIS</span></span>
<span data-ttu-id="1180a-103">Создает нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="1180a-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="1180a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1180a-104">SYNTAX</span></span>

### <span data-ttu-id="1180a-105">NewEmailReceiver (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1180a-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1180a-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="1180a-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1180a-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="1180a-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1180a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1180a-108">DESCRIPTION</span></span>
<span data-ttu-id="1180a-109">Командлет **New-AzActionGroupReceiver** создает в памяти нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="1180a-109">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="1180a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1180a-110">EXAMPLES</span></span>

### <span data-ttu-id="1180a-111">Пример 1: создание нового получателя электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="1180a-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="1180a-112">Эта команда создает новый ресивер электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="1180a-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="1180a-113">Пример 2: создание нового приемника SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="1180a-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="1180a-114">Эта команда создает новый ресивер SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="1180a-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="1180a-115">Пример 3: создание в памяти нового приемника веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="1180a-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="1180a-116">Эта команда создает в памяти нового приемника веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="1180a-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="1180a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1180a-117">PARAMETERS</span></span>

### <span data-ttu-id="1180a-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="1180a-118">-CountryCode</span></span>
<span data-ttu-id="1180a-119">Указывает код страны для получателя SMS.</span><span class="sxs-lookup"><span data-stu-id="1180a-119">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="1180a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1180a-120">-DefaultProfile</span></span>
<span data-ttu-id="1180a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1180a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1180a-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="1180a-122">-EmailAddress</span></span>
<span data-ttu-id="1180a-123">Указывает адрес получателя электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1180a-123">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="1180a-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="1180a-124">-EmailReceiver</span></span>
<span data-ttu-id="1180a-125">Указывает, что нужно создать получателя электронной почты</span><span class="sxs-lookup"><span data-stu-id="1180a-125">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="1180a-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1180a-126">-Name</span></span>
<span data-ttu-id="1180a-127">Указывает имя получателя.</span><span class="sxs-lookup"><span data-stu-id="1180a-127">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="1180a-128">-Заданный</span><span class="sxs-lookup"><span data-stu-id="1180a-128">-PhoneNumber</span></span>
<span data-ttu-id="1180a-129">Задает номер телефона для ресивера SMS.</span><span class="sxs-lookup"><span data-stu-id="1180a-129">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="1180a-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="1180a-130">-ServiceUri</span></span>
<span data-ttu-id="1180a-131">Задает универсальный код ресурса (URI) для приемника веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="1180a-131">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="1180a-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="1180a-132">-SmsReceiver</span></span>
<span data-ttu-id="1180a-133">Указывает, что нужно создать ресивер SMS</span><span class="sxs-lookup"><span data-stu-id="1180a-133">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="1180a-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="1180a-134">-WebhookReceiver</span></span>
<span data-ttu-id="1180a-135">Указывает, что нужно создать приемник веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="1180a-135">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="1180a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1180a-136">CommonParameters</span></span>
<span data-ttu-id="1180a-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1180a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1180a-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1180a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1180a-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1180a-139">INPUTS</span></span>

### <span data-ttu-id="1180a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1180a-140">System.String</span></span>

### <span data-ttu-id="1180a-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1180a-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1180a-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1180a-142">OUTPUTS</span></span>

### <span data-ttu-id="1180a-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="1180a-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="1180a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="1180a-144">NOTES</span></span>

## <span data-ttu-id="1180a-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1180a-145">RELATED LINKS</span></span>

<span data-ttu-id="1180a-146">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="1180a-146">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
