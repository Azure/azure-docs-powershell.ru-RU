---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505587"
---
# <span data-ttu-id="d2579-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="d2579-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="d2579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2579-102">SYNOPSIS</span></span>
<span data-ttu-id="d2579-103">Создает объект профиля контакта службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="d2579-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="d2579-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2579-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2579-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2579-105">DESCRIPTION</span></span>
<span data-ttu-id="d2579-106">Это дополнительный cmdlet, который можно использовать для создания объекта профиля службы поддержки при создании или обновлении билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="d2579-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="d2579-107">Необходимо указать следующие параметры, которые являются обязательными для создания билета в службу поддержки:</span><span class="sxs-lookup"><span data-stu-id="d2579-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="d2579-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2579-108">EXAMPLES</span></span>

### <span data-ttu-id="d2579-109">Пример 1. Создание объекта контакта</span><span class="sxs-lookup"><span data-stu-id="d2579-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="d2579-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2579-110">PARAMETERS</span></span>

### <span data-ttu-id="d2579-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d2579-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="d2579-112">Указанные здесь адреса электронной почты будут скопированы в любое переписке по поводу билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="d2579-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2579-113">-Country</span><span class="sxs-lookup"><span data-stu-id="d2579-113">-Country</span></span>
<span data-ttu-id="d2579-114">Страна клиента.</span><span class="sxs-lookup"><span data-stu-id="d2579-114">Customer country.</span></span>
<span data-ttu-id="d2579-115">Это должен быть действительный код страны ISO Alpha-3 (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="d2579-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2579-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2579-116">-DefaultProfile</span></span>
<span data-ttu-id="d2579-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2579-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2579-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="d2579-118">-FirstName</span></span>
<span data-ttu-id="d2579-119">Имя клиента.</span><span class="sxs-lookup"><span data-stu-id="d2579-119">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2579-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="d2579-120">-LastName</span></span>
<span data-ttu-id="d2579-121">Фамилия клиента.</span><span class="sxs-lookup"><span data-stu-id="d2579-121">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2579-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="d2579-122">-PhoneNumber</span></span>
<span data-ttu-id="d2579-123">Номер телефона клиента.</span><span class="sxs-lookup"><span data-stu-id="d2579-123">Customer phone number.</span></span>
<span data-ttu-id="d2579-124">Это необходимо, если предпочтительный способ связи — телефон.</span><span class="sxs-lookup"><span data-stu-id="d2579-124">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2579-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="d2579-125">-PreferredContactMethod</span></span>
<span data-ttu-id="d2579-126">Предпочтительный способ связи.</span><span class="sxs-lookup"><span data-stu-id="d2579-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2579-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="d2579-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="d2579-128">Язык поддержки, предпочитаемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="d2579-128">Customer preferred support language.</span></span>
<span data-ttu-id="d2579-129">Это должен быть допустимый код для одного из поддерживаемых языков, перечисленных в этом https://azure.microsoft.com/support/faq/ списке.</span><span class="sxs-lookup"><span data-stu-id="d2579-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2579-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="d2579-130">-PreferredTimeZone</span></span>
<span data-ttu-id="d2579-131">Часовой пояс, предпочитаемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="d2579-131">Customer preferred time zone.</span></span>
<span data-ttu-id="d2579-132">Значение должно быть System.TimeZoneInfo.Id значением.</span><span class="sxs-lookup"><span data-stu-id="d2579-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2579-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d2579-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="d2579-134">Основной адрес электронной почты клиента.</span><span class="sxs-lookup"><span data-stu-id="d2579-134">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2579-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2579-135">-Confirm</span></span>
<span data-ttu-id="d2579-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2579-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2579-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2579-137">-WhatIf</span></span>
<span data-ttu-id="d2579-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2579-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2579-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d2579-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2579-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2579-140">CommonParameters</span></span>
<span data-ttu-id="d2579-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2579-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2579-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2579-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2579-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2579-143">INPUTS</span></span>

### <span data-ttu-id="d2579-144">Нет</span><span class="sxs-lookup"><span data-stu-id="d2579-144">None</span></span>

## <span data-ttu-id="d2579-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2579-145">OUTPUTS</span></span>

### <span data-ttu-id="d2579-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="d2579-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="d2579-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2579-147">NOTES</span></span>

## <span data-ttu-id="d2579-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2579-148">RELATED LINKS</span></span>
