---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732195"
---
# <span data-ttu-id="ee34e-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ee34e-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="ee34e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee34e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee34e-103">Обновление существующего пользователя Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ee34e-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee34e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee34e-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee34e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee34e-105">DESCRIPTION</span></span>
<span data-ttu-id="ee34e-106">Обновление существующего пользователя Active Directory (рабочей или учебной учетной записи, известной как "org-ID").</span><span class="sxs-lookup"><span data-stu-id="ee34e-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="ee34e-107">Дополнительные сведения: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="ee34e-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="ee34e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee34e-108">EXAMPLES</span></span>

### <span data-ttu-id="ee34e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee34e-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ee34e-110">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="ee34e-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="ee34e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee34e-111">PARAMETERS</span></span>

### <span data-ttu-id="ee34e-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ee34e-112">-DisplayName</span></span>
<span data-ttu-id="ee34e-113">Новое имя, которое будет отображаться в адресной книге пользователя.</span><span class="sxs-lookup"><span data-stu-id="ee34e-113">New name to display in the address book for the user.</span></span>
<span data-ttu-id="ee34e-114">Пример — 'Alex Wu.</span><span class="sxs-lookup"><span data-stu-id="ee34e-114">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="ee34e-115">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="ee34e-115">-EnableAccount</span></span>
<span data-ttu-id="ee34e-116">Значение true для включения учетной записи; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="ee34e-116">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee34e-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="ee34e-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="ee34e-118">Он должен быть указан только в том случае, если вы обновляете пароль.</span><span class="sxs-lookup"><span data-stu-id="ee34e-118">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="ee34e-119">В противном случае оно будет проигнорировано.</span><span class="sxs-lookup"><span data-stu-id="ee34e-119">Otherwise it will be ignored.</span></span>
<span data-ttu-id="ee34e-120">Он должен быть указан, если пользователь должен сменить пароль при следующем успешном входе (истина).</span><span class="sxs-lookup"><span data-stu-id="ee34e-120">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="ee34e-121">По умолчанию используется значение (false), чтобы не менять пароль при следующем успешном входе.</span><span class="sxs-lookup"><span data-stu-id="ee34e-121">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="ee34e-122">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="ee34e-122">-Password</span></span>
<span data-ttu-id="ee34e-123">Новый пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="ee34e-123">New password for the user.</span></span>
<span data-ttu-id="ee34e-124">Он должен соответствовать требованиям к сложности пароля клиента.</span><span class="sxs-lookup"><span data-stu-id="ee34e-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="ee34e-125">Рекомендуется установить надежный пароль.</span><span class="sxs-lookup"><span data-stu-id="ee34e-125">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="ee34e-126">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="ee34e-126">-UPNOrObjectId</span></span>
<span data-ttu-id="ee34e-127">Имя участника-пользователя (например, " someuser@contoso.com ") или ObjectID пользователя, для которого нужно обновить свойства.</span><span class="sxs-lookup"><span data-stu-id="ee34e-127">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="ee34e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee34e-128">-Confirm</span></span>
<span data-ttu-id="ee34e-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee34e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee34e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee34e-130">-WhatIf</span></span>
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

### <span data-ttu-id="ee34e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee34e-131">-DefaultProfile</span></span>
<span data-ttu-id="ee34e-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee34e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee34e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee34e-133">CommonParameters</span></span>
<span data-ttu-id="ee34e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee34e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee34e-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee34e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee34e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee34e-136">INPUTS</span></span>

## <span data-ttu-id="ee34e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee34e-137">OUTPUTS</span></span>

### <span data-ttu-id="ee34e-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="ee34e-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ee34e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee34e-139">NOTES</span></span>

## <span data-ttu-id="ee34e-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee34e-140">RELATED LINKS</span></span>

[<span data-ttu-id="ee34e-141">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ee34e-141">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="ee34e-142">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ee34e-142">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="ee34e-143">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ee34e-143">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

