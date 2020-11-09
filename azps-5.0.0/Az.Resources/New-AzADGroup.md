---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316352"
---
# <span data-ttu-id="cd252-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="cd252-101">New-AzADGroup</span></span>

## <span data-ttu-id="cd252-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd252-102">SYNOPSIS</span></span>
<span data-ttu-id="cd252-103">Создание новой группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cd252-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="cd252-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd252-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd252-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd252-105">DESCRIPTION</span></span>
<span data-ttu-id="cd252-106">Создание новой группы Active Directory. Ниже приводятся необходимые разрешения:</span><span class="sxs-lookup"><span data-stu-id="cd252-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="cd252-107">Graph Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="cd252-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="cd252-108">Directory. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="cd252-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="cd252-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="cd252-109">Microsoft Graph</span></span>
  - <span data-ttu-id="cd252-110">Directory. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="cd252-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="cd252-111">PrivilegedAccess. ReadWrite. AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="cd252-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="cd252-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd252-112">EXAMPLES</span></span>

### <span data-ttu-id="cd252-113">Пример 1: создание новой группы рекламных объявлений</span><span class="sxs-lookup"><span data-stu-id="cd252-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="cd252-114">Создание новой группы Active Directory с именем "MyGroupDisplayName" и псевдонимом почты "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="cd252-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="cd252-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd252-115">PARAMETERS</span></span>

### <span data-ttu-id="cd252-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd252-116">-DefaultProfile</span></span>
<span data-ttu-id="cd252-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd252-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd252-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="cd252-118">-Description</span></span>
<span data-ttu-id="cd252-119">Описание группы.</span><span class="sxs-lookup"><span data-stu-id="cd252-119">The description for the group.</span></span>

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

### <span data-ttu-id="cd252-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd252-120">-DisplayName</span></span>
<span data-ttu-id="cd252-121">Отображаемое имя группы.</span><span class="sxs-lookup"><span data-stu-id="cd252-121">The display name for the group.</span></span>

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

### <span data-ttu-id="cd252-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="cd252-122">-MailNickname</span></span>
<span data-ttu-id="cd252-123">Псевдоним электронной почты для группы.</span><span class="sxs-lookup"><span data-stu-id="cd252-123">The mail nickname for the group.</span></span> <span data-ttu-id="cd252-124">Не может содержать знак @.</span><span class="sxs-lookup"><span data-stu-id="cd252-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="cd252-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd252-125">-Confirm</span></span>
<span data-ttu-id="cd252-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd252-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd252-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd252-127">-WhatIf</span></span>
<span data-ttu-id="cd252-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd252-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd252-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd252-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd252-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd252-130">CommonParameters</span></span>
<span data-ttu-id="cd252-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd252-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd252-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd252-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd252-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd252-133">INPUTS</span></span>

### <span data-ttu-id="cd252-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cd252-134">System.String</span></span>

## <span data-ttu-id="cd252-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd252-135">OUTPUTS</span></span>

### <span data-ttu-id="cd252-136">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="cd252-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="cd252-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd252-137">NOTES</span></span>

## <span data-ttu-id="cd252-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd252-138">RELATED LINKS</span></span>
