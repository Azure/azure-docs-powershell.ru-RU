---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: fa9f708355e9c2fd4df530955db1d893e7591740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913970"
---
# <span data-ttu-id="fcdd5-101">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="fcdd5-101">New-AzureRmADGroup</span></span>

## <span data-ttu-id="fcdd5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fcdd5-102">SYNOPSIS</span></span>
<span data-ttu-id="fcdd5-103">Создание новой группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-103">Creates a new active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcdd5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fcdd5-104">SYNTAX</span></span>

```
New-AzureRmADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcdd5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcdd5-105">DESCRIPTION</span></span>
<span data-ttu-id="fcdd5-106">Создание новой группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="fcdd5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fcdd5-107">EXAMPLES</span></span>

### <span data-ttu-id="fcdd5-108">Пример 1: создание новой группы рекламных объявлений</span><span class="sxs-lookup"><span data-stu-id="fcdd5-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzureRmADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="fcdd5-109">Создание новой группы Active Directory с именем "MyGroupDisplayName" и псевдонимом почты " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="fcdd5-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="fcdd5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fcdd5-110">PARAMETERS</span></span>

### <span data-ttu-id="fcdd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcdd5-111">-DefaultProfile</span></span>
<span data-ttu-id="fcdd5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcdd5-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fcdd5-113">-DisplayName</span></span>
<span data-ttu-id="fcdd5-114">Отображаемое имя группы.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-114">The display name for the group.</span></span>

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

### <span data-ttu-id="fcdd5-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="fcdd5-115">-MailNickname</span></span>
<span data-ttu-id="fcdd5-116">Псевдоним электронной почты для группы.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="fcdd5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcdd5-117">-Confirm</span></span>
<span data-ttu-id="fcdd5-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcdd5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcdd5-119">-WhatIf</span></span>
<span data-ttu-id="fcdd5-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcdd5-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcdd5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcdd5-122">CommonParameters</span></span>
<span data-ttu-id="fcdd5-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fcdd5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcdd5-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcdd5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcdd5-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fcdd5-125">INPUTS</span></span>

### <span data-ttu-id="fcdd5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fcdd5-126">System.String</span></span>

## <span data-ttu-id="fcdd5-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcdd5-127">OUTPUTS</span></span>

### <span data-ttu-id="fcdd5-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="fcdd5-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="fcdd5-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="fcdd5-129">NOTES</span></span>

## <span data-ttu-id="fcdd5-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcdd5-130">RELATED LINKS</span></span>
