---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557187"
---
# <span data-ttu-id="2f0a8-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="2f0a8-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="2f0a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0a8-103">Обновление существующего пользователя Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f0a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f0a8-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f0a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f0a8-105">DESCRIPTION</span></span>
<span data-ttu-id="2f0a8-106">Обновление существующего пользователя Active Directory (рабочей или учебной учетной записи, известной как "org-ID").</span><span class="sxs-lookup"><span data-stu-id="2f0a8-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="2f0a8-107">Дополнительные сведения: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="2f0a8-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="2f0a8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f0a8-108">EXAMPLES</span></span>

### <span data-ttu-id="2f0a8-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f0a8-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2f0a8-110">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="2f0a8-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="2f0a8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f0a8-111">PARAMETERS</span></span>

### <span data-ttu-id="2f0a8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0a8-112">-DefaultProfile</span></span>
<span data-ttu-id="2f0a8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2f0a8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f0a8-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2f0a8-114">-DisplayName</span></span>
<span data-ttu-id="2f0a8-115">Новое имя, которое будет отображаться в адресной книге пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-115">New name to display in the address book for the user.</span></span>
<span data-ttu-id="2f0a8-116">Пример — 'Alex Wu.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-116">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="2f0a8-117">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="2f0a8-117">-EnableAccount</span></span>
<span data-ttu-id="2f0a8-118">Значение true для включения учетной записи; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-118">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f0a8-119">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="2f0a8-119">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="2f0a8-120">Он должен быть указан только в том случае, если вы обновляете пароль.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-120">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="2f0a8-121">В противном случае оно будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-121">Otherwise it will be ignored.</span></span>
<span data-ttu-id="2f0a8-122">Он должен быть указан, если пользователь должен сменить пароль при следующем успешном входе (истина).</span><span class="sxs-lookup"><span data-stu-id="2f0a8-122">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="2f0a8-123">По умолчанию используется значение (false), чтобы не менять пароль при следующем успешном входе.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-123">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="2f0a8-124">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="2f0a8-124">-Password</span></span>
<span data-ttu-id="2f0a8-125">Новый пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-125">New password for the user.</span></span>
<span data-ttu-id="2f0a8-126">Он должен соответствовать требованиям к сложности пароля клиента.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="2f0a8-127">Рекомендуется установить надежный пароль.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-127">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f0a8-128">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="2f0a8-128">-UPNOrObjectId</span></span>
<span data-ttu-id="2f0a8-129">Имя участника-пользователя (например, " someuser@contoso.com ") или ObjectID пользователя, для которого нужно обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-129">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="2f0a8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f0a8-130">-Confirm</span></span>
<span data-ttu-id="2f0a8-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f0a8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f0a8-132">-WhatIf</span></span>
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

### <span data-ttu-id="2f0a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0a8-133">CommonParameters</span></span>
<span data-ttu-id="2f0a8-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0a8-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f0a8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0a8-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f0a8-136">INPUTS</span></span>

### <span data-ttu-id="2f0a8-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="2f0a8-137">None</span></span>
<span data-ttu-id="2f0a8-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2f0a8-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f0a8-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f0a8-139">OUTPUTS</span></span>

### <span data-ttu-id="2f0a8-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="2f0a8-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="2f0a8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f0a8-141">NOTES</span></span>

## <span data-ttu-id="2f0a8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f0a8-142">RELATED LINKS</span></span>

[<span data-ttu-id="2f0a8-143">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="2f0a8-143">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="2f0a8-144">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="2f0a8-144">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="2f0a8-145">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="2f0a8-145">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

