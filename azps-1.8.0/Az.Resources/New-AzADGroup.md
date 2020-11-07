---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 50cb6a806522e8e8b0f3a792ad74e2543633f668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729406"
---
# <span data-ttu-id="2e9d3-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="2e9d3-101">New-AzADGroup</span></span>

## <span data-ttu-id="2e9d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="2e9d3-103">Создание новой группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="2e9d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e9d3-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e9d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e9d3-105">DESCRIPTION</span></span>
<span data-ttu-id="2e9d3-106">Создание новой группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="2e9d3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e9d3-107">EXAMPLES</span></span>

### <span data-ttu-id="2e9d3-108">Пример 1: создание новой группы рекламных объявлений</span><span class="sxs-lookup"><span data-stu-id="2e9d3-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="2e9d3-109">Создание новой группы Active Directory с именем "MyGroupDisplayName" и псевдонимом почты "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="2e9d3-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="2e9d3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e9d3-110">PARAMETERS</span></span>

### <span data-ttu-id="2e9d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e9d3-111">-DefaultProfile</span></span>
<span data-ttu-id="2e9d3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e9d3-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2e9d3-113">-DisplayName</span></span>
<span data-ttu-id="2e9d3-114">Отображаемое имя группы.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-114">The display name for the group.</span></span>

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

### <span data-ttu-id="2e9d3-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="2e9d3-115">-MailNickname</span></span>
<span data-ttu-id="2e9d3-116">Псевдоним электронной почты для группы.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-116">The mail nickname for the group.</span></span> <span data-ttu-id="2e9d3-117">Не может содержать знак @.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-117">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="2e9d3-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e9d3-118">-Confirm</span></span>
<span data-ttu-id="2e9d3-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e9d3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e9d3-120">-WhatIf</span></span>
<span data-ttu-id="2e9d3-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e9d3-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e9d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e9d3-123">CommonParameters</span></span>
<span data-ttu-id="2e9d3-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e9d3-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e9d3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e9d3-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e9d3-126">INPUTS</span></span>

### <span data-ttu-id="2e9d3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2e9d3-127">System.String</span></span>

## <span data-ttu-id="2e9d3-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e9d3-128">OUTPUTS</span></span>

### <span data-ttu-id="2e9d3-129">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="2e9d3-129">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="2e9d3-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e9d3-130">NOTES</span></span>

## <span data-ttu-id="2e9d3-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e9d3-131">RELATED LINKS</span></span>
