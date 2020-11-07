---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: b0f4e67630a3a762fe78c9438c6ae39f948404c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734246"
---
# <span data-ttu-id="4e18c-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4e18c-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="4e18c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e18c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e18c-103">Удаляет пользователя Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e18c-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e18c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e18c-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e18c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e18c-105">DESCRIPTION</span></span>
<span data-ttu-id="4e18c-106">Удаление пользователя Active Directory (рабочей или учебной учетной записи, известной как "org-ID").</span><span class="sxs-lookup"><span data-stu-id="4e18c-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="4e18c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e18c-107">EXAMPLES</span></span>

### <span data-ttu-id="4e18c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e18c-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4e18c-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="4e18c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="4e18c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e18c-110">PARAMETERS</span></span>

### <span data-ttu-id="4e18c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4e18c-111">-Force</span></span>
<span data-ttu-id="4e18c-112">Если задано, не запрашивает подтверждение удаления пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e18c-112">If specified, doesn't ask for confirmation for deleting user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e18c-113">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="4e18c-113">-UPNOrObjectId</span></span>
<span data-ttu-id="4e18c-114">Имя субъекта-пользователя или ИД объекта пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4e18c-114">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="4e18c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e18c-115">-Confirm</span></span>
<span data-ttu-id="4e18c-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e18c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e18c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e18c-117">-WhatIf</span></span>
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

### <span data-ttu-id="4e18c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e18c-118">-DefaultProfile</span></span>
<span data-ttu-id="4e18c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e18c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e18c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e18c-120">CommonParameters</span></span>
<span data-ttu-id="4e18c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e18c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e18c-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e18c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e18c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e18c-123">INPUTS</span></span>

## <span data-ttu-id="4e18c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e18c-124">OUTPUTS</span></span>

## <span data-ttu-id="4e18c-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e18c-125">NOTES</span></span>

## <span data-ttu-id="4e18c-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e18c-126">RELATED LINKS</span></span>

[<span data-ttu-id="4e18c-127">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4e18c-127">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="4e18c-128">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4e18c-128">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="4e18c-129">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4e18c-129">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

