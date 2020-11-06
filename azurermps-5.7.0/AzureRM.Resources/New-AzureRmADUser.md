---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 80a35ac1a1087d9e74cb47c3297af3ded491e701
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563320"
---
# <span data-ttu-id="fe457-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fe457-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="fe457-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe457-102">SYNOPSIS</span></span>
<span data-ttu-id="fe457-103">Создание нового пользователя Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fe457-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe457-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe457-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe457-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe457-105">DESCRIPTION</span></span>
<span data-ttu-id="fe457-106">Создание нового пользователя Active Directory (рабочей или учебной учетной записи, которая известна как "org-ID").</span><span class="sxs-lookup"><span data-stu-id="fe457-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="fe457-107">Дополнительные сведения: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="fe457-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="fe457-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe457-108">EXAMPLES</span></span>

### <span data-ttu-id="fe457-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe457-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fe457-110">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="fe457-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="fe457-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe457-111">PARAMETERS</span></span>

### <span data-ttu-id="fe457-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe457-112">-DefaultProfile</span></span>
<span data-ttu-id="fe457-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fe457-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe457-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fe457-114">-DisplayName</span></span>
<span data-ttu-id="fe457-115">Имя, которое будет отображаться в адресной книге пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe457-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="fe457-116">Пример "Алекс Wu".</span><span class="sxs-lookup"><span data-stu-id="fe457-116">example 'Alex Wu'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe457-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="fe457-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="fe457-118">Он должен быть указан, если пользователь должен сменить пароль при следующем успешном входе (истина).</span><span class="sxs-lookup"><span data-stu-id="fe457-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="fe457-119">По умолчанию используется значение (false), чтобы не менять пароль при следующем успешном входе.</span><span class="sxs-lookup"><span data-stu-id="fe457-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe457-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="fe457-120">-ImmutableId</span></span>
<span data-ttu-id="fe457-121">Он должен быть указан только в том случае, если вы используете федеративный домен для основного имени пользователя (UPN).</span><span class="sxs-lookup"><span data-stu-id="fe457-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe457-122">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="fe457-122">-Password</span></span>
<span data-ttu-id="fe457-123">Пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe457-123">Password for the user.</span></span>
<span data-ttu-id="fe457-124">Он должен соответствовать требованиям к сложности пароля клиента.</span><span class="sxs-lookup"><span data-stu-id="fe457-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="fe457-125">Рекомендуется установить надежный пароль.</span><span class="sxs-lookup"><span data-stu-id="fe457-125">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe457-126">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fe457-126">-UserPrincipalName</span></span>
<span data-ttu-id="fe457-127">Имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe457-127">The user principal name.</span></span>
<span data-ttu-id="fe457-128">Пример: " someuser@contoso.com ".</span><span class="sxs-lookup"><span data-stu-id="fe457-128">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe457-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe457-129">-Confirm</span></span>
<span data-ttu-id="fe457-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe457-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe457-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe457-131">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe457-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe457-132">CommonParameters</span></span>
<span data-ttu-id="fe457-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe457-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe457-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe457-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe457-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe457-135">INPUTS</span></span>

### <span data-ttu-id="fe457-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="fe457-136">None</span></span>
<span data-ttu-id="fe457-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fe457-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe457-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe457-138">OUTPUTS</span></span>

### <span data-ttu-id="fe457-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="fe457-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="fe457-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe457-140">NOTES</span></span>

## <span data-ttu-id="fe457-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe457-141">RELATED LINKS</span></span>

[<span data-ttu-id="fe457-142">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fe457-142">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="fe457-143">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fe457-143">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="fe457-144">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fe457-144">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
