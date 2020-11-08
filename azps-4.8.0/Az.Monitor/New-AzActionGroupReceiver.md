---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236280"
---
# <span data-ttu-id="26811-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="26811-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26811-102">SYNOPSIS</span></span>
<span data-ttu-id="26811-103">Создает нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="26811-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="26811-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26811-104">SYNTAX</span></span>

### <span data-ttu-id="26811-105">NewEmailReceiver (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26811-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26811-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26811-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26811-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26811-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26811-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26811-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26811-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26811-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26811-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26811-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26811-115">DESCRIPTION</span></span>
<span data-ttu-id="26811-116">Командлет **New-AzActionGroupReceiver** создает в памяти нового приемника группы действий.</span><span class="sxs-lookup"><span data-stu-id="26811-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="26811-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26811-117">EXAMPLES</span></span>

### <span data-ttu-id="26811-118">Пример 1: создание нового получателя электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="26811-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="26811-119">Эта команда создает новый ресивер электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="26811-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="26811-120">Пример 2: создание нового приемника SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="26811-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="26811-121">Эта команда создает новый ресивер SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="26811-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="26811-122">Пример 3: создание в памяти нового приемника веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="26811-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="26811-123">Эта команда создает в памяти нового приемника веб-перехватчиков.</span><span class="sxs-lookup"><span data-stu-id="26811-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="26811-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26811-124">PARAMETERS</span></span>

### <span data-ttu-id="26811-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="26811-126">Создание ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="26811-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="26811-127">-AutomationAccountId</span></span>
<span data-ttu-id="26811-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="26811-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="26811-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="26811-130">Создание AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="26811-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="26811-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="26811-132">URI, на который должны отправляться веб-перехватчики</span><span class="sxs-lookup"><span data-stu-id="26811-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="26811-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="26811-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="26811-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="26811-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="26811-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="26811-136">Создание AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="26811-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="26811-138">Создание ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="26811-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="26811-139">-CallbackUrl</span></span>
<span data-ttu-id="26811-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="26811-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="26811-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="26811-141">-ConnectionId</span></span>
<span data-ttu-id="26811-142">Идентификатор подключения ITSM для этого получателя.</span><span class="sxs-lookup"><span data-stu-id="26811-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="26811-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="26811-143">-CountryCode</span></span>
<span data-ttu-id="26811-144">Указывает код страны для получателя SMS.</span><span class="sxs-lookup"><span data-stu-id="26811-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="26811-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26811-145">-DefaultProfile</span></span>
<span data-ttu-id="26811-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="26811-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26811-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="26811-147">-EmailAddress</span></span>
<span data-ttu-id="26811-148">Указывает адрес получателя электронной почты.</span><span class="sxs-lookup"><span data-stu-id="26811-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="26811-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-149">-EmailReceiver</span></span>
<span data-ttu-id="26811-150">Указывает, что нужно создать получателя электронной почты</span><span class="sxs-lookup"><span data-stu-id="26811-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="26811-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="26811-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="26811-152">ИД приложения функции</span><span class="sxs-lookup"><span data-stu-id="26811-152">the function app resourceId</span></span>

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

### <span data-ttu-id="26811-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="26811-153">-FunctionName</span></span>
<span data-ttu-id="26811-154">"functionName"</span><span class="sxs-lookup"><span data-stu-id="26811-154">the functionName</span></span>

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

### <span data-ttu-id="26811-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="26811-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="26811-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="26811-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="26811-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="26811-157">-IdentifierUri</span></span>
<span data-ttu-id="26811-158">универсальный код ресурса (URI) идентификатора для проверки подлинности AAD</span><span class="sxs-lookup"><span data-stu-id="26811-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="26811-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="26811-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="26811-160">Указывает, является ли этот экземпляр глобальным модулем Runbook</span><span class="sxs-lookup"><span data-stu-id="26811-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="26811-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-161">-ItsmReceiver</span></span>
<span data-ttu-id="26811-162">Создание ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="26811-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-163">-LogicAppReceiver</span></span>
<span data-ttu-id="26811-164">Создание LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="26811-165">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26811-165">-Name</span></span>
<span data-ttu-id="26811-166">Указывает имя получателя.</span><span class="sxs-lookup"><span data-stu-id="26811-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="26811-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="26811-167">-ObjectId</span></span>
<span data-ttu-id="26811-168">Идентификатор объекта приложения веб-перехватчика для проверки подлинности AAD</span><span class="sxs-lookup"><span data-stu-id="26811-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="26811-169">-Заданный</span><span class="sxs-lookup"><span data-stu-id="26811-169">-PhoneNumber</span></span>
<span data-ttu-id="26811-170">Задает номер телефона для ресивера SMS.</span><span class="sxs-lookup"><span data-stu-id="26811-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="26811-171">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="26811-171">-Region</span></span>
<span data-ttu-id="26811-172">itsmская область этого получателя.</span><span class="sxs-lookup"><span data-stu-id="26811-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="26811-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26811-173">-ResourceId</span></span>
<span data-ttu-id="26811-174">ResourceId (ИД ресурса)</span><span class="sxs-lookup"><span data-stu-id="26811-174">the ResourceId</span></span>

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

