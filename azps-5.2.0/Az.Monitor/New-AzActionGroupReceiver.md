---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391300"
---
# <span data-ttu-id="36514-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="36514-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36514-102">SYNOPSIS</span></span>
<span data-ttu-id="36514-103">Создает новый приемник группы действий.</span><span class="sxs-lookup"><span data-stu-id="36514-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="36514-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36514-104">SYNTAX</span></span>

### <span data-ttu-id="36514-105">NewEmailReceiver (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36514-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36514-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36514-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36514-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36514-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36514-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36514-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36514-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36514-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36514-114">NewAzureAppPыReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36514-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36514-115">DESCRIPTION</span></span>
<span data-ttu-id="36514-116">Для создания нового приемера группы действий в памяти создается новый приемник группы действий **New-AzActionGroupReceiver.**</span><span class="sxs-lookup"><span data-stu-id="36514-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="36514-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36514-117">EXAMPLES</span></span>

### <span data-ttu-id="36514-118">Пример 1. Создание нового приемера электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="36514-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="36514-119">Эта команда создает новый приемник электронной почты в памяти.</span><span class="sxs-lookup"><span data-stu-id="36514-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="36514-120">Пример 2. Создание нового приемника SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="36514-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="36514-121">Эта команда создает новый приемник SMS в памяти.</span><span class="sxs-lookup"><span data-stu-id="36514-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="36514-122">Пример 3. Создайте новый приемник webhook в памяти.</span><span class="sxs-lookup"><span data-stu-id="36514-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="36514-123">Эта команда создает новый приемник webhook в памяти.</span><span class="sxs-lookup"><span data-stu-id="36514-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="36514-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36514-124">PARAMETERS</span></span>

### <span data-ttu-id="36514-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="36514-126">Создание armRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="36514-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="36514-127">-AutomationAccountId</span></span>
<span data-ttu-id="36514-128">the AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="36514-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="36514-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="36514-130">Создание automationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="36514-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="36514-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="36514-132">URI, в который должны быть отправлены веб-сайты</span><span class="sxs-lookup"><span data-stu-id="36514-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="36514-133">-AzureAppPmailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="36514-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="36514-134">the AzureAppPmailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="36514-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="36514-135">-AzureAppPовReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="36514-136">Создание AzureAppPыReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="36514-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="36514-138">Создание armRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="36514-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="36514-139">-CallbackUrl</span></span>
<span data-ttu-id="36514-140">The CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="36514-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="36514-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="36514-141">-ConnectionId</span></span>
<span data-ttu-id="36514-142">the itsm connection id of this receiver</span><span class="sxs-lookup"><span data-stu-id="36514-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="36514-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="36514-143">-CountryCode</span></span>
<span data-ttu-id="36514-144">Код страны для приемник SMS.</span><span class="sxs-lookup"><span data-stu-id="36514-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="36514-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36514-145">-DefaultProfile</span></span>
<span data-ttu-id="36514-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="36514-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36514-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="36514-147">-EmailAddress</span></span>
<span data-ttu-id="36514-148">Адрес для получения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="36514-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="36514-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-149">-EmailReceiver</span></span>
<span data-ttu-id="36514-150">Указывает, что нужно создать приемник электронной почты</span><span class="sxs-lookup"><span data-stu-id="36514-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="36514-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="36514-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="36514-152">resourceId приложения функции</span><span class="sxs-lookup"><span data-stu-id="36514-152">the function app resourceId</span></span>

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

### <span data-ttu-id="36514-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="36514-153">-FunctionName</span></span>
<span data-ttu-id="36514-154">the functionName</span><span class="sxs-lookup"><span data-stu-id="36514-154">the functionName</span></span>

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

