---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 43eda2eb27003a079dae0442d7ab8e9f636cbef4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902658"
---
# <span data-ttu-id="6dcdd-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="6dcdd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6dcdd-102">SYNOPSIS</span></span>
<span data-ttu-id="6dcdd-103">Создает нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="6dcdd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6dcdd-104">SYNTAX</span></span>

### <span data-ttu-id="6dcdd-105">NewEmailReceiver (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6dcdd-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dcdd-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dcdd-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dcdd-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dcdd-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dcdd-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dcdd-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dcdd-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dcdd-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dcdd-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dcdd-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dcdd-115">DESCRIPTION</span></span>
<span data-ttu-id="6dcdd-116">Командлет **New-AzActionGroupReceiver** создает в памяти нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="6dcdd-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6dcdd-117">EXAMPLES</span></span>

### <span data-ttu-id="6dcdd-118">Пример 1: создание нового получателя электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="6dcdd-119">Эта команда создает новый ресивер электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="6dcdd-120">Пример 2: создание нового приемника SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="6dcdd-121">Эта команда создает новый ресивер SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="6dcdd-122">Пример 3: создание в памяти нового приемника веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="6dcdd-123">Эта команда создает в памяти нового приемника веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="6dcdd-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6dcdd-124">PARAMETERS</span></span>

### <span data-ttu-id="6dcdd-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="6dcdd-126">Создание ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="6dcdd-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-127">-AutomationAccountId</span></span>
<span data-ttu-id="6dcdd-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="6dcdd-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="6dcdd-130">Создание AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="6dcdd-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="6dcdd-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="6dcdd-132">URI, на который должны отправляться веб-перехватчики</span><span class="sxs-lookup"><span data-stu-id="6dcdd-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="6dcdd-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6dcdd-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="6dcdd-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6dcdd-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="6dcdd-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="6dcdd-136">Создание AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="6dcdd-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="6dcdd-138">Создание ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="6dcdd-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="6dcdd-139">-CallbackUrl</span></span>
<span data-ttu-id="6dcdd-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="6dcdd-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="6dcdd-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-141">-ConnectionId</span></span>
<span data-ttu-id="6dcdd-142">Идентификатор подключения ITSM для этого получателя.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="6dcdd-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="6dcdd-143">-CountryCode</span></span>
<span data-ttu-id="6dcdd-144">Указывает код страны для получателя SMS.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="6dcdd-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dcdd-145">-DefaultProfile</span></span>
<span data-ttu-id="6dcdd-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6dcdd-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dcdd-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="6dcdd-147">-EmailAddress</span></span>
<span data-ttu-id="6dcdd-148">Указывает адрес получателя электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="6dcdd-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-149">-EmailReceiver</span></span>
<span data-ttu-id="6dcdd-150">Указывает, что нужно создать получателя электронной почты</span><span class="sxs-lookup"><span data-stu-id="6dcdd-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="6dcdd-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="6dcdd-152">ИД приложения функции</span><span class="sxs-lookup"><span data-stu-id="6dcdd-152">the function app resourceId</span></span>

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

### <span data-ttu-id="6dcdd-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="6dcdd-153">-FunctionName</span></span>
<span data-ttu-id="6dcdd-154">"functionName"</span><span class="sxs-lookup"><span data-stu-id="6dcdd-154">the functionName</span></span>

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

### <span data-ttu-id="6dcdd-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="6dcdd-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="6dcdd-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="6dcdd-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="6dcdd-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="6dcdd-157">-IdentifierUri</span></span>
<span data-ttu-id="6dcdd-158">универсальный код ресурса (URI) идентификатора для проверки подлинности AAD</span><span class="sxs-lookup"><span data-stu-id="6dcdd-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="6dcdd-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="6dcdd-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="6dcdd-160">Указывает, является ли этот экземпляр глобальным модулем Runbook</span><span class="sxs-lookup"><span data-stu-id="6dcdd-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="6dcdd-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-161">-ItsmReceiver</span></span>
<span data-ttu-id="6dcdd-162">Создание ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="6dcdd-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-163">-LogicAppReceiver</span></span>
<span data-ttu-id="6dcdd-164">Создание LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="6dcdd-165">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6dcdd-165">-Name</span></span>
<span data-ttu-id="6dcdd-166">Указывает имя получателя.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="6dcdd-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-167">-ObjectId</span></span>
<span data-ttu-id="6dcdd-168">Идентификатор объекта приложения веб-перехватчика для проверки подлинности AAD</span><span class="sxs-lookup"><span data-stu-id="6dcdd-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="6dcdd-169">-Заданный</span><span class="sxs-lookup"><span data-stu-id="6dcdd-169">-PhoneNumber</span></span>
<span data-ttu-id="6dcdd-170">Задает номер телефона для ресивера SMS.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="6dcdd-171">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="6dcdd-171">-Region</span></span>
<span data-ttu-id="6dcdd-172">itsmская область этого получателя.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="6dcdd-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-173">-ResourceId</span></span>
<span data-ttu-id="6dcdd-174">ResourceId (ИД ресурса)</span><span class="sxs-lookup"><span data-stu-id="6dcdd-174">the ResourceId</span></span>

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

