---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 917f6287c40d4c26123217cccbf1dfc11866a488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979907"
---
# <span data-ttu-id="956de-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="956de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="956de-102">SYNOPSIS</span></span>
<span data-ttu-id="956de-103">Создает новый приемник группы действий.</span><span class="sxs-lookup"><span data-stu-id="956de-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="956de-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="956de-104">SYNTAX</span></span>

### <span data-ttu-id="956de-105">NewEmailReceiver (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="956de-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="956de-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="956de-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="956de-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="956de-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="956de-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="956de-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="956de-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="956de-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="956de-114">NewAzureAppPыReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="956de-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="956de-115">DESCRIPTION</span></span>
<span data-ttu-id="956de-116">Для создания нового приемера группы действий в памяти создается новый приемник группы действий **New-AzActionGroupReceiver.**</span><span class="sxs-lookup"><span data-stu-id="956de-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="956de-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="956de-117">EXAMPLES</span></span>

### <span data-ttu-id="956de-118">Пример 1. Создание нового приемера электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="956de-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="956de-119">Эта команда создает новый приемник электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="956de-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="956de-120">Пример 2. Создайте новый приемник SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="956de-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="956de-121">Эта команда создает новый приемник SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="956de-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="956de-122">Пример 3. Создайте новый приемник webhook в памяти.</span><span class="sxs-lookup"><span data-stu-id="956de-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="956de-123">Эта команда создает новый приемник webhook в памяти.</span><span class="sxs-lookup"><span data-stu-id="956de-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="956de-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="956de-124">PARAMETERS</span></span>

### <span data-ttu-id="956de-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="956de-126">Создание armRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="956de-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="956de-127">-AutomationAccountId</span></span>
<span data-ttu-id="956de-128">the AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="956de-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="956de-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="956de-130">Создание automationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="956de-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="956de-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="956de-132">URI, в который должны быть отправлены веб-сайты</span><span class="sxs-lookup"><span data-stu-id="956de-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="956de-133">-AzureAppPmailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="956de-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="956de-134">the AzureAppPmailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="956de-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="956de-135">-AzureAppPовReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="956de-136">Создание AzureAppP уreceiver</span><span class="sxs-lookup"><span data-stu-id="956de-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="956de-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="956de-138">Создание armRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="956de-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="956de-139">-CallbackUrl</span></span>
<span data-ttu-id="956de-140">the CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="956de-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="956de-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="956de-141">-ConnectionId</span></span>
<span data-ttu-id="956de-142">the itsm connection id of this receiver</span><span class="sxs-lookup"><span data-stu-id="956de-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="956de-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="956de-143">-CountryCode</span></span>
<span data-ttu-id="956de-144">Код страны для приемник SMS.</span><span class="sxs-lookup"><span data-stu-id="956de-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="956de-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956de-145">-DefaultProfile</span></span>
<span data-ttu-id="956de-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="956de-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="956de-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="956de-147">-EmailAddress</span></span>
<span data-ttu-id="956de-148">Адрес для получения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="956de-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="956de-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-149">-EmailReceiver</span></span>
<span data-ttu-id="956de-150">Указывает, что нужно создать приемник электронной почты</span><span class="sxs-lookup"><span data-stu-id="956de-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="956de-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="956de-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="956de-152">resourceId приложения функции</span><span class="sxs-lookup"><span data-stu-id="956de-152">the function app resourceId</span></span>

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

### <span data-ttu-id="956de-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="956de-153">-FunctionName</span></span>
<span data-ttu-id="956de-154">the functionName</span><span class="sxs-lookup"><span data-stu-id="956de-154">the functionName</span></span>

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

### <span data-ttu-id="956de-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="956de-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="956de-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="956de-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="956de-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="956de-157">-IdentifierUri</span></span>
<span data-ttu-id="956de-158">URI идентификатора для aad auth</span><span class="sxs-lookup"><span data-stu-id="956de-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="956de-159">-IsBalbalRunbook</span><span class="sxs-lookup"><span data-stu-id="956de-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="956de-160">указывает, является ли этот экземпляр глобальной runbook</span><span class="sxs-lookup"><span data-stu-id="956de-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="956de-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-161">-ItsmReceiver</span></span>
<span data-ttu-id="956de-162">Создание itsmReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="956de-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-163">-LogicAppReceiver</span></span>
<span data-ttu-id="956de-164">Создание logicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="956de-165">-Name</span><span class="sxs-lookup"><span data-stu-id="956de-165">-Name</span></span>
<span data-ttu-id="956de-166">Указывает имя приемник.</span><span class="sxs-lookup"><span data-stu-id="956de-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="956de-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="956de-167">-ObjectId</span></span>
<span data-ttu-id="956de-168">ИД объекта приложения WebHook для aad auth</span><span class="sxs-lookup"><span data-stu-id="956de-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="956de-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="956de-169">-PhoneNumber</span></span>
<span data-ttu-id="956de-170">Номер телефона для приемки SMS.</span><span class="sxs-lookup"><span data-stu-id="956de-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="956de-171">-Регион</span><span class="sxs-lookup"><span data-stu-id="956de-171">-Region</span></span>
<span data-ttu-id="956de-172">itsm Region of this receiver</span><span class="sxs-lookup"><span data-stu-id="956de-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="956de-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="956de-173">-ResourceId</span></span>
<span data-ttu-id="956de-174">the ResourceId</span><span class="sxs-lookup"><span data-stu-id="956de-174">the ResourceId</span></span>

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