### <span data-ttu-id="36514-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="36514-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="36514-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="36514-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="36514-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="36514-157">-IdentifierUri</span></span>
<span data-ttu-id="36514-158">URI идентификатора для aad auth</span><span class="sxs-lookup"><span data-stu-id="36514-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="36514-159">-IsBalBalRunbook</span><span class="sxs-lookup"><span data-stu-id="36514-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="36514-160">указывает, является ли этот экземпляр глобальной runbook</span><span class="sxs-lookup"><span data-stu-id="36514-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="36514-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-161">-ItsmReceiver</span></span>
<span data-ttu-id="36514-162">Создание itsmReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="36514-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-163">-LogicAppReceiver</span></span>
<span data-ttu-id="36514-164">Создание logicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="36514-165">-Name</span><span class="sxs-lookup"><span data-stu-id="36514-165">-Name</span></span>
<span data-ttu-id="36514-166">Указывает имя приемник.</span><span class="sxs-lookup"><span data-stu-id="36514-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="36514-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="36514-167">-ObjectId</span></span>
<span data-ttu-id="36514-168">ИД объекта приложения WebHook для aad auth</span><span class="sxs-lookup"><span data-stu-id="36514-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="36514-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="36514-169">-PhoneNumber</span></span>
<span data-ttu-id="36514-170">Номер телефона для приемки SMS.</span><span class="sxs-lookup"><span data-stu-id="36514-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="36514-171">-Регион</span><span class="sxs-lookup"><span data-stu-id="36514-171">-Region</span></span>
<span data-ttu-id="36514-172">itsm Region of this receiver</span><span class="sxs-lookup"><span data-stu-id="36514-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="36514-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36514-173">-ResourceId</span></span>
<span data-ttu-id="36514-174">the ResourceId</span><span class="sxs-lookup"><span data-stu-id="36514-174">the ResourceId</span></span>

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

### <span data-ttu-id="36514-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="36514-175">-RoleId</span></span>
<span data-ttu-id="36514-176">The arm role id of the receiver</span><span class="sxs-lookup"><span data-stu-id="36514-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="36514-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="36514-177">-RunbookName</span></span>
<span data-ttu-id="36514-178">the RunbookName</span><span class="sxs-lookup"><span data-stu-id="36514-178">the RunbookName</span></span>

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

### <span data-ttu-id="36514-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="36514-179">-ServiceUri</span></span>
<span data-ttu-id="36514-180">Определяет URI для приемера веб-ook.</span><span class="sxs-lookup"><span data-stu-id="36514-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="36514-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-181">-SmsReceiver</span></span>
<span data-ttu-id="36514-182">Указывает, что нужно создать приемник SMS</span><span class="sxs-lookup"><span data-stu-id="36514-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="36514-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="36514-183">-TenantId</span></span>
<span data-ttu-id="36514-184">ид клиента для aad auth</span><span class="sxs-lookup"><span data-stu-id="36514-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="36514-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="36514-185">-TicketConfiguration</span></span>
<span data-ttu-id="36514-186">The itsm TicketConfiguration of this receiver</span><span class="sxs-lookup"><span data-stu-id="36514-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="36514-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="36514-187">-UseAadAuth</span></span>
<span data-ttu-id="36514-188">Флажок для добавления auth</span><span class="sxs-lookup"><span data-stu-id="36514-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="36514-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="36514-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="36514-190">Флажок, следует ли использовать общую схему оповещения.</span><span class="sxs-lookup"><span data-stu-id="36514-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="36514-191">Это значение будет игнорироваться для СЛУЖБ SMS, Azure App Push, ITSM и голосового сообщения.</span><span class="sxs-lookup"><span data-stu-id="36514-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="36514-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="36514-192">-VoiceCountryCode</span></span>
<span data-ttu-id="36514-193">Код страны получения голосовой почты</span><span class="sxs-lookup"><span data-stu-id="36514-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="36514-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="36514-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="36514-195">Номер телефона в приемнике голосовой связи</span><span class="sxs-lookup"><span data-stu-id="36514-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="36514-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-196">-VoiceReceiver</span></span>
<span data-ttu-id="36514-197">Создание приемной голоса</span><span class="sxs-lookup"><span data-stu-id="36514-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="36514-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="36514-198">-WebhookReceiver</span></span>
<span data-ttu-id="36514-199">Указывает, что нужно создать приемник webhook</span><span class="sxs-lookup"><span data-stu-id="36514-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="36514-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="36514-200">-WebhookResourceId</span></span>
<span data-ttu-id="36514-201">the WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="36514-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="36514-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="36514-202">-WorkspaceId</span></span>
<span data-ttu-id="36514-203">id рабочей области itsm этого приемник</span><span class="sxs-lookup"><span data-stu-id="36514-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="36514-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36514-204">CommonParameters</span></span>
<span data-ttu-id="36514-205">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36514-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36514-206">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36514-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36514-207">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36514-207">INPUTS</span></span>

### <span data-ttu-id="36514-208">System.String</span><span class="sxs-lookup"><span data-stu-id="36514-208">System.String</span></span>

### <span data-ttu-id="36514-209">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36514-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36514-210">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36514-210">OUTPUTS</span></span>

### <span data-ttu-id="36514-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="36514-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="36514-212">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36514-212">NOTES</span></span>

## <span data-ttu-id="36514-213">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36514-213">RELATED LINKS</span></span>

<span data-ttu-id="36514-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="36514-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
