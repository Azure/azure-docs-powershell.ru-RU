---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: cd8834dd329ab82e98316cb0d94b554eb3bb6c13
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408327"
---
# <span data-ttu-id="ed261-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ed261-101">New-AzADUser</span></span>

## <span data-ttu-id="ed261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed261-102">SYNOPSIS</span></span>
<span data-ttu-id="ed261-103">Создает нового пользователя Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ed261-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="ed261-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed261-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed261-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed261-105">DESCRIPTION</span></span>
<span data-ttu-id="ed261-106">Создает нового пользователя Active Directory (рабочих и учебных учетных записей, также известных как ид организации).</span><span class="sxs-lookup"><span data-stu-id="ed261-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="ed261-107">Дополнительные сведения https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="ed261-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="ed261-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed261-108">EXAMPLES</span></span>

### <span data-ttu-id="ed261-109">Пример 1. Создание нового пользователя с AD</span><span class="sxs-lookup"><span data-stu-id="ed261-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="ed261-110">Создает нового пользователя AD с именем MyDisplayName и именем директора пользователя myemail@domain.com " в клиенте.</span><span class="sxs-lookup"><span data-stu-id="ed261-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="ed261-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed261-111">PARAMETERS</span></span>

### <span data-ttu-id="ed261-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed261-112">-DefaultProfile</span></span>
<span data-ttu-id="ed261-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed261-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed261-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed261-114">-DisplayName</span></span>
<span data-ttu-id="ed261-115">Имя, которое будет отображаться в адресной книге пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed261-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="ed261-116">пример "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="ed261-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="ed261-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="ed261-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="ed261-118">При следующем успешном входе необходимо у указывается, должен ли пользователь изменить пароль (true).</span><span class="sxs-lookup"><span data-stu-id="ed261-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="ed261-119">По умолчанию (false) не нужно менять пароль при следующем успешном входе в систему.</span><span class="sxs-lookup"><span data-stu-id="ed261-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="ed261-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="ed261-120">-ImmutableId</span></span>
<span data-ttu-id="ed261-121">Его нужно укадрять только в том случае, если вы используете федератный домен в качестве свойства имени пользователя (upn).</span><span class="sxs-lookup"><span data-stu-id="ed261-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="ed261-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="ed261-122">-MailNickname</span></span>
<span data-ttu-id="ed261-123">Псевдоним электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed261-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="ed261-124">-Password</span><span class="sxs-lookup"><span data-stu-id="ed261-124">-Password</span></span>
<span data-ttu-id="ed261-125">Пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed261-125">Password for the user.</span></span>
<span data-ttu-id="ed261-126">Оно должно соответствовать требованиям клиента к сложности паролей.</span><span class="sxs-lookup"><span data-stu-id="ed261-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="ed261-127">Рекомендуется установить надежный пароль.</span><span class="sxs-lookup"><span data-stu-id="ed261-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="ed261-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ed261-128">-UserPrincipalName</span></span>
<span data-ttu-id="ed261-129">Имя директора пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed261-129">The user principal name.</span></span>
<span data-ttu-id="ed261-130">Example-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="ed261-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="ed261-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed261-131">-Confirm</span></span>
<span data-ttu-id="ed261-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ed261-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed261-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed261-133">-WhatIf</span></span>
<span data-ttu-id="ed261-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed261-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed261-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ed261-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed261-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed261-136">CommonParameters</span></span>
<span data-ttu-id="ed261-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed261-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed261-138">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed261-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed261-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed261-139">INPUTS</span></span>

### <span data-ttu-id="ed261-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ed261-140">System.String</span></span>

### <span data-ttu-id="ed261-141">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="ed261-141">System.Security.SecureString</span></span>

### <span data-ttu-id="ed261-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ed261-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ed261-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed261-143">OUTPUTS</span></span>

### <span data-ttu-id="ed261-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="ed261-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ed261-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed261-145">NOTES</span></span>

## <span data-ttu-id="ed261-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed261-146">RELATED LINKS</span></span>

[<span data-ttu-id="ed261-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ed261-147">Get-AzADUser</span></span>](./Get-AzADUser.md)


[<span data-ttu-id="ed261-148">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ed261-148">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