### <span data-ttu-id="6dcdd-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-175">-RoleId</span></span>
<span data-ttu-id="6dcdd-176">Идентификатор роли ARM получателя.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="6dcdd-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="6dcdd-177">-RunbookName</span></span>
<span data-ttu-id="6dcdd-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="6dcdd-178">the RunbookName</span></span>

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

### <span data-ttu-id="6dcdd-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="6dcdd-179">-ServiceUri</span></span>
<span data-ttu-id="6dcdd-180">Задает универсальный код ресурса (URI) для приемника веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="6dcdd-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-181">-SmsReceiver</span></span>
<span data-ttu-id="6dcdd-182">Указывает, что нужно создать ресивер SMS</span><span class="sxs-lookup"><span data-stu-id="6dcdd-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="6dcdd-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-183">-TenantId</span></span>
<span data-ttu-id="6dcdd-184">Идентификатор клиента для проверки подлинности AAD</span><span class="sxs-lookup"><span data-stu-id="6dcdd-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="6dcdd-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dcdd-185">-TicketConfiguration</span></span>
<span data-ttu-id="6dcdd-186">ITSM TicketConfiguration этого получателя.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="6dcdd-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="6dcdd-187">-UseAadAuth</span></span>
<span data-ttu-id="6dcdd-188">флаг для использования добавления проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="6dcdd-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="6dcdd-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="6dcdd-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="6dcdd-190">Пометка о том, следует ли использовать общую схему оповещения.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="6dcdd-191">Это значение будет использоваться в neglectedfor SMS, приложении Azure Push, ITSM и голосовой recievers.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="6dcdd-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="6dcdd-192">-VoiceCountryCode</span></span>
<span data-ttu-id="6dcdd-193">Код страны для голосового приемника</span><span class="sxs-lookup"><span data-stu-id="6dcdd-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="6dcdd-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6dcdd-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="6dcdd-195">Номер телефона голосового приемника</span><span class="sxs-lookup"><span data-stu-id="6dcdd-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="6dcdd-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-196">-VoiceReceiver</span></span>
<span data-ttu-id="6dcdd-197">Создание голосового приемника</span><span class="sxs-lookup"><span data-stu-id="6dcdd-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="6dcdd-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="6dcdd-198">-WebhookReceiver</span></span>
<span data-ttu-id="6dcdd-199">Указывает, что нужно создать приемник веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="6dcdd-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="6dcdd-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-200">-WebhookResourceId</span></span>
<span data-ttu-id="6dcdd-201">WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="6dcdd-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="6dcdd-202">-WorkspaceId</span></span>
<span data-ttu-id="6dcdd-203">идентификатор рабочей области ITSM для этого получателя.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="6dcdd-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dcdd-204">CommonParameters</span></span>
<span data-ttu-id="6dcdd-205">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6dcdd-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dcdd-206">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dcdd-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dcdd-207">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6dcdd-207">INPUTS</span></span>

### <span data-ttu-id="6dcdd-208">System. String</span><span class="sxs-lookup"><span data-stu-id="6dcdd-208">System.String</span></span>

### <span data-ttu-id="6dcdd-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6dcdd-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6dcdd-210">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dcdd-210">OUTPUTS</span></span>

### <span data-ttu-id="6dcdd-211">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="6dcdd-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="6dcdd-212">Пуск</span><span class="sxs-lookup"><span data-stu-id="6dcdd-212">NOTES</span></span>

## <span data-ttu-id="6dcdd-213">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dcdd-213">RELATED LINKS</span></span>

<span data-ttu-id="6dcdd-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="6dcdd-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