### <span data-ttu-id="956de-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="956de-175">-RoleId</span></span>
<span data-ttu-id="956de-176">The arm role id of the receiver</span><span class="sxs-lookup"><span data-stu-id="956de-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="956de-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="956de-177">-RunbookName</span></span>
<span data-ttu-id="956de-178">the RunbookName</span><span class="sxs-lookup"><span data-stu-id="956de-178">the RunbookName</span></span>

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

### <span data-ttu-id="956de-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="956de-179">-ServiceUri</span></span>
<span data-ttu-id="956de-180">Определяет URI для приемера веб-ook.</span><span class="sxs-lookup"><span data-stu-id="956de-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="956de-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-181">-SmsReceiver</span></span>
<span data-ttu-id="956de-182">Указывает, что нужно создать приемник SMS</span><span class="sxs-lookup"><span data-stu-id="956de-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="956de-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="956de-183">-TenantId</span></span>
<span data-ttu-id="956de-184">ид клиента для aad auth</span><span class="sxs-lookup"><span data-stu-id="956de-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="956de-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="956de-185">-TicketConfiguration</span></span>
<span data-ttu-id="956de-186">The itsm TicketConfiguration of this receiver</span><span class="sxs-lookup"><span data-stu-id="956de-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="956de-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="956de-187">-UseAadAuth</span></span>
<span data-ttu-id="956de-188">Флажок для добавления auth</span><span class="sxs-lookup"><span data-stu-id="956de-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="956de-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="956de-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="956de-190">Флажок, следует ли использовать общую схему оповещения.</span><span class="sxs-lookup"><span data-stu-id="956de-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="956de-191">Это значение не будет игнорироваться для служб SMS, Azure App Push, ITSM и голосового сообщения.</span><span class="sxs-lookup"><span data-stu-id="956de-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="956de-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="956de-192">-VoiceCountryCode</span></span>
<span data-ttu-id="956de-193">Код страны получения голосовой почты</span><span class="sxs-lookup"><span data-stu-id="956de-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="956de-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="956de-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="956de-195">Номер телефона телефонного трубки</span><span class="sxs-lookup"><span data-stu-id="956de-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="956de-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-196">-VoiceReceiver</span></span>
<span data-ttu-id="956de-197">Создание приемной голоса</span><span class="sxs-lookup"><span data-stu-id="956de-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="956de-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="956de-198">-WebhookReceiver</span></span>
<span data-ttu-id="956de-199">Указывает, что нужно создать приемник webhook</span><span class="sxs-lookup"><span data-stu-id="956de-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="956de-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="956de-200">-WebhookResourceId</span></span>
<span data-ttu-id="956de-201">the WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="956de-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="956de-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="956de-202">-WorkspaceId</span></span>
<span data-ttu-id="956de-203">id рабочей области itsm этого приемник</span><span class="sxs-lookup"><span data-stu-id="956de-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="956de-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956de-204">CommonParameters</span></span>
<span data-ttu-id="956de-205">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="956de-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956de-206">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="956de-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956de-207">INPUTS</span><span class="sxs-lookup"><span data-stu-id="956de-207">INPUTS</span></span>

### <span data-ttu-id="956de-208">System.String</span><span class="sxs-lookup"><span data-stu-id="956de-208">System.String</span></span>

### <span data-ttu-id="956de-209">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="956de-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="956de-210">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="956de-210">OUTPUTS</span></span>

### <span data-ttu-id="956de-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="956de-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="956de-212">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="956de-212">NOTES</span></span>

## <span data-ttu-id="956de-213">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="956de-213">RELATED LINKS</span></span>

<span data-ttu-id="956de-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="956de-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
