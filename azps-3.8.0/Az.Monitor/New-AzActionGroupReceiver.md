---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072986"
---
# <span data-ttu-id="a2659-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="a2659-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2659-102">SYNOPSIS</span></span>
<span data-ttu-id="a2659-103">Создает нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="a2659-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="a2659-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2659-104">SYNTAX</span></span>

### <span data-ttu-id="a2659-105">NewEmailReceiver (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2659-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2659-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2659-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2659-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2659-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2659-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2659-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2659-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2659-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2659-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2659-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2659-115">DESCRIPTION</span></span>
<span data-ttu-id="a2659-116">Командлет **New-AzActionGroupReceiver** создает в памяти нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="a2659-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="a2659-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2659-117">EXAMPLES</span></span>

### <span data-ttu-id="a2659-118">Пример 1: создание нового получателя электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="a2659-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="a2659-119">Эта команда создает новый ресивер электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="a2659-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="a2659-120">Пример 2: создание нового приемника SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="a2659-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="a2659-121">Эта команда создает новый ресивер SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="a2659-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="a2659-122">Пример 3: создание в памяти нового приемника веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="a2659-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="a2659-123">Эта команда создает в памяти нового приемника веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="a2659-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="a2659-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2659-124">PARAMETERS</span></span>