### <span data-ttu-id="26811-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="26811-175">-RoleId</span></span>
<span data-ttu-id="26811-176">Идентификатор роли ARM получателя.</span><span class="sxs-lookup"><span data-stu-id="26811-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="26811-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="26811-177">-RunbookName</span></span>
<span data-ttu-id="26811-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="26811-178">the RunbookName</span></span>

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

### <span data-ttu-id="26811-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="26811-179">-ServiceUri</span></span>
<span data-ttu-id="26811-180">Задает универсальный код ресурса (URI) для приемника веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="26811-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="26811-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-181">-SmsReceiver</span></span>
<span data-ttu-id="26811-182">Указывает, что нужно создать ресивер SMS</span><span class="sxs-lookup"><span data-stu-id="26811-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="26811-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="26811-183">-TenantId</span></span>
<span data-ttu-id="26811-184">Идентификатор клиента для проверки подлинности AAD</span><span class="sxs-lookup"><span data-stu-id="26811-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="26811-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="26811-185">-TicketConfiguration</span></span>
<span data-ttu-id="26811-186">ITSM TicketConfiguration этого получателя.</span><span class="sxs-lookup"><span data-stu-id="26811-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="26811-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="26811-187">-UseAadAuth</span></span>
<span data-ttu-id="26811-188">флаг для использования добавления проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="26811-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="26811-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="26811-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="26811-190">Пометка о том, следует ли использовать общую схему оповещения.</span><span class="sxs-lookup"><span data-stu-id="26811-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="26811-191">Это значение будет использоваться в neglectedfor SMS, приложении Azure Push, ITSM и голосовой recievers.</span><span class="sxs-lookup"><span data-stu-id="26811-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="26811-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="26811-192">-VoiceCountryCode</span></span>
<span data-ttu-id="26811-193">Код страны для голосового приемника</span><span class="sxs-lookup"><span data-stu-id="26811-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="26811-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="26811-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="26811-195">Номер телефона голосового приемника</span><span class="sxs-lookup"><span data-stu-id="26811-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="26811-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-196">-VoiceReceiver</span></span>
<span data-ttu-id="26811-197">Создание голосового приемника</span><span class="sxs-lookup"><span data-stu-id="26811-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="26811-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="26811-198">-WebhookReceiver</span></span>
<span data-ttu-id="26811-199">Указывает, что нужно создать приемник веб-перехватчика</span><span class="sxs-lookup"><span data-stu-id="26811-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="26811-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="26811-200">-WebhookResourceId</span></span>
<span data-ttu-id="26811-201">WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="26811-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="26811-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="26811-202">-WorkspaceId</span></span>
<span data-ttu-id="26811-203">идентификатор рабочей области ITSM для этого получателя.</span><span class="sxs-lookup"><span data-stu-id="26811-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="26811-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26811-204">CommonParameters</span></span>
<span data-ttu-id="26811-205">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26811-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26811-206">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26811-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26811-207">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26811-207">INPUTS</span></span>

### <span data-ttu-id="26811-208">System. String</span><span class="sxs-lookup"><span data-stu-id="26811-208">System.String</span></span>

### <span data-ttu-id="26811-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="26811-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26811-210">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26811-210">OUTPUTS</span></span>

### <span data-ttu-id="26811-211">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="26811-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="26811-212">Пуск</span><span class="sxs-lookup"><span data-stu-id="26811-212">NOTES</span></span>

## <span data-ttu-id="26811-213">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26811-213">RELATED LINKS</span></span>

<span data-ttu-id="26811-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="26811-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
