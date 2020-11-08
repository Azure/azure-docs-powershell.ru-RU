---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: 13b157accea6303363aebca54eb68a5f0ffbd6d9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074458"
---
# <span data-ttu-id="55351-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="55351-101">New-AzADUser</span></span>

## <span data-ttu-id="55351-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55351-102">SYNOPSIS</span></span>
<span data-ttu-id="55351-103">Создание нового пользователя Active Directory.</span><span class="sxs-lookup"><span data-stu-id="55351-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="55351-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55351-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55351-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55351-105">DESCRIPTION</span></span>
<span data-ttu-id="55351-106">Создание нового пользователя Active Directory (рабочей или учебной учетной записи, которая известна как "org-ID").</span><span class="sxs-lookup"><span data-stu-id="55351-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="55351-107">Дополнительные сведения: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="55351-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="55351-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55351-108">EXAMPLES</span></span>

### <span data-ttu-id="55351-109">Пример 1: создание нового пользователя рекламы</span><span class="sxs-lookup"><span data-stu-id="55351-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="55351-110">Создает в клиенте нового пользователя AD с именем "MyDisplayName" и именем участника-пользователя " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="55351-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="55351-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55351-111">PARAMETERS</span></span>

### <span data-ttu-id="55351-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55351-112">-DefaultProfile</span></span>
<span data-ttu-id="55351-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="55351-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55351-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="55351-114">-DisplayName</span></span>
<span data-ttu-id="55351-115">Имя, которое будет отображаться в адресной книге пользователя.</span><span class="sxs-lookup"><span data-stu-id="55351-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="55351-116">Пример "Алекс Wu".</span><span class="sxs-lookup"><span data-stu-id="55351-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="55351-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="55351-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="55351-118">Он должен быть указан, если пользователь должен сменить пароль при следующем успешном входе (истина).</span><span class="sxs-lookup"><span data-stu-id="55351-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="55351-119">По умолчанию используется значение (false), чтобы не менять пароль при следующем успешном входе.</span><span class="sxs-lookup"><span data-stu-id="55351-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="55351-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="55351-120">-ImmutableId</span></span>
<span data-ttu-id="55351-121">Он должен быть указан только в том случае, если вы используете федеративный домен для основного имени пользователя (UPN).</span><span class="sxs-lookup"><span data-stu-id="55351-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55351-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="55351-122">-MailNickname</span></span>
<span data-ttu-id="55351-123">Псевдоним почты для пользователя.</span><span class="sxs-lookup"><span data-stu-id="55351-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="55351-124">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="55351-124">-Password</span></span>
<span data-ttu-id="55351-125">Пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="55351-125">Password for the user.</span></span>
<span data-ttu-id="55351-126">Он должен соответствовать требованиям к сложности пароля клиента.</span><span class="sxs-lookup"><span data-stu-id="55351-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="55351-127">Рекомендуется установить надежный пароль.</span><span class="sxs-lookup"><span data-stu-id="55351-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55351-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="55351-128">-UserPrincipalName</span></span>
<span data-ttu-id="55351-129">Имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="55351-129">The user principal name.</span></span>
<span data-ttu-id="55351-130">Пример: " someuser@contoso.com ".</span><span class="sxs-lookup"><span data-stu-id="55351-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="55351-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55351-131">-Confirm</span></span>
<span data-ttu-id="55351-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55351-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55351-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55351-133">-WhatIf</span></span>
<span data-ttu-id="55351-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55351-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55351-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55351-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55351-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55351-136">CommonParameters</span></span>
<span data-ttu-id="55351-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55351-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55351-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55351-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55351-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55351-139">INPUTS</span></span>

### <span data-ttu-id="55351-140">System. String</span><span class="sxs-lookup"><span data-stu-id="55351-140">System.String</span></span>

### <span data-ttu-id="55351-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="55351-141">System.Security.SecureString</span></span>

### <span data-ttu-id="55351-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55351-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="55351-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55351-143">OUTPUTS</span></span>

### <span data-ttu-id="55351-144">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="55351-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="55351-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="55351-145">NOTES</span></span>

## <span data-ttu-id="55351-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55351-146">RELATED LINKS</span></span>

[<span data-ttu-id="55351-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="55351-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="55351-148">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="55351-148">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="55351-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="55351-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
