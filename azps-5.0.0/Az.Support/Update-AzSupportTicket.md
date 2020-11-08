---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247150"
---
# <span data-ttu-id="fe000-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="fe000-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="fe000-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe000-102">SYNOPSIS</span></span>
<span data-ttu-id="fe000-103">Обновление билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="fe000-103">Updates support ticket.</span></span>

## <span data-ttu-id="fe000-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe000-104">SYNTAX</span></span>

### <span data-ttu-id="fe000-105">UpdateByNameWithContactDetailParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe000-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe000-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe000-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe000-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe000-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe000-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe000-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe000-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe000-109">DESCRIPTION</span></span>
<span data-ttu-id="fe000-110">Используйте этот командлет, чтобы обновить уровень важности билета на обслуживание, состояние или контактные данные клиента.</span><span class="sxs-lookup"><span data-stu-id="fe000-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="fe000-111">Обратите внимание, что при назначении билета специалисту службы поддержки не разрешается обновлять уровень серьезности билета и состояние.</span><span class="sxs-lookup"><span data-stu-id="fe000-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="fe000-112">Если вы хотите обновить уровень серьезности или состояние после назначения билета, обратитесь в инженера службы поддержки, отправив им связь на билете.</span><span class="sxs-lookup"><span data-stu-id="fe000-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="fe000-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe000-113">EXAMPLES</span></span>

### <span data-ttu-id="fe000-114">Пример 1: обновление важности билета поддержки.</span><span class="sxs-lookup"><span data-stu-id="fe000-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="fe000-115">Пример 2: обновление состояния билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="fe000-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="fe000-116">Пример 3: обновление контактных данных билета в службу поддержки с помощью указания объекта контакта.</span><span class="sxs-lookup"><span data-stu-id="fe000-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="fe000-117">Пример 4: обновление уровня серьезности билета поддержки посредством объекта билета поддержки трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="fe000-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="fe000-118">Пример 5. Обновите контактные данные билета в службу поддержки, указав индивидуальные параметры контакта.</span><span class="sxs-lookup"><span data-stu-id="fe000-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="fe000-119">Пример 6: обновление состояния билета поддержки с помощью объекта билета поддержки трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="fe000-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="fe000-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe000-120">PARAMETERS</span></span>

### <span data-ttu-id="fe000-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fe000-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="fe000-122">Дополнительные адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fe000-122">Additional email addresses.</span></span>
<span data-ttu-id="fe000-123">Адреса электронной почты, указанные здесь, будут скопированы в соответствии с билетом поддержки.</span><span class="sxs-lookup"><span data-stu-id="fe000-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="fe000-124">-CustomerContactDetail</span></span>
<span data-ttu-id="fe000-125">Обновите контактные данные в SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="fe000-125">Update Contact details on SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: UpdateByNameWithContactObjectParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="fe000-126">-CustomerCountry</span></span>
<span data-ttu-id="fe000-127">Страна клиента.</span><span class="sxs-lookup"><span data-stu-id="fe000-127">Customer country.</span></span>
<span data-ttu-id="fe000-128">Это должен быть допустимый код страны (ISO 3166) в формате ISO Alpha-3.</span><span class="sxs-lookup"><span data-stu-id="fe000-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="fe000-129">-CustomerFirstName</span></span>
<span data-ttu-id="fe000-130">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe000-130">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="fe000-131">-CustomerLastName</span></span>
<span data-ttu-id="fe000-132">Фамилия пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe000-132">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="fe000-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="fe000-134">Номер телефона клиента.</span><span class="sxs-lookup"><span data-stu-id="fe000-134">Customer phone number.</span></span>
<span data-ttu-id="fe000-135">Это необходимо, если предпочтительный метод связи — Phone.</span><span class="sxs-lookup"><span data-stu-id="fe000-135">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="fe000-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="fe000-137">Язык предпочтительного обслуживания клиента.</span><span class="sxs-lookup"><span data-stu-id="fe000-137">Customer preferred support language.</span></span>
<span data-ttu-id="fe000-138">Это должен быть допустимый код для языкового элемента для одного из поддерживаемых языков, перечисленных здесь https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="fe000-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="fe000-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="fe000-140">Предпочитаемый пользователем часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="fe000-140">Customer preferred time zone.</span></span>
<span data-ttu-id="fe000-141">Это должно быть действительное значение System.TimeZoneInfo.Id.</span><span class="sxs-lookup"><span data-stu-id="fe000-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fe000-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="fe000-143">Основной адрес электронной почты клиента.</span><span class="sxs-lookup"><span data-stu-id="fe000-143">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe000-144">-DefaultProfile</span></span>
<span data-ttu-id="fe000-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe000-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe000-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe000-146">-InputObject</span></span>
<span data-ttu-id="fe000-147">Объект ресурса SupportTicket, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fe000-147">SupportTicket resource object that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: UpdateByInputObjectWithContactDetailParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe000-148">-Name</span></span>
<span data-ttu-id="fe000-149">Имя ресурса SupportTicket, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fe000-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByNameWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="fe000-150">-PreferredContactMethod</span></span>
<span data-ttu-id="fe000-151">Предпочтительный метод связи.</span><span class="sxs-lookup"><span data-stu-id="fe000-151">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-152">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="fe000-152">-Severity</span></span>
<span data-ttu-id="fe000-153">Обновите уровень важности SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="fe000-153">Update Severity of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-154">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="fe000-154">-Status</span></span>
<span data-ttu-id="fe000-155">Обновить состояние SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="fe000-155">Update Status of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Status
Parameter Sets: (All)
Aliases:
Accepted values: Open, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe000-156">-Confirm</span></span>
<span data-ttu-id="fe000-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe000-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe000-158">-WhatIf</span></span>
<span data-ttu-id="fe000-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe000-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe000-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe000-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe000-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe000-161">CommonParameters</span></span>
<span data-ttu-id="fe000-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe000-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe000-163">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe000-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe000-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe000-164">INPUTS</span></span>

### <span data-ttu-id="fe000-165">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="fe000-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="fe000-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe000-166">OUTPUTS</span></span>

### <span data-ttu-id="fe000-167">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="fe000-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="fe000-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe000-168">NOTES</span></span>

## <span data-ttu-id="fe000-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe000-169">RELATED LINKS</span></span>
