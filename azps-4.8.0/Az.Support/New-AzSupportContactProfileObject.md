---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243169"
---
# <span data-ttu-id="3b9b4-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="3b9b4-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="3b9b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9b4-103">Создание объекта профиля контакта в службе поддержки.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="3b9b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b9b4-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b9b4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b9b4-105">DESCRIPTION</span></span>
<span data-ttu-id="3b9b4-106">Это вспомогательный командлет, с помощью которого можно создать объект профиля контакта поддержки при создании или обновлении билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="3b9b4-107">Необходимо указать следующие параметры, которые являются обязательными для создания билета службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="3b9b4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b9b4-108">EXAMPLES</span></span>

### <span data-ttu-id="3b9b4-109">Пример 1: создание объекта контакта</span><span class="sxs-lookup"><span data-stu-id="3b9b4-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="3b9b4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b9b4-110">PARAMETERS</span></span>

### <span data-ttu-id="3b9b4-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3b9b4-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="3b9b4-112">Адреса электронной почты, указанные здесь, будут скопированы в соответствии с билетом поддержки.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="3b9b4-113">-Country</span><span class="sxs-lookup"><span data-stu-id="3b9b4-113">-Country</span></span>
<span data-ttu-id="3b9b4-114">Страна клиента.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-114">Customer country.</span></span>
<span data-ttu-id="3b9b4-115">Это должен быть допустимый код страны (ISO 3166) в формате ISO Alpha-3.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="3b9b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9b4-116">-DefaultProfile</span></span>
<span data-ttu-id="3b9b4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b9b4-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="3b9b4-118">-FirstName</span></span>
<span data-ttu-id="3b9b4-119">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-119">Customer first name.</span></span>

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

### <span data-ttu-id="3b9b4-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="3b9b4-120">-LastName</span></span>
<span data-ttu-id="3b9b4-121">Фамилия пользователя.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-121">Customer last name.</span></span>

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

### <span data-ttu-id="3b9b4-122">-Заданный</span><span class="sxs-lookup"><span data-stu-id="3b9b4-122">-PhoneNumber</span></span>
<span data-ttu-id="3b9b4-123">Номер телефона клиента.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-123">Customer phone number.</span></span>
<span data-ttu-id="3b9b4-124">Это необходимо, если предпочтительный метод связи — Phone.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="3b9b4-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="3b9b4-125">-PreferredContactMethod</span></span>
<span data-ttu-id="3b9b4-126">Предпочтительный метод связи.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="3b9b4-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="3b9b4-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="3b9b4-128">Язык предпочтительного обслуживания клиента.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-128">Customer preferred support language.</span></span>
<span data-ttu-id="3b9b4-129">Это должен быть допустимый код для языкового элемента для одного из поддерживаемых языков, перечисленных здесь https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="3b9b4-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="3b9b4-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="3b9b4-130">-PreferredTimeZone</span></span>
<span data-ttu-id="3b9b4-131">Предпочитаемый пользователем часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-131">Customer preferred time zone.</span></span>
<span data-ttu-id="3b9b4-132">Это должно быть действительное значение System.TimeZoneInfo.Id.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="3b9b4-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3b9b4-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="3b9b4-134">Основной адрес электронной почты клиента.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="3b9b4-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b9b4-135">-Confirm</span></span>
<span data-ttu-id="3b9b4-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b9b4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b9b4-137">-WhatIf</span></span>
<span data-ttu-id="3b9b4-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b9b4-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b9b4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9b4-140">CommonParameters</span></span>
<span data-ttu-id="3b9b4-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9b4-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b9b4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9b4-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b9b4-143">INPUTS</span></span>

### <span data-ttu-id="3b9b4-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="3b9b4-144">None</span></span>

## <span data-ttu-id="3b9b4-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b9b4-145">OUTPUTS</span></span>

### <span data-ttu-id="3b9b4-146">Microsoft. Azure. Commands. support. Models. PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="3b9b4-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="3b9b4-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b9b4-147">NOTES</span></span>

## <span data-ttu-id="3b9b4-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b9b4-148">RELATED LINKS</span></span>