### <span data-ttu-id="a2659-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="a2659-126">Создание ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-126">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="a2659-127">-AutomationAccountId</span></span>
<span data-ttu-id="a2659-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="a2659-128">the AutomationAccountId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="a2659-130">Создание AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-130">Create a AutomationRunbookReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="a2659-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="a2659-132">URI, на который должны отправляться веб-перехватчики</span><span class="sxs-lookup"><span data-stu-id="a2659-132">the URI where webhooks should be sent</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a2659-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="a2659-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a2659-134">the AzureAppPushEmailAddress</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="a2659-136">Создание AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-136">Create a AzureAppPushReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="a2659-138">Создание ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-138">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="a2659-139">-CallbackUrl</span></span>
<span data-ttu-id="a2659-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="a2659-140">the CallbackUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="a2659-141">-ConnectionId</span></span>
<span data-ttu-id="a2659-142">Идентификатор подключения ITSM для этого получателя.</span><span class="sxs-lookup"><span data-stu-id="a2659-142">the itsm connection id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="a2659-143">-CountryCode</span></span>
<span data-ttu-id="a2659-144">Указывает код страны для получателя SMS.</span><span class="sxs-lookup"><span data-stu-id="a2659-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="a2659-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2659-145">-DefaultProfile</span></span>
<span data-ttu-id="a2659-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a2659-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2659-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a2659-147">-EmailAddress</span></span>
<span data-ttu-id="a2659-148">Указывает адрес получателя электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a2659-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="a2659-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-149">-EmailReceiver</span></span>
<span data-ttu-id="a2659-150">Указывает, что нужно создать получателя электронной почты</span><span class="sxs-lookup"><span data-stu-id="a2659-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="a2659-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="a2659-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="a2659-152">ИД приложения функции</span><span class="sxs-lookup"><span data-stu-id="a2659-152">the function app resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="a2659-153">-FunctionName</span></span>
<span data-ttu-id="a2659-154">"functionName"</span><span class="sxs-lookup"><span data-stu-id="a2659-154">the functionName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="a2659-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="a2659-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="a2659-156">the httpTriggerUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="a2659-157">-IdentifierUri</span></span>
<span data-ttu-id="a2659-158">универсальный код ресурса (URI) идентификатора для проверки подлинности AAD</span><span class="sxs-lookup"><span data-stu-id="a2659-158">the Identifier uri for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="a2659-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="a2659-160">Указывает, является ли этот экземпляр глобальным модулем Runbook</span><span class="sxs-lookup"><span data-stu-id="a2659-160">indicating whether this instance is global runbook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-161">-ItsmReceiver</span></span>
<span data-ttu-id="a2659-162">Создание ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-162">Create a ItsmReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewItsmReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-163">-LogicAppReceiver</span></span>
<span data-ttu-id="a2659-164">Создание LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-164">Create a LogicAppReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-165">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2659-165">-Name</span></span>
<span data-ttu-id="a2659-166">Указывает имя получателя.</span><span class="sxs-lookup"><span data-stu-id="a2659-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="a2659-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a2659-167">-ObjectId</span></span>
<span data-ttu-id="a2659-168">Идентификатор объекта приложения веб-перехватчика для проверки подлинности AAD</span><span class="sxs-lookup"><span data-stu-id="a2659-168">the webhook app object Id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-169">-Заданный</span><span class="sxs-lookup"><span data-stu-id="a2659-169">-PhoneNumber</span></span>
<span data-ttu-id="a2659-170">Задает номер телефона для ресивера SMS.</span><span class="sxs-lookup"><span data-stu-id="a2659-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="a2659-171">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="a2659-171">-Region</span></span>
<span data-ttu-id="a2659-172">itsmская область этого получателя.</span><span class="sxs-lookup"><span data-stu-id="a2659-172">the itsm Region of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2659-173">-ResourceId</span></span>
<span data-ttu-id="a2659-174">ResourceId (ИД ресурса)</span><span class="sxs-lookup"><span data-stu-id="a2659-174">the ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="a2659-175">-RoleId</span></span>
<span data-ttu-id="a2659-176">Идентификатор роли ARM получателя.</span><span class="sxs-lookup"><span data-stu-id="a2659-176">The arm role id of the receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="a2659-177">-RunbookName</span></span>
<span data-ttu-id="a2659-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="a2659-178">the RunbookName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="a2659-179">-ServiceUri</span></span>
<span data-ttu-id="a2659-180">Задает универсальный код ресурса (URI) для приемника веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="a2659-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="a2659-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-181">-SmsReceiver</span></span>
<span data-ttu-id="a2659-182">Указывает, что нужно создать ресивер SMS</span><span class="sxs-lookup"><span data-stu-id="a2659-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="a2659-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a2659-183">-TenantId</span></span>
<span data-ttu-id="a2659-184">Идентификатор клиента для проверки подлинности AAD</span><span class="sxs-lookup"><span data-stu-id="a2659-184">the tenant id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2659-185">-TicketConfiguration</span></span>
<span data-ttu-id="a2659-186">ITSM TicketConfiguration этого получателя.</span><span class="sxs-lookup"><span data-stu-id="a2659-186">the itsm TicketConfiguration of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="a2659-187">-UseAadAuth</span></span>
<span data-ttu-id="a2659-188">флаг для использования добавления проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="a2659-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="a2659-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="a2659-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="a2659-190">Пометка о том, следует ли использовать общую схему оповещения.</span><span class="sxs-lookup"><span data-stu-id="a2659-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="a2659-191">Это значение будет использоваться в neglectedfor SMS, приложении Azure Push, ITSM и голосовой recievers.</span><span class="sxs-lookup"><span data-stu-id="a2659-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="a2659-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="a2659-192">-VoiceCountryCode</span></span>
<span data-ttu-id="a2659-193">Код страны для голосового приемника</span><span class="sxs-lookup"><span data-stu-id="a2659-193">The country code of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="a2659-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="a2659-195">Номер телефона голосового приемника</span><span class="sxs-lookup"><span data-stu-id="a2659-195">The phone number of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-196">-VoiceReceiver</span></span>
<span data-ttu-id="a2659-197">Создание голосового приемника</span><span class="sxs-lookup"><span data-stu-id="a2659-197">Create a voice receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="a2659-198">-WebhookReceiver</span></span>
<span data-ttu-id="a2659-199">Указывает, что нужно создать приемник веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="a2659-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="a2659-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="a2659-200">-WebhookResourceId</span></span>
<span data-ttu-id="a2659-201">WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="a2659-201">the WebhookResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a2659-202">-WorkspaceId</span></span>
<span data-ttu-id="a2659-203">идентификатор рабочей области ITSM для этого получателя.</span><span class="sxs-lookup"><span data-stu-id="a2659-203">the itsm workspace id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2659-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2659-204">CommonParameters</span></span>
<span data-ttu-id="a2659-205">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2659-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2659-206">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2659-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2659-207">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2659-207">INPUTS</span></span>

### <span data-ttu-id="a2659-208">System. String</span><span class="sxs-lookup"><span data-stu-id="a2659-208">System.String</span></span>

### <span data-ttu-id="a2659-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a2659-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a2659-210">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2659-210">OUTPUTS</span></span>

### <span data-ttu-id="a2659-211">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="a2659-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="a2659-212">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2659-212">NOTES</span></span>

## <span data-ttu-id="a2659-213">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2659-213">RELATED LINKS</span></span>

<span data-ttu-id="a2659-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="a2659-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
