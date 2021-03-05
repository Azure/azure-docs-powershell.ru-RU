---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 5fac9eac7225364af7c884ab64a80d4299939ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005027"
---
# <span data-ttu-id="c9237-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c9237-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="c9237-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9237-102">SYNOPSIS</span></span>
<span data-ttu-id="c9237-103">Обновляет билет в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c9237-103">Updates support ticket.</span></span>

## <span data-ttu-id="c9237-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c9237-104">SYNTAX</span></span>

### <span data-ttu-id="c9237-105">UpdateByNameWithContactDetailParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9237-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9237-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9237-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9237-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9237-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9237-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9237-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9237-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9237-109">DESCRIPTION</span></span>
<span data-ttu-id="c9237-110">Используйте этот cmdlet для обновления уровня серьезности, состояния или контактных данных клиента.</span><span class="sxs-lookup"><span data-stu-id="c9237-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="c9237-111">Обратите внимание, что обновление уровня серьезности или состояния для билета в службу поддержки не допускается, если он назначен инженеру службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="c9237-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="c9237-112">Если вы хотите обновить уровень серьезности или состояние после назначения билета, обратитесь к инженеру службы поддержки, отправив сообщение с вопросом.</span><span class="sxs-lookup"><span data-stu-id="c9237-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="c9237-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c9237-113">EXAMPLES</span></span>

### <span data-ttu-id="c9237-114">Пример 1. Обновление серьезности билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c9237-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c9237-115">Пример 2. Обновление состояния билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c9237-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c9237-116">Пример 3. Обновив контактные данные для билета в службу поддержки, укажите объект контакта.</span><span class="sxs-lookup"><span data-stu-id="c9237-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c9237-117">Пример 4. Обновив уровень серьезности билета в службу поддержки, с помощью piping support ticket object.</span><span class="sxs-lookup"><span data-stu-id="c9237-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c9237-118">Пример 5. Обновление контактных данных для билета в службу поддержки с помощью параметров контактов.</span><span class="sxs-lookup"><span data-stu-id="c9237-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c9237-119">Пример 6. Обновление состояния билета в службу поддержки путем обновки объекта билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c9237-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="c9237-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9237-120">PARAMETERS</span></span>

### <span data-ttu-id="c9237-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c9237-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="c9237-122">Дополнительные адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c9237-122">Additional email addresses.</span></span>
<span data-ttu-id="c9237-123">Указанные здесь адреса электронной почты будут скопированы в любое переписке по поводу билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c9237-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="c9237-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="c9237-124">-CustomerContactDetail</span></span>
<span data-ttu-id="c9237-125">Обновив контактные данные на supportTicket.</span><span class="sxs-lookup"><span data-stu-id="c9237-125">Update Contact details on SupportTicket.</span></span>

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

### <span data-ttu-id="c9237-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="c9237-126">-CustomerCountry</span></span>
<span data-ttu-id="c9237-127">Страна клиента.</span><span class="sxs-lookup"><span data-stu-id="c9237-127">Customer country.</span></span>
<span data-ttu-id="c9237-128">Это должен быть действительный код страны ISO Alpha-3 (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="c9237-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="c9237-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="c9237-129">-CustomerFirstName</span></span>
<span data-ttu-id="c9237-130">Имя клиента.</span><span class="sxs-lookup"><span data-stu-id="c9237-130">Customer first name.</span></span>

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

### <span data-ttu-id="c9237-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="c9237-131">-CustomerLastName</span></span>
<span data-ttu-id="c9237-132">Фамилия клиента.</span><span class="sxs-lookup"><span data-stu-id="c9237-132">Customer last name.</span></span>

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

### <span data-ttu-id="c9237-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="c9237-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="c9237-134">Номер телефона клиента.</span><span class="sxs-lookup"><span data-stu-id="c9237-134">Customer phone number.</span></span>
<span data-ttu-id="c9237-135">Это необходимо, если предпочтительный способ связи — телефон.</span><span class="sxs-lookup"><span data-stu-id="c9237-135">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="c9237-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="c9237-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="c9237-137">Язык поддержки, предпочитаемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="c9237-137">Customer preferred support language.</span></span>
<span data-ttu-id="c9237-138">Это должен быть допустимый код для одного из поддерживаемых языков, перечисленных в этом https://azure.microsoft.com/support/faq/ списке.</span><span class="sxs-lookup"><span data-stu-id="c9237-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="c9237-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="c9237-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="c9237-140">Часовой пояс, предпочитаемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="c9237-140">Customer preferred time zone.</span></span>
<span data-ttu-id="c9237-141">Значение должно быть System.TimeZoneInfo.Id значением.</span><span class="sxs-lookup"><span data-stu-id="c9237-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="c9237-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c9237-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="c9237-143">Основной адрес электронной почты клиента.</span><span class="sxs-lookup"><span data-stu-id="c9237-143">Customer primary email address.</span></span>

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

### <span data-ttu-id="c9237-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9237-144">-DefaultProfile</span></span>
<span data-ttu-id="c9237-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9237-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9237-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9237-146">-InputObject</span></span>
<span data-ttu-id="c9237-147">Объект ресурса SupportTicket, который обновляется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9237-147">SupportTicket resource object that this cmdlet updates.</span></span>

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

### <span data-ttu-id="c9237-148">-Name</span><span class="sxs-lookup"><span data-stu-id="c9237-148">-Name</span></span>
<span data-ttu-id="c9237-149">Имя ресурса SupportTicket, который обновляется этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="c9237-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

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

### <span data-ttu-id="c9237-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="c9237-150">-PreferredContactMethod</span></span>
<span data-ttu-id="c9237-151">Предпочтительный способ связи.</span><span class="sxs-lookup"><span data-stu-id="c9237-151">Preferred contact method.</span></span>

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

### <span data-ttu-id="c9237-152">-Severity</span><span class="sxs-lookup"><span data-stu-id="c9237-152">-Severity</span></span>
<span data-ttu-id="c9237-153">"Обновить серьезность supportTicket".</span><span class="sxs-lookup"><span data-stu-id="c9237-153">Update Severity of SupportTicket.</span></span>

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

### <span data-ttu-id="c9237-154">-Status</span><span class="sxs-lookup"><span data-stu-id="c9237-154">-Status</span></span>
<span data-ttu-id="c9237-155">Состояние обновления supportTicket.</span><span class="sxs-lookup"><span data-stu-id="c9237-155">Update Status of SupportTicket.</span></span>

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

### <span data-ttu-id="c9237-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9237-156">-Confirm</span></span>
<span data-ttu-id="c9237-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9237-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9237-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9237-158">-WhatIf</span></span>
<span data-ttu-id="c9237-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9237-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9237-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c9237-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9237-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9237-161">CommonParameters</span></span>
<span data-ttu-id="c9237-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9237-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9237-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9237-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9237-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9237-164">INPUTS</span></span>

### <span data-ttu-id="c9237-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c9237-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="c9237-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9237-166">OUTPUTS</span></span>

### <span data-ttu-id="c9237-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c9237-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="c9237-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c9237-168">NOTES</span></span>

## <span data-ttu-id="c9237-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9237-169">RELATED LINKS</span></span>
