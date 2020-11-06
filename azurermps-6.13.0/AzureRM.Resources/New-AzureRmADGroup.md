---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADGroup.md
ms.openlocfilehash: 751b1b7daff59861b3f8e480b27dc4c88d35709d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564028"
---
# <span data-ttu-id="5e407-101">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="5e407-101">New-AzureRmADGroup</span></span>

## <span data-ttu-id="5e407-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e407-102">SYNOPSIS</span></span>
<span data-ttu-id="5e407-103">Создание новой группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5e407-103">Creates a new active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e407-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e407-104">SYNTAX</span></span>

```
New-AzureRmADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e407-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e407-105">DESCRIPTION</span></span>
<span data-ttu-id="5e407-106">Создание новой группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5e407-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="5e407-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e407-107">EXAMPLES</span></span>

### <span data-ttu-id="5e407-108">Пример 1: создание новой группы рекламных объявлений</span><span class="sxs-lookup"><span data-stu-id="5e407-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzureRmADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="5e407-109">Создание новой группы Active Directory с именем "MyGroupDisplayName" и псевдонимом почты " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="5e407-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="5e407-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e407-110">PARAMETERS</span></span>

### <span data-ttu-id="5e407-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e407-111">-DefaultProfile</span></span>
<span data-ttu-id="5e407-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e407-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e407-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5e407-113">-DisplayName</span></span>
<span data-ttu-id="5e407-114">Отображаемое имя группы.</span><span class="sxs-lookup"><span data-stu-id="5e407-114">The display name for the group.</span></span>

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

### <span data-ttu-id="5e407-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="5e407-115">-MailNickname</span></span>
<span data-ttu-id="5e407-116">Псевдоним электронной почты для группы.</span><span class="sxs-lookup"><span data-stu-id="5e407-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="5e407-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e407-117">-Confirm</span></span>
<span data-ttu-id="5e407-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e407-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e407-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e407-119">-WhatIf</span></span>
<span data-ttu-id="5e407-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e407-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e407-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e407-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e407-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e407-122">CommonParameters</span></span>
<span data-ttu-id="5e407-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e407-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e407-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e407-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e407-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e407-125">INPUTS</span></span>

### <span data-ttu-id="5e407-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5e407-126">System.String</span></span>

## <span data-ttu-id="5e407-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e407-127">OUTPUTS</span></span>

### <span data-ttu-id="5e407-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5e407-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="5e407-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e407-129">NOTES</span></span>

## <span data-ttu-id="5e407-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e407-130">RELATED LINKS</span></span>
