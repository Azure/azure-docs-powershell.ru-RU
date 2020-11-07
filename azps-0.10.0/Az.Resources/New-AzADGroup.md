---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: b5bc2f2eb99a8256dcaa6bc4f026d922f0f563ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910919"
---
# <span data-ttu-id="5dddb-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="5dddb-101">New-AzADGroup</span></span>

## <span data-ttu-id="5dddb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5dddb-102">SYNOPSIS</span></span>
<span data-ttu-id="5dddb-103">Создание новой группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5dddb-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="5dddb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5dddb-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dddb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dddb-105">DESCRIPTION</span></span>
<span data-ttu-id="5dddb-106">Создание новой группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5dddb-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="5dddb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5dddb-107">EXAMPLES</span></span>

### <span data-ttu-id="5dddb-108">Пример 1: создание новой группы рекламных объявлений</span><span class="sxs-lookup"><span data-stu-id="5dddb-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="5dddb-109">Создание новой группы Active Directory с именем "MyGroupDisplayName" и псевдонимом почты " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="5dddb-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="5dddb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5dddb-110">PARAMETERS</span></span>

### <span data-ttu-id="5dddb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dddb-111">-DefaultProfile</span></span>
<span data-ttu-id="5dddb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dddb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dddb-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5dddb-113">-DisplayName</span></span>
<span data-ttu-id="5dddb-114">Отображаемое имя группы.</span><span class="sxs-lookup"><span data-stu-id="5dddb-114">The display name for the group.</span></span>

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

### <span data-ttu-id="5dddb-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="5dddb-115">-MailNickname</span></span>
<span data-ttu-id="5dddb-116">Псевдоним электронной почты для группы.</span><span class="sxs-lookup"><span data-stu-id="5dddb-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="5dddb-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5dddb-117">-Confirm</span></span>
<span data-ttu-id="5dddb-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5dddb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dddb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dddb-119">-WhatIf</span></span>
<span data-ttu-id="5dddb-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5dddb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dddb-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5dddb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dddb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dddb-122">CommonParameters</span></span>
<span data-ttu-id="5dddb-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5dddb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dddb-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dddb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dddb-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5dddb-125">INPUTS</span></span>

### <span data-ttu-id="5dddb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5dddb-126">System.String</span></span>

## <span data-ttu-id="5dddb-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dddb-127">OUTPUTS</span></span>

### <span data-ttu-id="5dddb-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5dddb-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="5dddb-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5dddb-129">NOTES</span></span>

## <span data-ttu-id="5dddb-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dddb-130">RELATED LINKS</span></span>
